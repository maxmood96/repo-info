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
$ docker pull spark@sha256:3f3a4fdd853e3c42c386e1ae1afebf0177d08f0a683a3813d130f5fd2099bf88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3` - linux; amd64

```console
$ docker pull spark@sha256:a220aa6e2a34def1cee4ef0f2931489fc8842843f2e86ecac80592bf7b59d1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528438314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cb8e09cb396ea76ee5b1c82d28162fef7b8acfe0edeb0b746fd8596ee275ba`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38794addc8141986ab7e424a67a45cc6a9a6d230f9e679063fcf8099dc4ad4dd`  
		Last Modified: Sat, 19 Oct 2024 03:58:59 GMT  
		Size: 94.4 MB (94363835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3` - unknown; unknown

```console
$ docker pull spark@sha256:7de97f8ec98a1ef0ecc8c5252b665feedc7d0a20690a615b5e4595a4ef0facd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9095740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e963eb3d72489d009b3f14199f624d007c3ff2fde7e420bed7304a32f91a7d9a`

```dockerfile
```

-	Layers:
	-	`sha256:8585d699e5dc47e54e680cbade7c61983e8a0361c17a55f67fcf1366993cb051`  
		Last Modified: Sat, 19 Oct 2024 03:58:56 GMT  
		Size: 9.1 MB (9084771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289ae91f584276931957cd24c0cfc6376df08a6d8238fcfdf758e9693383c8b9`  
		Last Modified: Sat, 19 Oct 2024 03:58:56 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:22b17d8d99f08403dbee950b2a6f9da38e0d119ecae1bc542837b8d3c71f36d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.8 MB (517796442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33004d1b1a1fa7d95ee331a58fbf6f883206091e7866da5428777e23b43fc2a4`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35caf147190528611faa01a478bed13c2a6921b4f15ad3254dee40c86c622d7`  
		Last Modified: Sat, 19 Oct 2024 20:56:44 GMT  
		Size: 87.3 MB (87320502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3` - unknown; unknown

```console
$ docker pull spark@sha256:08c8fb81feb7c91e519442a5f739dd29fb1623c2738e4dce37c62ba4c00e02ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9099632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57d589e4de720c9d4f0117ae659d26faab30e95474d5700b3c11aa3f23a9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:b55a7c96504dde61ff5cfc4adedc9416a46e3b018eb1d63fdda669d72a0c67ac`  
		Last Modified: Sat, 19 Oct 2024 20:56:38 GMT  
		Size: 9.1 MB (9088571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade45bb19ce79cd451976a81a4f40f15d2c3188d47c5679c85057927d385c98c`  
		Last Modified: Sat, 19 Oct 2024 20:56:38 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-python3`

```console
$ docker pull spark@sha256:3f3a4fdd853e3c42c386e1ae1afebf0177d08f0a683a3813d130f5fd2099bf88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-python3` - linux; amd64

```console
$ docker pull spark@sha256:a220aa6e2a34def1cee4ef0f2931489fc8842843f2e86ecac80592bf7b59d1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528438314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cb8e09cb396ea76ee5b1c82d28162fef7b8acfe0edeb0b746fd8596ee275ba`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38794addc8141986ab7e424a67a45cc6a9a6d230f9e679063fcf8099dc4ad4dd`  
		Last Modified: Sat, 19 Oct 2024 03:58:59 GMT  
		Size: 94.4 MB (94363835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:7de97f8ec98a1ef0ecc8c5252b665feedc7d0a20690a615b5e4595a4ef0facd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9095740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e963eb3d72489d009b3f14199f624d007c3ff2fde7e420bed7304a32f91a7d9a`

```dockerfile
```

-	Layers:
	-	`sha256:8585d699e5dc47e54e680cbade7c61983e8a0361c17a55f67fcf1366993cb051`  
		Last Modified: Sat, 19 Oct 2024 03:58:56 GMT  
		Size: 9.1 MB (9084771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289ae91f584276931957cd24c0cfc6376df08a6d8238fcfdf758e9693383c8b9`  
		Last Modified: Sat, 19 Oct 2024 03:58:56 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:22b17d8d99f08403dbee950b2a6f9da38e0d119ecae1bc542837b8d3c71f36d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.8 MB (517796442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33004d1b1a1fa7d95ee331a58fbf6f883206091e7866da5428777e23b43fc2a4`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35caf147190528611faa01a478bed13c2a6921b4f15ad3254dee40c86c622d7`  
		Last Modified: Sat, 19 Oct 2024 20:56:44 GMT  
		Size: 87.3 MB (87320502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:08c8fb81feb7c91e519442a5f739dd29fb1623c2738e4dce37c62ba4c00e02ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9099632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57d589e4de720c9d4f0117ae659d26faab30e95474d5700b3c11aa3f23a9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:b55a7c96504dde61ff5cfc4adedc9416a46e3b018eb1d63fdda669d72a0c67ac`  
		Last Modified: Sat, 19 Oct 2024 20:56:38 GMT  
		Size: 9.1 MB (9088571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade45bb19ce79cd451976a81a4f40f15d2c3188d47c5679c85057927d385c98c`  
		Last Modified: Sat, 19 Oct 2024 20:56:38 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-r`

```console
$ docker pull spark@sha256:bb903d53afb7d2f779cc0e2c2b30cb4b0dfbf517efa63797e86b36387ee09dbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-r` - linux; amd64

```console
$ docker pull spark@sha256:4bcde2c8634c2addfd04363dd4eca319d1e1bb205a81015ae6718aa8fe4ff24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.4 MB (666367816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e703f2d8f29c4a323245e5f3d56f0fc572d23f7210aaca132829eb2522c34606`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266792957be2e8ae0163ec36dcdd2158b1c6bb1dba649d426eca592836a5b93c`  
		Last Modified: Sat, 19 Oct 2024 03:59:41 GMT  
		Size: 232.3 MB (232293337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:00783c539be9c5566f495468327bdbfbc8a6527ed976069ff222dd985a206cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11268788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf13bc7a46e2bea2c91eeda848433069d97c397c5fa2cb1f122a645a64ac944`

```dockerfile
```

-	Layers:
	-	`sha256:c07d40f8de61c1c9319bcfc36842d07a346eef2cd62d4e0d6aef905c837b3cf3`  
		Last Modified: Sat, 19 Oct 2024 03:59:37 GMT  
		Size: 11.3 MB (11258122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718f2c0efcc733520df12e16192441d77a7fd99efe958f23ee3fd82963844121`  
		Last Modified: Sat, 19 Oct 2024 03:59:36 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:509df66403d7e61e072ac30c94bcb86dcd6d7da70ed48859d236745eb912d11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.0 MB (643982857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409498bb39c5df8ece9a1ccaa79f6db6d68bb3749307d52c3af4461ab99f72f1`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e2cb9cc04e4afc883692146a42894462e423bf5051530e47e8c97e95f80cd2`  
		Last Modified: Sat, 19 Oct 2024 20:59:30 GMT  
		Size: 213.5 MB (213506917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:275936ee95dff15a76f48f90a09543fcfb349597c270672b982d912eefd795f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11252989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba96b23efaec902cd3340706feb42d56c3e1ea753d1038ec64dabd50efbec17c`

```dockerfile
```

-	Layers:
	-	`sha256:f96342dd89c4730611bc8cf83dd7498c3947b5dd8937091bb32159d5a441c71e`  
		Last Modified: Sat, 19 Oct 2024 20:59:25 GMT  
		Size: 11.2 MB (11242243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60b593813c6d4b8d48e032cb4e0a2f91e94d25696ca1bfbae6d7f7d9adc09b5`  
		Last Modified: Sat, 19 Oct 2024 20:59:25 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala`

```console
$ docker pull spark@sha256:23dd72d196908422a86648cfd14a4c6ddde15d554fc86bdb8291414b53fb014d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala` - linux; amd64

```console
$ docker pull spark@sha256:11000153d7287f9e09343894b06bd03fb6e65f399ced8bac19b179cdbabdd6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.1 MB (434074479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f19eb8ae6e3f7f469cefbb12b0ea2b0d9aff8b2f512461008098b6f67bd87`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:365728b0bc1cf5cf274a5419b3141cef5fced592c201739ae2d07e42c87508b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96173cbb3da52701c9b944bcaf82f9827995a29f927a4f4abe7f8c795af4374`

```dockerfile
```

-	Layers:
	-	`sha256:f6ec6c013a0b762e57a7ebdea4a48e66d44213d4dff060ef4a165e3251026793`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 4.4 MB (4354160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc668ed2789e1c87a071bf995c04aa84fb0d61e13e91e4d2bc8d6496c0436d8`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 22.4 KB (22432 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:59b31ad4707effddf8fbd00a0764b9fe089115db7a4e4df54b6b5f3416da7967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.5 MB (430475940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311d95f225e7ef3a2e7dc0c8fab82f07b28445031d130b2d37679679651f83be`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:38343bacbb8fc141d5469ab054100e8462e424443cfc2c13d151ac8b871ec197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c63e832d8ba6bcc1bc6b51a170f5f2a05194bc6f544ef0a66eb08fef73b23ae`

```dockerfile
```

-	Layers:
	-	`sha256:5e87ed62daf9a8a67b20e6061126cfb9d6f5db1f4ba015d1f8a89ba4071a8e4e`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 4.4 MB (4354451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0c56a53531cec217064d6454b77e0b3c985350e667c1fd808590243b09492c`  
		Last Modified: Sat, 19 Oct 2024 10:34:56 GMT  
		Size: 22.5 KB (22543 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:daef7273e07874e2bab456cbbb5c2d038fa5e46e7adfff1083c008fbee32a0a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:43fe0524ac292ddd28ea2803b084cf51ca9d3a2a27a8781bc62dccb2c28c4ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687985389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a19a98d07c914c9aa2cfefebde2296bd4cc7850cfc7b9c6f42f927f17debcf`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8d932ce8198d290b9c048e144df2e55b0bc2dec4ba2387d56bd51c05b2213`  
		Last Modified: Sat, 19 Oct 2024 03:57:08 GMT  
		Size: 253.9 MB (253910910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c9afc57e2fe3bb8b1e37946e331c4a09b909f18f47ca62fc2900e6a9bbb688da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12394704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc3ba117680b14bb1a00a7d2ec71e93f45e80887eab2878edf89d0483c9b852`

```dockerfile
```

-	Layers:
	-	`sha256:24da3c1f0428e8a569b2e668d0c8a63e92bd466c40d845f947673b4416ed8e8a`  
		Last Modified: Sat, 19 Oct 2024 03:57:05 GMT  
		Size: 12.4 MB (12384160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961d2d20144b1b9e6a52e22d867338eb4be1764f5cb92c38c5a20ec81ca1530c`  
		Last Modified: Sat, 19 Oct 2024 03:57:05 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:6810a51ce51caca8702140979c0cacc65b89146d82dd68213db46432ccdbdd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.6 MB (665617114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3555eb54774dc977f6799f6563bcf053dc221588353a00514d500750c4e4dc93`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38df9fed25433d6e6f0314c82467914ce376418beaecbd1f171044bb30b1a7cd`  
		Last Modified: Sat, 19 Oct 2024 20:30:09 GMT  
		Size: 235.1 MB (235141174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:ff266c960090086913578e18609bfd6620fdca251641618a449cda0534b195d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12378948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723bcd72e38e8fd669136a7e8ee782ec5278beb5e47057c3deb74db861178ba`

```dockerfile
```

-	Layers:
	-	`sha256:a4899657ecd05b156930b1e790fedd0452e32a79fc28e1c8cb1846a063b02867`  
		Last Modified: Sat, 19 Oct 2024 20:30:04 GMT  
		Size: 12.4 MB (12368336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307226f1e9c9a94a40162a29cbb5697f3028940ae9b48cc35b461a9f5fc8a025`  
		Last Modified: Sat, 19 Oct 2024 20:30:03 GMT  
		Size: 10.6 KB (10612 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:3f3a4fdd853e3c42c386e1ae1afebf0177d08f0a683a3813d130f5fd2099bf88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a220aa6e2a34def1cee4ef0f2931489fc8842843f2e86ecac80592bf7b59d1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528438314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cb8e09cb396ea76ee5b1c82d28162fef7b8acfe0edeb0b746fd8596ee275ba`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38794addc8141986ab7e424a67a45cc6a9a6d230f9e679063fcf8099dc4ad4dd`  
		Last Modified: Sat, 19 Oct 2024 03:58:59 GMT  
		Size: 94.4 MB (94363835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:7de97f8ec98a1ef0ecc8c5252b665feedc7d0a20690a615b5e4595a4ef0facd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9095740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e963eb3d72489d009b3f14199f624d007c3ff2fde7e420bed7304a32f91a7d9a`

```dockerfile
```

-	Layers:
	-	`sha256:8585d699e5dc47e54e680cbade7c61983e8a0361c17a55f67fcf1366993cb051`  
		Last Modified: Sat, 19 Oct 2024 03:58:56 GMT  
		Size: 9.1 MB (9084771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289ae91f584276931957cd24c0cfc6376df08a6d8238fcfdf758e9693383c8b9`  
		Last Modified: Sat, 19 Oct 2024 03:58:56 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:22b17d8d99f08403dbee950b2a6f9da38e0d119ecae1bc542837b8d3c71f36d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.8 MB (517796442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33004d1b1a1fa7d95ee331a58fbf6f883206091e7866da5428777e23b43fc2a4`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35caf147190528611faa01a478bed13c2a6921b4f15ad3254dee40c86c622d7`  
		Last Modified: Sat, 19 Oct 2024 20:56:44 GMT  
		Size: 87.3 MB (87320502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:08c8fb81feb7c91e519442a5f739dd29fb1623c2738e4dce37c62ba4c00e02ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9099632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57d589e4de720c9d4f0117ae659d26faab30e95474d5700b3c11aa3f23a9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:b55a7c96504dde61ff5cfc4adedc9416a46e3b018eb1d63fdda669d72a0c67ac`  
		Last Modified: Sat, 19 Oct 2024 20:56:38 GMT  
		Size: 9.1 MB (9088571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade45bb19ce79cd451976a81a4f40f15d2c3188d47c5679c85057927d385c98c`  
		Last Modified: Sat, 19 Oct 2024 20:56:38 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:bb903d53afb7d2f779cc0e2c2b30cb4b0dfbf517efa63797e86b36387ee09dbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:4bcde2c8634c2addfd04363dd4eca319d1e1bb205a81015ae6718aa8fe4ff24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.4 MB (666367816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e703f2d8f29c4a323245e5f3d56f0fc572d23f7210aaca132829eb2522c34606`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266792957be2e8ae0163ec36dcdd2158b1c6bb1dba649d426eca592836a5b93c`  
		Last Modified: Sat, 19 Oct 2024 03:59:41 GMT  
		Size: 232.3 MB (232293337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:00783c539be9c5566f495468327bdbfbc8a6527ed976069ff222dd985a206cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11268788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf13bc7a46e2bea2c91eeda848433069d97c397c5fa2cb1f122a645a64ac944`

```dockerfile
```

-	Layers:
	-	`sha256:c07d40f8de61c1c9319bcfc36842d07a346eef2cd62d4e0d6aef905c837b3cf3`  
		Last Modified: Sat, 19 Oct 2024 03:59:37 GMT  
		Size: 11.3 MB (11258122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718f2c0efcc733520df12e16192441d77a7fd99efe958f23ee3fd82963844121`  
		Last Modified: Sat, 19 Oct 2024 03:59:36 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:509df66403d7e61e072ac30c94bcb86dcd6d7da70ed48859d236745eb912d11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.0 MB (643982857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409498bb39c5df8ece9a1ccaa79f6db6d68bb3749307d52c3af4461ab99f72f1`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e2cb9cc04e4afc883692146a42894462e423bf5051530e47e8c97e95f80cd2`  
		Last Modified: Sat, 19 Oct 2024 20:59:30 GMT  
		Size: 213.5 MB (213506917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:275936ee95dff15a76f48f90a09543fcfb349597c270672b982d912eefd795f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11252989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba96b23efaec902cd3340706feb42d56c3e1ea753d1038ec64dabd50efbec17c`

```dockerfile
```

-	Layers:
	-	`sha256:f96342dd89c4730611bc8cf83dd7498c3947b5dd8937091bb32159d5a441c71e`  
		Last Modified: Sat, 19 Oct 2024 20:59:25 GMT  
		Size: 11.2 MB (11242243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60b593813c6d4b8d48e032cb4e0a2f91e94d25696ca1bfbae6d7f7d9adc09b5`  
		Last Modified: Sat, 19 Oct 2024 20:59:25 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:23dd72d196908422a86648cfd14a4c6ddde15d554fc86bdb8291414b53fb014d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:11000153d7287f9e09343894b06bd03fb6e65f399ced8bac19b179cdbabdd6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.1 MB (434074479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f19eb8ae6e3f7f469cefbb12b0ea2b0d9aff8b2f512461008098b6f67bd87`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886805ade7d29fc416e9a112a3ded4e29f4692b3572789a16d26f0a7487b5ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812fa63a24eb4a6c3b48ce48aeb9f25e727b9ff1df86e561cee574bd8839a2a`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 23.9 MB (23947242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28fba303f91cd0585c746701d3ba9efc8994bae373a8e5a2d41e8a6884eac25`  
		Last Modified: Sat, 19 Oct 2024 02:59:10 GMT  
		Size: 318.5 MB (318481064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c457bac9986e62dabf0fa89a1fd91a0ef633b551dae6c3ccaa992cacde34f21`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:365728b0bc1cf5cf274a5419b3141cef5fced592c201739ae2d07e42c87508b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96173cbb3da52701c9b944bcaf82f9827995a29f927a4f4abe7f8c795af4374`

```dockerfile
```

-	Layers:
	-	`sha256:f6ec6c013a0b762e57a7ebdea4a48e66d44213d4dff060ef4a165e3251026793`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 4.4 MB (4354160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc668ed2789e1c87a071bf995c04aa84fb0d61e13e91e4d2bc8d6496c0436d8`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 22.4 KB (22432 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:59b31ad4707effddf8fbd00a0764b9fe089115db7a4e4df54b6b5f3416da7967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.5 MB (430475940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311d95f225e7ef3a2e7dc0c8fab82f07b28445031d130b2d37679679651f83be`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3188a6b6a3ba404d0b2f67cd93ddf16952b01e7b10869b0ebe6d26eb6da36df`  
		Last Modified: Sat, 19 Oct 2024 10:35:03 GMT  
		Size: 318.5 MB (318481047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27694777c4c06d1633afcc52b890d1cc57a15074f4508433e44270d09beb`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:38343bacbb8fc141d5469ab054100e8462e424443cfc2c13d151ac8b871ec197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c63e832d8ba6bcc1bc6b51a170f5f2a05194bc6f544ef0a66eb08fef73b23ae`

```dockerfile
```

-	Layers:
	-	`sha256:5e87ed62daf9a8a67b20e6061126cfb9d6f5db1f4ba015d1f8a89ba4071a8e4e`  
		Last Modified: Sat, 19 Oct 2024 10:34:57 GMT  
		Size: 4.4 MB (4354451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0c56a53531cec217064d6454b77e0b3c985350e667c1fd808590243b09492c`  
		Last Modified: Sat, 19 Oct 2024 10:34:56 GMT  
		Size: 22.5 KB (22543 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3`

```console
$ docker pull spark@sha256:87e5072a66233acc33c5be87df97d9222ccf87506e3b1eb2f19ec67f3521fc7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3` - linux; amd64

```console
$ docker pull spark@sha256:7c46e98893b0bea0b156073c6322fb604a1bc2bdafb57954df954b8919615392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.8 MB (534825450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bc5cb3030aeff035eaf4c15c14035a5125f28f914d68c109f4f0b4ab462a2e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e8a38f365b1833707603c7367696d82be7bb983e4e0936836c0a51df026714`  
		Last Modified: Sat, 19 Oct 2024 03:57:37 GMT  
		Size: 94.4 MB (94363522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3` - unknown; unknown

```console
$ docker pull spark@sha256:7ae027b5af20136b0184957fcf888c8154d63aa2ff1cd7077f0a006516b06c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9106683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c982bcc231f273161c8f8dcd4cbe0375a17d1aa6b2d891363b086e17152e20a`

```dockerfile
```

-	Layers:
	-	`sha256:19a0f54f98a6122660a2328daea08f2dc7fc1c7bbc512ece992ef01f2329447b`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 9.1 MB (9095120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7c35de4255da0356bbeeb2a652ed9db3d700eab73576dc65e19743a99290a1`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f2f38e8f17b215f7da238a52981c15f63066193714a2e9c301fbaaca163c22ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524182847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653c551918ee722d3d6378deb1d11458902ff12869999eaaaea39662c571e36c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e51a6d72775f54aa3319ab3dec66092f226a8d502996e5138b39cdfbca7a8`  
		Last Modified: Sat, 19 Oct 2024 20:51:33 GMT  
		Size: 87.3 MB (87319332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3` - unknown; unknown

```console
$ docker pull spark@sha256:c4a9ba3e01e8c0a5b71d3bbe10de6ea55f3011aaf2e0a6517ecbb783b5d2fe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9110623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fb126440a97a54cdd88a3b1a89cca93f15296a1e6744d0c0580f4402d31195`

```dockerfile
```

-	Layers:
	-	`sha256:3e4eb379fb63badbc4ed56a7b84e08446b5aeb31e2450375597b92aed80d3524`  
		Last Modified: Sat, 19 Oct 2024 20:51:31 GMT  
		Size: 9.1 MB (9098944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ebb3615f1f59c1390c20a4d87210c0ae6abf0fbbed9fb54533419685b36c96`  
		Last Modified: Sat, 19 Oct 2024 20:51:30 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17`

```console
$ docker pull spark@sha256:d10996cb72671857b8f869f3deb35747d26d9ace217672cd355d31b8b51dfd14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17` - linux; amd64

```console
$ docker pull spark@sha256:17a6e46ef5244773e6a24b3287c5b3410c4ac73d66c1c97704e98867d2ebea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 MB (655660457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f956d55d1819bce2c3e036856062f44ff1d3c7d034531c10f83e7bc912150626`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b8f1cd0cbd7fb8685624dd7fa7b3cb436e6a8029bc2aa9957583684165d9a`  
		Last Modified: Sat, 19 Oct 2024 03:57:35 GMT  
		Size: 113.7 MB (113739864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:94241355b904f03bd7c0106eefe222a81866d45898bbdb94ad4578b0d91561c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9979324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb7f63984a0dc4cf67005bb454513db1a7c38f53b7afe520f2d1dbfc5b61b36`

```dockerfile
```

-	Layers:
	-	`sha256:6effb41ff2d222794841f7889cf8d189c8f53b6e7e561db1ede64b7be1263ddd`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 10.0 MB (9968012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6625829987fb97a0b2de6a8192018e365fa51ce446447ad66cae438fe1f6c54`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07e09a83d6dd5d5b8ba62953ac271a8a4b9401e97df164182b94d3e3bec146ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647883758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c069feced92260d8423f5c0fdaeeaf4da8becc09b74acf3361827167c991a21`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de733cea9df4008028a83681c30b600f13b07b9ea301fe2a403f793bcd1de46`  
		Last Modified: Sat, 19 Oct 2024 20:45:43 GMT  
		Size: 108.3 MB (108280712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:9eca174b852c37ab632025400c05f5aac2e47b417669393213945db370d05be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9973873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8394dad5755ee38b22b7fe70ea8d33b907570ee27a3a3c4f5ae6855e680a0a5d`

```dockerfile
```

-	Layers:
	-	`sha256:41b639b112327c903e5f7c89d5f694a8bfaa9791441aa112d8319e36c6cb2b04`  
		Last Modified: Sat, 19 Oct 2024 20:45:41 GMT  
		Size: 10.0 MB (9962459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa0941162aba1dbd5021b7022bd92631fd7dd82e35f1f3b00120ff14517aa18`  
		Last Modified: Sat, 19 Oct 2024 20:45:40 GMT  
		Size: 11.4 KB (11414 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17-python3`

```console
$ docker pull spark@sha256:d10996cb72671857b8f869f3deb35747d26d9ace217672cd355d31b8b51dfd14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:17a6e46ef5244773e6a24b3287c5b3410c4ac73d66c1c97704e98867d2ebea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 MB (655660457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f956d55d1819bce2c3e036856062f44ff1d3c7d034531c10f83e7bc912150626`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b8f1cd0cbd7fb8685624dd7fa7b3cb436e6a8029bc2aa9957583684165d9a`  
		Last Modified: Sat, 19 Oct 2024 03:57:35 GMT  
		Size: 113.7 MB (113739864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:94241355b904f03bd7c0106eefe222a81866d45898bbdb94ad4578b0d91561c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9979324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb7f63984a0dc4cf67005bb454513db1a7c38f53b7afe520f2d1dbfc5b61b36`

```dockerfile
```

-	Layers:
	-	`sha256:6effb41ff2d222794841f7889cf8d189c8f53b6e7e561db1ede64b7be1263ddd`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 10.0 MB (9968012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6625829987fb97a0b2de6a8192018e365fa51ce446447ad66cae438fe1f6c54`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07e09a83d6dd5d5b8ba62953ac271a8a4b9401e97df164182b94d3e3bec146ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647883758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c069feced92260d8423f5c0fdaeeaf4da8becc09b74acf3361827167c991a21`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de733cea9df4008028a83681c30b600f13b07b9ea301fe2a403f793bcd1de46`  
		Last Modified: Sat, 19 Oct 2024 20:45:43 GMT  
		Size: 108.3 MB (108280712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:9eca174b852c37ab632025400c05f5aac2e47b417669393213945db370d05be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9973873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8394dad5755ee38b22b7fe70ea8d33b907570ee27a3a3c4f5ae6855e680a0a5d`

```dockerfile
```

-	Layers:
	-	`sha256:41b639b112327c903e5f7c89d5f694a8bfaa9791441aa112d8319e36c6cb2b04`  
		Last Modified: Sat, 19 Oct 2024 20:45:41 GMT  
		Size: 10.0 MB (9962459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa0941162aba1dbd5021b7022bd92631fd7dd82e35f1f3b00120ff14517aa18`  
		Last Modified: Sat, 19 Oct 2024 20:45:40 GMT  
		Size: 11.4 KB (11414 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17-r`

```console
$ docker pull spark@sha256:271b7571f576e9b0f0ee7e8a99dbddd7ded652092a50870273516f9d0e113b85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:f5a598ffcdf9b8bd103661972309e72feee7e0b5bc72d418be00fcb26024dbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.2 MB (861230280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b5ccd5bb46e2ad7411fc7d3cf25423794bd709e46b63295488e87c8e26b2e1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770d8dbeb932ef7e9e8e134f6a890967d93ff323f04de8fc4e137a2a658e1136`  
		Last Modified: Sat, 19 Oct 2024 03:58:55 GMT  
		Size: 319.3 MB (319309687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:b5b53601d267eb634e0d6fb8364728c7b72821d27e1abdf53062642088acfddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18029173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51e6d4c5c77ca38ede3f16556be3c5f4c48325c95f8aa67f0d57ec256478e4e`

```dockerfile
```

-	Layers:
	-	`sha256:d4a4602d0730e259a2ac6c9f3613eb88521651613d60632046ebd759e16fb00a`  
		Last Modified: Sat, 19 Oct 2024 03:58:48 GMT  
		Size: 18.0 MB (18018491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a607e8212193d21b147db7193aa8a239ccb5ec31eb21ae6230c72703a76b1b1`  
		Last Modified: Sat, 19 Oct 2024 03:58:48 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f6940f39e556bb7eda223e3800aea081f9b956cd96c83ad03ae20dd138ef8181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.1 MB (842081589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72fe110c78df0f52457c620b1210a7ce1811ef3972eae4a90241156c027509`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a33d36781a18b80ae5e8b8c38c598df29e30a1bd52f434456c35897561b73`  
		Last Modified: Sat, 19 Oct 2024 20:49:06 GMT  
		Size: 302.5 MB (302478543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:2f7d60c6151ac38a85e10f0b240fbf40a8b8c41b5301ae3aef7e2a133f92d7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17994655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47374c09522b19e83545263daddeba80485011cda715a912d4c2768543a76575`

```dockerfile
```

-	Layers:
	-	`sha256:bf2d313bd29107f44cbbef52bb545df5f15f3909559a90505465461792b1e2a6`  
		Last Modified: Sat, 19 Oct 2024 20:49:00 GMT  
		Size: 18.0 MB (17983894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d19ac1fab238bbf10ed9febeb1363865ec4a0c72925bc6d982edce71a6fccdd9`  
		Last Modified: Sat, 19 Oct 2024 20:48:59 GMT  
		Size: 10.8 KB (10761 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17-scala`

```console
$ docker pull spark@sha256:31c4f1394aeeafafb5094dfb7aaf3773305685468ad21b8feeb4a83ecd13e2db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:0b7f6fc109ec5e8a808a2069a6acda7be83a0fb7bc6a0bff570f15e1111879c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541920593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683510bf0353cf3e0b30def533f193417204a0639fda94047db47b3e26701f7f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:7979a5a634afb744ad2affffdcac776c755f1256ab16b623e00589c99362cc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4616101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1820147274578ed3a4fafcac9dd9b0c2468bef98de36fad5f069c919c78a96e`

```dockerfile
```

-	Layers:
	-	`sha256:aa9971e34c9ccbfa8436850679f52c3c74aac5b4fd9d536f0f480d86055754f9`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 4.6 MB (4593235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f44263cf2b60e53493267754b72d8defffd212296a043bea17fe3b3b5c0fc2e`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 22.9 KB (22866 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:08955f77f5dc58e32e8e7ca5d9a7dd1da391e1157c19cf9567b472b652212b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539603046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0e2b6378eee41f02f2d0616e1f6a84a3d70fb813cb2b3f1deb559bd73d04b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:36f1e1914ecebcb055b747598ae9df45dfab8b60c6ebce84903314fe95b4f823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4711826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06525f713772487510ad1c3c398d3a85b3968c2b127b1adcb88c4b96a32ca19`

```dockerfile
```

-	Layers:
	-	`sha256:506d0f7637093e41e970ba3b1877786406f5ff8b52c4a0bc5610e307393d1b6d`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 4.7 MB (4688850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7e20cc6a72a031d6f2024b759efdc02f0c1c6b9203d30ffe6b934206c70758`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 23.0 KB (22976 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-python3`

```console
$ docker pull spark@sha256:87e5072a66233acc33c5be87df97d9222ccf87506e3b1eb2f19ec67f3521fc7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-python3` - linux; amd64

```console
$ docker pull spark@sha256:7c46e98893b0bea0b156073c6322fb604a1bc2bdafb57954df954b8919615392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.8 MB (534825450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bc5cb3030aeff035eaf4c15c14035a5125f28f914d68c109f4f0b4ab462a2e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e8a38f365b1833707603c7367696d82be7bb983e4e0936836c0a51df026714`  
		Last Modified: Sat, 19 Oct 2024 03:57:37 GMT  
		Size: 94.4 MB (94363522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:7ae027b5af20136b0184957fcf888c8154d63aa2ff1cd7077f0a006516b06c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9106683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c982bcc231f273161c8f8dcd4cbe0375a17d1aa6b2d891363b086e17152e20a`

```dockerfile
```

-	Layers:
	-	`sha256:19a0f54f98a6122660a2328daea08f2dc7fc1c7bbc512ece992ef01f2329447b`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 9.1 MB (9095120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7c35de4255da0356bbeeb2a652ed9db3d700eab73576dc65e19743a99290a1`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f2f38e8f17b215f7da238a52981c15f63066193714a2e9c301fbaaca163c22ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524182847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653c551918ee722d3d6378deb1d11458902ff12869999eaaaea39662c571e36c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e51a6d72775f54aa3319ab3dec66092f226a8d502996e5138b39cdfbca7a8`  
		Last Modified: Sat, 19 Oct 2024 20:51:33 GMT  
		Size: 87.3 MB (87319332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:c4a9ba3e01e8c0a5b71d3bbe10de6ea55f3011aaf2e0a6517ecbb783b5d2fe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9110623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fb126440a97a54cdd88a3b1a89cca93f15296a1e6744d0c0580f4402d31195`

```dockerfile
```

-	Layers:
	-	`sha256:3e4eb379fb63badbc4ed56a7b84e08446b5aeb31e2450375597b92aed80d3524`  
		Last Modified: Sat, 19 Oct 2024 20:51:31 GMT  
		Size: 9.1 MB (9098944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ebb3615f1f59c1390c20a4d87210c0ae6abf0fbbed9fb54533419685b36c96`  
		Last Modified: Sat, 19 Oct 2024 20:51:30 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-r`

```console
$ docker pull spark@sha256:6b806b6db4d9a44f4efaa40e6b40687da0b0337702d99e2431a5bbe7236d6428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-r` - linux; amd64

```console
$ docker pull spark@sha256:d24f88385165563cb7587699b10fff3427980371499f68fec9dcbddc0b96ac9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672755890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf338e6d8f6e8c3098be0970fe3f0d067e47cca9d8b6c259a9c1679780e819`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d82af4f5e587c52a1d7d59a7c2744ed1df96042b8e3e8571d8d72cbc42e53`  
		Last Modified: Sat, 19 Oct 2024 03:58:15 GMT  
		Size: 232.3 MB (232293962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:6fdc9103345e74f956adac4f03d9382a446e2d55cd7e5f8e8e05f67bd0c361ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db881f47a3b618af5b200b67450c288d85535a3e74aae65a1b3954ed24fe9cbd`

```dockerfile
```

-	Layers:
	-	`sha256:67375003d3c76ff7cee5afa79883fc262225bbaac5a321e6a57e2d1579dc20cf`  
		Last Modified: Sat, 19 Oct 2024 03:58:11 GMT  
		Size: 11.3 MB (11268163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d10454e5ed40b9f9484da9afa4a4aea2302ded269581c0966a833adc8e43e9`  
		Last Modified: Sat, 19 Oct 2024 03:58:11 GMT  
		Size: 11.0 KB (10952 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8e236f0f77a8dffdc275b72b3751b0262c8c092da62f83c66cfacb36fc4c6fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.4 MB (650369967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2584d6821039f02aa7d39a10296488400cce7d441c1e32fd707a4c72f3ff3606`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c15203a3b832a6bf097eaadfe5334e323b7ede17afcdc939e3058f32343a3d0`  
		Last Modified: Sat, 19 Oct 2024 20:54:27 GMT  
		Size: 213.5 MB (213506452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:5d6e376f543068def7000626d6b77fcb1200cf7d18562db4f3291beec3a24655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11263340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356d79baf2ae3102256f7272c0f3d955c12ac7fab5217ea7ee900ec80be73b3`

```dockerfile
```

-	Layers:
	-	`sha256:92bcc3f3766a7aa49648110038062196e95eedab0bd883f2dc1dec6ad6534889`  
		Last Modified: Sat, 19 Oct 2024 20:54:22 GMT  
		Size: 11.3 MB (11252296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20897221290be9049ef264a1c290ab559375434844adbc463059c01c0123a092`  
		Last Modified: Sat, 19 Oct 2024 20:54:22 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala`

```console
$ docker pull spark@sha256:b6d253f9f5d758ed2ac967d042a6c793b0e41fbdd4612e19a16f10d7f63629bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala` - linux; amd64

```console
$ docker pull spark@sha256:37369531ea1b50ca65070ed10d5be68fb307d5bf7bc5bfe5f520aaa8a40b58d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440461928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5e17d604f32589289c5b2e93e6c61d81ee591aec43353a19b906e2d57de553`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:a42e4f5ad2684c05c877142b952e9b4b8ab238cdad13d0c28cc18fddfea71453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4387356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376c0a8d363021b6b3c604741971b6766ecc6717debe8b6921762622469ce0d`

```dockerfile
```

-	Layers:
	-	`sha256:d29c0bebb95290113ff07c8e3c10cbe63e323f97089f1e0e4196f10297e94b91`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 4.4 MB (4364209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c23d3a7313e1a3c52dd7052fbb48edd238b0d33b839fa2e72867b797524d2c`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 23.1 KB (23147 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:514c6bf838f1a5f7152a85e27610ea70caf1eb403b68bc00633b57ecd372d07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436863515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac54614220459fe2fca66183fc248bd9b35fc5a3526bd8426dd91eb0187f7d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:1418b1370fe1ff4cdc95385ad9f9963585d73417403ac1a7d52472c9718fc80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4387781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b42fb8becad584e32987757ee9ae862dfdb1abe173b96a63eeb1071ff95c4b`

```dockerfile
```

-	Layers:
	-	`sha256:99e16d310b094301529958980e972eda787ee77ca3fb3298837395bce204b0ec`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 4.4 MB (4364512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc402ec52c7713eedd4489491145ddc10bceb1510f3fb4a6a63e5f8d90c9756b`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 23.3 KB (23269 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:9e179cda6e6d7520f583c27452905194fa172534758f069a695133deeae63bd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:88024b673423fbd4103cc7a99a2997164e2cb047b61a1664f42d131c8925e596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.4 MB (694373252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d52bd5c353328b6115507f13d49d10b1dcab9cf68687abc78a1ab28303e3af`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e2e90017b5fca0197513f47dbf689dca367cd9abcaa80779d223a870cc54f5`  
		Last Modified: Sat, 19 Oct 2024 03:57:02 GMT  
		Size: 253.9 MB (253911324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:478415b5d578c080dff77f6bc7c45fdb2b79a4e0ea299fb48d46ba5729969bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12404458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e485522c0aeea2c1b906b8ea27a1ded6730fb9486f46c73bba4d1cc8a5b9f6`

```dockerfile
```

-	Layers:
	-	`sha256:fd059968ef1691d6c48ad12178122c4533843a67a97c4e39e6cca7d8e7f92aee`  
		Last Modified: Sat, 19 Oct 2024 03:56:59 GMT  
		Size: 12.4 MB (12393915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd7b503dc5706bc700747ee9b3601c6a6b7c3e68a6322295b47bdf9b9146187`  
		Last Modified: Sat, 19 Oct 2024 03:56:58 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:90387ec26244e83c35875d40722bd0734ef8424dfa59249242137b8e1460eac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (672004031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570e5a1bd1125781df234037feaf7fabb9f57ffd6bcddf95615281f58c29fbd9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb1d84737f8feb29c7eb4266b2b9bf4f6eaa3f16eb217eb1d811aa0ce84135`  
		Last Modified: Sat, 19 Oct 2024 20:26:07 GMT  
		Size: 235.1 MB (235140516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e928964cc63117acc145e229441c74cc77b00b413b1f19cd373d92fb68c895e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12388702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6487cb8de10d9ada7f4046fa1449eb8022d9e28febb58c4ae1f70e30f3e263`

```dockerfile
```

-	Layers:
	-	`sha256:da14d31a06eca208f2d5711de5c9a7f5ec8d0d4b1523b6cceb7a84c4a25c734a`  
		Last Modified: Sat, 19 Oct 2024 20:26:01 GMT  
		Size: 12.4 MB (12378091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02fe4f7239aef3d84e701b1865cff31d3fd188fac9d140a0f046da4a635f831`  
		Last Modified: Sat, 19 Oct 2024 20:26:00 GMT  
		Size: 10.6 KB (10611 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:87e5072a66233acc33c5be87df97d9222ccf87506e3b1eb2f19ec67f3521fc7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:7c46e98893b0bea0b156073c6322fb604a1bc2bdafb57954df954b8919615392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.8 MB (534825450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bc5cb3030aeff035eaf4c15c14035a5125f28f914d68c109f4f0b4ab462a2e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e8a38f365b1833707603c7367696d82be7bb983e4e0936836c0a51df026714`  
		Last Modified: Sat, 19 Oct 2024 03:57:37 GMT  
		Size: 94.4 MB (94363522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:7ae027b5af20136b0184957fcf888c8154d63aa2ff1cd7077f0a006516b06c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9106683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c982bcc231f273161c8f8dcd4cbe0375a17d1aa6b2d891363b086e17152e20a`

```dockerfile
```

-	Layers:
	-	`sha256:19a0f54f98a6122660a2328daea08f2dc7fc1c7bbc512ece992ef01f2329447b`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 9.1 MB (9095120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7c35de4255da0356bbeeb2a652ed9db3d700eab73576dc65e19743a99290a1`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f2f38e8f17b215f7da238a52981c15f63066193714a2e9c301fbaaca163c22ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524182847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653c551918ee722d3d6378deb1d11458902ff12869999eaaaea39662c571e36c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e51a6d72775f54aa3319ab3dec66092f226a8d502996e5138b39cdfbca7a8`  
		Last Modified: Sat, 19 Oct 2024 20:51:33 GMT  
		Size: 87.3 MB (87319332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c4a9ba3e01e8c0a5b71d3bbe10de6ea55f3011aaf2e0a6517ecbb783b5d2fe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9110623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fb126440a97a54cdd88a3b1a89cca93f15296a1e6744d0c0580f4402d31195`

```dockerfile
```

-	Layers:
	-	`sha256:3e4eb379fb63badbc4ed56a7b84e08446b5aeb31e2450375597b92aed80d3524`  
		Last Modified: Sat, 19 Oct 2024 20:51:31 GMT  
		Size: 9.1 MB (9098944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ebb3615f1f59c1390c20a4d87210c0ae6abf0fbbed9fb54533419685b36c96`  
		Last Modified: Sat, 19 Oct 2024 20:51:30 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:6b806b6db4d9a44f4efaa40e6b40687da0b0337702d99e2431a5bbe7236d6428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:d24f88385165563cb7587699b10fff3427980371499f68fec9dcbddc0b96ac9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672755890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf338e6d8f6e8c3098be0970fe3f0d067e47cca9d8b6c259a9c1679780e819`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d82af4f5e587c52a1d7d59a7c2744ed1df96042b8e3e8571d8d72cbc42e53`  
		Last Modified: Sat, 19 Oct 2024 03:58:15 GMT  
		Size: 232.3 MB (232293962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6fdc9103345e74f956adac4f03d9382a446e2d55cd7e5f8e8e05f67bd0c361ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db881f47a3b618af5b200b67450c288d85535a3e74aae65a1b3954ed24fe9cbd`

```dockerfile
```

-	Layers:
	-	`sha256:67375003d3c76ff7cee5afa79883fc262225bbaac5a321e6a57e2d1579dc20cf`  
		Last Modified: Sat, 19 Oct 2024 03:58:11 GMT  
		Size: 11.3 MB (11268163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d10454e5ed40b9f9484da9afa4a4aea2302ded269581c0966a833adc8e43e9`  
		Last Modified: Sat, 19 Oct 2024 03:58:11 GMT  
		Size: 11.0 KB (10952 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8e236f0f77a8dffdc275b72b3751b0262c8c092da62f83c66cfacb36fc4c6fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.4 MB (650369967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2584d6821039f02aa7d39a10296488400cce7d441c1e32fd707a4c72f3ff3606`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c15203a3b832a6bf097eaadfe5334e323b7ede17afcdc939e3058f32343a3d0`  
		Last Modified: Sat, 19 Oct 2024 20:54:27 GMT  
		Size: 213.5 MB (213506452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5d6e376f543068def7000626d6b77fcb1200cf7d18562db4f3291beec3a24655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11263340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356d79baf2ae3102256f7272c0f3d955c12ac7fab5217ea7ee900ec80be73b3`

```dockerfile
```

-	Layers:
	-	`sha256:92bcc3f3766a7aa49648110038062196e95eedab0bd883f2dc1dec6ad6534889`  
		Last Modified: Sat, 19 Oct 2024 20:54:22 GMT  
		Size: 11.3 MB (11252296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20897221290be9049ef264a1c290ab559375434844adbc463059c01c0123a092`  
		Last Modified: Sat, 19 Oct 2024 20:54:22 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:b6d253f9f5d758ed2ac967d042a6c793b0e41fbdd4612e19a16f10d7f63629bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:37369531ea1b50ca65070ed10d5be68fb307d5bf7bc5bfe5f520aaa8a40b58d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440461928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5e17d604f32589289c5b2e93e6c61d81ee591aec43353a19b906e2d57de553`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a42e4f5ad2684c05c877142b952e9b4b8ab238cdad13d0c28cc18fddfea71453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4387356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376c0a8d363021b6b3c604741971b6766ecc6717debe8b6921762622469ce0d`

```dockerfile
```

-	Layers:
	-	`sha256:d29c0bebb95290113ff07c8e3c10cbe63e323f97089f1e0e4196f10297e94b91`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 4.4 MB (4364209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c23d3a7313e1a3c52dd7052fbb48edd238b0d33b839fa2e72867b797524d2c`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 23.1 KB (23147 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:514c6bf838f1a5f7152a85e27610ea70caf1eb403b68bc00633b57ecd372d07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436863515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac54614220459fe2fca66183fc248bd9b35fc5a3526bd8426dd91eb0187f7d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:1418b1370fe1ff4cdc95385ad9f9963585d73417403ac1a7d52472c9718fc80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4387781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b42fb8becad584e32987757ee9ae862dfdb1abe173b96a63eeb1071ff95c4b`

```dockerfile
```

-	Layers:
	-	`sha256:99e16d310b094301529958980e972eda787ee77ca3fb3298837395bce204b0ec`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 4.4 MB (4364512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc402ec52c7713eedd4489491145ddc10bceb1510f3fb4a6a63e5f8d90c9756b`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 23.3 KB (23269 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:f38031830e0a8eb0588be857fc093349b2bf2f18148113d567220dfa78e3b58d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:4b7c4511449c5b88d56ab3361b726a34c8b6145081ce30023a11471b9dc93d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.9 MB (875915245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6954a84e4fb6e245f51f7ec05d614f719e9ee8a37fbef62d888e423687e6b8e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23311193dd293112f560aba41bbd848b024e13d63c1623348be2c0199f77c37`  
		Last Modified: Sat, 19 Oct 2024 04:06:41 GMT  
		Size: 334.0 MB (333994652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:9a340b4b66b438fd4a50b6f8afd7524ff0f425db6655eda648ca52066f20aa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19042767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50edf980d45d55633464acc8cba28ce8775d1c844925f44ce8f4f7ddba623b38`

```dockerfile
```

-	Layers:
	-	`sha256:72c01662b17aa582fb5bdbebfaef7f78ba261dca96cc1b75289dba0f1d74f348`  
		Last Modified: Sat, 19 Oct 2024 04:06:37 GMT  
		Size: 19.0 MB (19032221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28836d5b7629c2c8918a62f6a10becb17a16f7e38d6a6cd73ee70a42cf006201`  
		Last Modified: Sat, 19 Oct 2024 04:06:37 GMT  
		Size: 10.5 KB (10546 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f9661ae470c803727e76c68eaadf9616ee5095754ad406976673923e28766d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 MB (856646301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555eb1f3ab52c8b2e5883f835df8a96c892304b90ee5491f04790ff538f2008a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f4780a16937aaed79d9e040dfa54fca6fabe2f819d195f55197fa18cbfefa6`  
		Last Modified: Sat, 19 Oct 2024 20:19:31 GMT  
		Size: 317.0 MB (317043255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8a68bb08b44b7be72f2ce624d354d3366fe6c1733a39727b8375daffef0b32f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19008250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570a298602e08111987540981845e5aa8f25edc71161c0c6e9d44148e2d961b6`

```dockerfile
```

-	Layers:
	-	`sha256:da02cd6ab1d2600845b45972e5a4288e6202da993fa6bd7e1b19b1d9e65b2021`  
		Last Modified: Sat, 19 Oct 2024 20:19:20 GMT  
		Size: 19.0 MB (18997636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995bf1b35e7d6454539174824648d3ee5200b2a515d77247b26a849635024a9c`  
		Last Modified: Sat, 19 Oct 2024 20:19:19 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:d10996cb72671857b8f869f3deb35747d26d9ace217672cd355d31b8b51dfd14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:17a6e46ef5244773e6a24b3287c5b3410c4ac73d66c1c97704e98867d2ebea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 MB (655660457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f956d55d1819bce2c3e036856062f44ff1d3c7d034531c10f83e7bc912150626`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b8f1cd0cbd7fb8685624dd7fa7b3cb436e6a8029bc2aa9957583684165d9a`  
		Last Modified: Sat, 19 Oct 2024 03:57:35 GMT  
		Size: 113.7 MB (113739864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:94241355b904f03bd7c0106eefe222a81866d45898bbdb94ad4578b0d91561c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9979324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb7f63984a0dc4cf67005bb454513db1a7c38f53b7afe520f2d1dbfc5b61b36`

```dockerfile
```

-	Layers:
	-	`sha256:6effb41ff2d222794841f7889cf8d189c8f53b6e7e561db1ede64b7be1263ddd`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 10.0 MB (9968012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6625829987fb97a0b2de6a8192018e365fa51ce446447ad66cae438fe1f6c54`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07e09a83d6dd5d5b8ba62953ac271a8a4b9401e97df164182b94d3e3bec146ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647883758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c069feced92260d8423f5c0fdaeeaf4da8becc09b74acf3361827167c991a21`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de733cea9df4008028a83681c30b600f13b07b9ea301fe2a403f793bcd1de46`  
		Last Modified: Sat, 19 Oct 2024 20:45:43 GMT  
		Size: 108.3 MB (108280712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:9eca174b852c37ab632025400c05f5aac2e47b417669393213945db370d05be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9973873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8394dad5755ee38b22b7fe70ea8d33b907570ee27a3a3c4f5ae6855e680a0a5d`

```dockerfile
```

-	Layers:
	-	`sha256:41b639b112327c903e5f7c89d5f694a8bfaa9791441aa112d8319e36c6cb2b04`  
		Last Modified: Sat, 19 Oct 2024 20:45:41 GMT  
		Size: 10.0 MB (9962459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa0941162aba1dbd5021b7022bd92631fd7dd82e35f1f3b00120ff14517aa18`  
		Last Modified: Sat, 19 Oct 2024 20:45:40 GMT  
		Size: 11.4 KB (11414 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:271b7571f576e9b0f0ee7e8a99dbddd7ded652092a50870273516f9d0e113b85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:f5a598ffcdf9b8bd103661972309e72feee7e0b5bc72d418be00fcb26024dbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.2 MB (861230280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b5ccd5bb46e2ad7411fc7d3cf25423794bd709e46b63295488e87c8e26b2e1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770d8dbeb932ef7e9e8e134f6a890967d93ff323f04de8fc4e137a2a658e1136`  
		Last Modified: Sat, 19 Oct 2024 03:58:55 GMT  
		Size: 319.3 MB (319309687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b5b53601d267eb634e0d6fb8364728c7b72821d27e1abdf53062642088acfddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18029173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51e6d4c5c77ca38ede3f16556be3c5f4c48325c95f8aa67f0d57ec256478e4e`

```dockerfile
```

-	Layers:
	-	`sha256:d4a4602d0730e259a2ac6c9f3613eb88521651613d60632046ebd759e16fb00a`  
		Last Modified: Sat, 19 Oct 2024 03:58:48 GMT  
		Size: 18.0 MB (18018491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a607e8212193d21b147db7193aa8a239ccb5ec31eb21ae6230c72703a76b1b1`  
		Last Modified: Sat, 19 Oct 2024 03:58:48 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f6940f39e556bb7eda223e3800aea081f9b956cd96c83ad03ae20dd138ef8181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.1 MB (842081589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72fe110c78df0f52457c620b1210a7ce1811ef3972eae4a90241156c027509`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a33d36781a18b80ae5e8b8c38c598df29e30a1bd52f434456c35897561b73`  
		Last Modified: Sat, 19 Oct 2024 20:49:06 GMT  
		Size: 302.5 MB (302478543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2f7d60c6151ac38a85e10f0b240fbf40a8b8c41b5301ae3aef7e2a133f92d7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17994655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47374c09522b19e83545263daddeba80485011cda715a912d4c2768543a76575`

```dockerfile
```

-	Layers:
	-	`sha256:bf2d313bd29107f44cbbef52bb545df5f15f3909559a90505465461792b1e2a6`  
		Last Modified: Sat, 19 Oct 2024 20:49:00 GMT  
		Size: 18.0 MB (17983894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d19ac1fab238bbf10ed9febeb1363865ec4a0c72925bc6d982edce71a6fccdd9`  
		Last Modified: Sat, 19 Oct 2024 20:48:59 GMT  
		Size: 10.8 KB (10761 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:31c4f1394aeeafafb5094dfb7aaf3773305685468ad21b8feeb4a83ecd13e2db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:0b7f6fc109ec5e8a808a2069a6acda7be83a0fb7bc6a0bff570f15e1111879c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541920593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683510bf0353cf3e0b30def533f193417204a0639fda94047db47b3e26701f7f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:7979a5a634afb744ad2affffdcac776c755f1256ab16b623e00589c99362cc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4616101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1820147274578ed3a4fafcac9dd9b0c2468bef98de36fad5f069c919c78a96e`

```dockerfile
```

-	Layers:
	-	`sha256:aa9971e34c9ccbfa8436850679f52c3c74aac5b4fd9d536f0f480d86055754f9`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 4.6 MB (4593235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f44263cf2b60e53493267754b72d8defffd212296a043bea17fe3b3b5c0fc2e`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 22.9 KB (22866 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:08955f77f5dc58e32e8e7ca5d9a7dd1da391e1157c19cf9567b472b652212b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539603046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0e2b6378eee41f02f2d0616e1f6a84a3d70fb813cb2b3f1deb559bd73d04b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:36f1e1914ecebcb055b747598ae9df45dfab8b60c6ebce84903314fe95b4f823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4711826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06525f713772487510ad1c3c398d3a85b3968c2b127b1adcb88c4b96a32ca19`

```dockerfile
```

-	Layers:
	-	`sha256:506d0f7637093e41e970ba3b1877786406f5ff8b52c4a0bc5610e307393d1b6d`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 4.7 MB (4688850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7e20cc6a72a031d6f2024b759efdc02f0c1c6b9203d30ffe6b934206c70758`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 23.0 KB (22976 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2`

```console
$ docker pull spark@sha256:52b391de693cb5e80e7de84ea27b25737c6fb004a0710a5147d8cb91c4794ea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2` - linux; amd64

```console
$ docker pull spark@sha256:1a30e3efd2aeec024b3788ac35f5d482a60f1ec9e625a88b1f03bbf4c4b092d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.8 MB (774824098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc4c23ec7077bc95f2907d6a4ea1fe9c8b994c985ab35fd8c70ef7abdcb716a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f6366eecac5038cc46d463f38273eb242aa8dabb1ae4f2de2372c8144b0dc3`  
		Last Modified: Sat, 19 Oct 2024 03:56:49 GMT  
		Size: 113.7 MB (113739991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2` - unknown; unknown

```console
$ docker pull spark@sha256:5740e66cf000c28c07c81e998d5505ee0c7dc2c801f248d6c102ce7c6f9b3724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10120584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0cb824ac7aef1084cf788f11ad2b402bfb3d0a27a80903f5c09e6ca31697b`

```dockerfile
```

-	Layers:
	-	`sha256:4a1584f030c6f008b49e59b70705a407a866f47132f7283fca431e5f1fac5157`  
		Last Modified: Sat, 19 Oct 2024 03:56:48 GMT  
		Size: 10.1 MB (10109483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5620ce8906725295fdbda4ad6d80a33bacf48e516ac901190b55e0b74fe79ae`  
		Last Modified: Sat, 19 Oct 2024 03:56:47 GMT  
		Size: 11.1 KB (11101 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9f10709da1dae6901a1b117b66591f596483739a950170432aa56d76f98e1fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **767.0 MB (767048025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0080c09d01598d6cf7729d3b5a3acaa6c079fd3e37c4d160b42c3a59ec3d0f91`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c460b6cc813335a293de06cbf1af1684e6c0869b5e8e38a578b596ccf86f242`  
		Last Modified: Sat, 19 Oct 2024 20:39:49 GMT  
		Size: 108.3 MB (108281387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2` - unknown; unknown

```console
$ docker pull spark@sha256:209ce8ee9fd1a23c2cfcaf621cafece15fe7289dad3bac77c4493cf7fb3b950b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10115111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f024458071ec6fd401220adda2afaa36e7d51b603b26b5636d1de958d35d2d5`

```dockerfile
```

-	Layers:
	-	`sha256:e1153b5d0bd1dbabc290ff37e4256b77355a5d8cb5b472cac148a7955612d82e`  
		Last Modified: Sat, 19 Oct 2024 20:39:47 GMT  
		Size: 10.1 MB (10103918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98075dfb713e33d02cd76ee8c8bf93effbbf12c3e2e57ca21075dcf741cd0f2a`  
		Last Modified: Sat, 19 Oct 2024 20:39:46 GMT  
		Size: 11.2 KB (11193 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21`

```console
$ docker pull spark@sha256:ea1780d3cb461337719b71e5bb7f327a7d3988b7b6aa0213bcda381b955d27ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21` - linux; amd64

```console
$ docker pull spark@sha256:232a2f0dcfd5af63a41a2e687f936cf5376fd202d8641acb0ad11323b4574a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **788.2 MB (788234220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26941152e9f92ffc847d06593f2ef1f2760dfd0bfdb8106678015464027f0c9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb568b1f16cfc59ac36c34713fdadb00b7be69fa8589dc1650c0cf124eec667`  
		Last Modified: Sat, 19 Oct 2024 03:56:39 GMT  
		Size: 113.7 MB (113740105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21` - unknown; unknown

```console
$ docker pull spark@sha256:68c752b188fa88e5a3267d90e66482acc31771f9a32da05bcd9bd943f6a66599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10124379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dfd1d98280f1b8c4cf1385ddb7e5f735b97cb7d2aed167e5ee6f831c42a8b5`

```dockerfile
```

-	Layers:
	-	`sha256:3b8257292aed961082977a06e8f465b0ca415811c1cea1a696eba631ff37717c`  
		Last Modified: Sat, 19 Oct 2024 03:56:38 GMT  
		Size: 10.1 MB (10113252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e75b1964d25843a363d8540b05c6c5eea599af4acc51d5d5310b59604d2a86`  
		Last Modified: Sat, 19 Oct 2024 03:56:37 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:decb03be71d6ff1a16ff1eb44d01c09edbbdfd2a3d0f7e215316865b5a5ce107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.8 MB (779838550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35c0cc1de09cda55a2ba01d372fe0214272e3abece54e28fe0a367d95c65c33`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed0abe4c9197505695967e1bd0774e45a6cf8ecf17a6e72080b3b06db24624`  
		Last Modified: Sat, 19 Oct 2024 20:32:55 GMT  
		Size: 108.3 MB (108280923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21` - unknown; unknown

```console
$ docker pull spark@sha256:4de2f30a07ef5b4811728d681b0e07dc2d6dd52f9267468a8e8780867f89cef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf79b9da0aaaebc1209aaff44f4c1c17b6bf18013c743676760107e21e9165dd`

```dockerfile
```

-	Layers:
	-	`sha256:86f6fe782b55b0f236f0ffe447e2c01e72604f1357ba2b6d8f030fea1efcedb8`  
		Last Modified: Sat, 19 Oct 2024 20:32:53 GMT  
		Size: 10.1 MB (10107687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88707dd2a9b21a19e27d32a5cef563df5707524c007821173905eb568b5aa22a`  
		Last Modified: Sat, 19 Oct 2024 20:32:52 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-python3`

```console
$ docker pull spark@sha256:ea1780d3cb461337719b71e5bb7f327a7d3988b7b6aa0213bcda381b955d27ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-python3` - linux; amd64

```console
$ docker pull spark@sha256:232a2f0dcfd5af63a41a2e687f936cf5376fd202d8641acb0ad11323b4574a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **788.2 MB (788234220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26941152e9f92ffc847d06593f2ef1f2760dfd0bfdb8106678015464027f0c9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb568b1f16cfc59ac36c34713fdadb00b7be69fa8589dc1650c0cf124eec667`  
		Last Modified: Sat, 19 Oct 2024 03:56:39 GMT  
		Size: 113.7 MB (113740105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:68c752b188fa88e5a3267d90e66482acc31771f9a32da05bcd9bd943f6a66599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10124379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dfd1d98280f1b8c4cf1385ddb7e5f735b97cb7d2aed167e5ee6f831c42a8b5`

```dockerfile
```

-	Layers:
	-	`sha256:3b8257292aed961082977a06e8f465b0ca415811c1cea1a696eba631ff37717c`  
		Last Modified: Sat, 19 Oct 2024 03:56:38 GMT  
		Size: 10.1 MB (10113252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e75b1964d25843a363d8540b05c6c5eea599af4acc51d5d5310b59604d2a86`  
		Last Modified: Sat, 19 Oct 2024 03:56:37 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:decb03be71d6ff1a16ff1eb44d01c09edbbdfd2a3d0f7e215316865b5a5ce107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.8 MB (779838550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35c0cc1de09cda55a2ba01d372fe0214272e3abece54e28fe0a367d95c65c33`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed0abe4c9197505695967e1bd0774e45a6cf8ecf17a6e72080b3b06db24624`  
		Last Modified: Sat, 19 Oct 2024 20:32:55 GMT  
		Size: 108.3 MB (108280923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:4de2f30a07ef5b4811728d681b0e07dc2d6dd52f9267468a8e8780867f89cef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf79b9da0aaaebc1209aaff44f4c1c17b6bf18013c743676760107e21e9165dd`

```dockerfile
```

-	Layers:
	-	`sha256:86f6fe782b55b0f236f0ffe447e2c01e72604f1357ba2b6d8f030fea1efcedb8`  
		Last Modified: Sat, 19 Oct 2024 20:32:53 GMT  
		Size: 10.1 MB (10107687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88707dd2a9b21a19e27d32a5cef563df5707524c007821173905eb568b5aa22a`  
		Last Modified: Sat, 19 Oct 2024 20:32:52 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-r`

```console
$ docker pull spark@sha256:7f515f6ff01abb66c58d54f508903cba7647b73b107c1cd6717cb646814b81f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-r` - linux; amd64

```console
$ docker pull spark@sha256:846443e5bf999785c32ceb39a12986ae183836d1eea084bf52c583c88681e34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 MB (993804052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9cb59e090c2b931b4e99aa3fe218fdfc5b315f1822cd593a6d948e1480cc9a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60074dc72be9d1c6c0f8fb660bf6ea34f853e31479f8c70c28af15c6105cc9a`  
		Last Modified: Sat, 19 Oct 2024 03:57:22 GMT  
		Size: 319.3 MB (319309937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:0896eeda3f9d44cf1079e7f7d03baa12bb1fddcd45cb5ab7c490894ecae760ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18174817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf2d107be3bbfcedfd057052dd00c42ee4005616c7d226ab14f88ac6f0d658`

```dockerfile
```

-	Layers:
	-	`sha256:608f682bf8b8c1b863b5a009d26bb6935f5d7be92a925342a2a0e0401ff2651f`  
		Last Modified: Sat, 19 Oct 2024 03:57:18 GMT  
		Size: 18.2 MB (18164025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546575844471803c1b5fb87405c84a67f8a78cd62459f19bc9c880f62dd77735`  
		Last Modified: Sat, 19 Oct 2024 03:57:17 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8473b5d99a7e7bcbe3a8585d3fac4d87f7c38f1c531f3c0bf257e48bc8b2abe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.0 MB (974035649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c25493059b4356b8425392f1e88b70e4228c3487bb3add68fda39cf7e0b819`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b00eba9b8684e5fd428eaf14d31ed635d00f5e78314545b7ce1964b9ede6af`  
		Last Modified: Sat, 19 Oct 2024 20:37:09 GMT  
		Size: 302.5 MB (302478022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:24b6e20517e4e4a7b4385b9e0402a1435cef73b838d694908bf34edbe3f8fa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18140300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c040820cf2fa6d9b84ce57dd159c7d95760003ef92f7e31bbe8b1e5fe8ca30b7`

```dockerfile
```

-	Layers:
	-	`sha256:e03d8e9b806aded4789304cdd53c77df3af37cb6cc1bdad2758bb5186731fa96`  
		Last Modified: Sat, 19 Oct 2024 20:37:02 GMT  
		Size: 18.1 MB (18129428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f973f9348d5efdcbbf0e3d1a6eaabaf58715a5ab2e4a865146eb7f3c64e9ea5`  
		Last Modified: Sat, 19 Oct 2024 20:37:02 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-scala`

```console
$ docker pull spark@sha256:a0eb35459d5169fb25f376d7f7526dc39acbbdded9d855d9b5fd98e24448ec56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-scala` - linux; amd64

```console
$ docker pull spark@sha256:3b2cf351ea3c834a1030b220315c2020523ac4de46f18c41caf28d612eb80dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.5 MB (674494115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e2df853051d2432170aabb094d613d2c1004971c49003ad2c632c8dd742484`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:f8e3c62d6b748ecda7fa3ca637af87310e4e4d88e2089bd4e7a39518d77f5d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4761779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2797e71dc55e13ee3bb81f26a22141e8d5f51c4bd3b6dc0f508aa86ea1d40722`

```dockerfile
```

-	Layers:
	-	`sha256:a6e0f0d7b4a13927b9c6db21202acf477cb4f9552a697337eb9f6136978bcd32`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 4.7 MB (4738769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a225ba703472461350cb8cec82923c3dea69b0b0283927f69d337b558948157`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 23.0 KB (23010 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b18c67d473a558a72f910cd3b6b1297254dbef0c87a3695416a601f4fb3d9f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 MB (671557627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e395971532bb0218d483f3d03ec10bd403c9b42ed93d54850c7f6feff6e9d5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:6cd8082982db7db48d5ed6bcc5cbc0213d0a7484613a6d6960a7d05534a57761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4857504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae1eee6b1d09617c6530d5b86255a438fbfc6b2178982d0dafee33c3131437e`

```dockerfile
```

-	Layers:
	-	`sha256:a57ec99c46f52afcf2fe407678d9606b249248e166dabf48de18f3458b078f90`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 4.8 MB (4834384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ab582e581f3d654585d04da83778c769d6db2bd2241d293acd64fcec0d017`  
		Last Modified: Sat, 19 Oct 2024 10:21:42 GMT  
		Size: 23.1 KB (23120 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-python3`

```console
$ docker pull spark@sha256:52b391de693cb5e80e7de84ea27b25737c6fb004a0710a5147d8cb91c4794ea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-python3` - linux; amd64

```console
$ docker pull spark@sha256:1a30e3efd2aeec024b3788ac35f5d482a60f1ec9e625a88b1f03bbf4c4b092d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.8 MB (774824098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc4c23ec7077bc95f2907d6a4ea1fe9c8b994c985ab35fd8c70ef7abdcb716a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f6366eecac5038cc46d463f38273eb242aa8dabb1ae4f2de2372c8144b0dc3`  
		Last Modified: Sat, 19 Oct 2024 03:56:49 GMT  
		Size: 113.7 MB (113739991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:5740e66cf000c28c07c81e998d5505ee0c7dc2c801f248d6c102ce7c6f9b3724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10120584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0cb824ac7aef1084cf788f11ad2b402bfb3d0a27a80903f5c09e6ca31697b`

```dockerfile
```

-	Layers:
	-	`sha256:4a1584f030c6f008b49e59b70705a407a866f47132f7283fca431e5f1fac5157`  
		Last Modified: Sat, 19 Oct 2024 03:56:48 GMT  
		Size: 10.1 MB (10109483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5620ce8906725295fdbda4ad6d80a33bacf48e516ac901190b55e0b74fe79ae`  
		Last Modified: Sat, 19 Oct 2024 03:56:47 GMT  
		Size: 11.1 KB (11101 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9f10709da1dae6901a1b117b66591f596483739a950170432aa56d76f98e1fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **767.0 MB (767048025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0080c09d01598d6cf7729d3b5a3acaa6c079fd3e37c4d160b42c3a59ec3d0f91`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c460b6cc813335a293de06cbf1af1684e6c0869b5e8e38a578b596ccf86f242`  
		Last Modified: Sat, 19 Oct 2024 20:39:49 GMT  
		Size: 108.3 MB (108281387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:209ce8ee9fd1a23c2cfcaf621cafece15fe7289dad3bac77c4493cf7fb3b950b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10115111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f024458071ec6fd401220adda2afaa36e7d51b603b26b5636d1de958d35d2d5`

```dockerfile
```

-	Layers:
	-	`sha256:e1153b5d0bd1dbabc290ff37e4256b77355a5d8cb5b472cac148a7955612d82e`  
		Last Modified: Sat, 19 Oct 2024 20:39:47 GMT  
		Size: 10.1 MB (10103918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98075dfb713e33d02cd76ee8c8bf93effbbf12c3e2e57ca21075dcf741cd0f2a`  
		Last Modified: Sat, 19 Oct 2024 20:39:46 GMT  
		Size: 11.2 KB (11193 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-r`

```console
$ docker pull spark@sha256:69fda212e1b079ced36ed84baeef0cb47c18485ba9627a80119b2b96033f1524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-r` - linux; amd64

```console
$ docker pull spark@sha256:bc366a36cc055612b85507934ab4cd1878af42e32dc84a88877298a5cab50e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.4 MB (980394455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e115dfd7ec28e8b5303db1321a7de5b51d801190b48ca52a0cdb83e1165dceb`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fa3b327f0b26d368aff6b633627233ce79ac5be96273786c0eeb5de8d7117e`  
		Last Modified: Sat, 19 Oct 2024 03:59:00 GMT  
		Size: 319.3 MB (319310348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-r` - unknown; unknown

```console
$ docker pull spark@sha256:96710a4b3dfb4531ee89ea63182be82d530ee198c1985fb77fd454b67d253ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18171049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dbc120de2790ba810694143c03d76075e71d2c2a3b77c7f596f2c4271deb21`

```dockerfile
```

-	Layers:
	-	`sha256:d63dd1552f4e3a4b6ded1dee0b9122890c6c20c355115c1fb70b3d810491b277`  
		Last Modified: Sat, 19 Oct 2024 03:58:55 GMT  
		Size: 18.2 MB (18160270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0a2faad6eba76d5e1a71c2f1ba92e56aaa291289e3e1ffc876471275f4a062`  
		Last Modified: Sat, 19 Oct 2024 03:58:54 GMT  
		Size: 10.8 KB (10779 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2779b5935f42d79e1b31bc885f338135dcf018ac4b9b03436c021b912e778902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.2 MB (961244883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f4e38a6ebe31c9f5a9028049ac9b9a0694751805e8a0cccf6d729db1b9e98`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329d1f817b82d41dcd6fd1f6b2ab26d46e7fb95fd0eab5bcc75b188631f907a4`  
		Last Modified: Sat, 19 Oct 2024 20:43:22 GMT  
		Size: 302.5 MB (302478245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-r` - unknown; unknown

```console
$ docker pull spark@sha256:836272be062ba3a9b4f395399b4ef642c90ec847dd0f18f3a213d00232250924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18136532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40dbe708955b9e71f1afc16bdc658a74dce453790ca20cf86ab5e9e5838195a`

```dockerfile
```

-	Layers:
	-	`sha256:e8066279d34ddff9d92057123a7fd3643031b747433f809280a38684898396ef`  
		Last Modified: Sat, 19 Oct 2024 20:43:15 GMT  
		Size: 18.1 MB (18125673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247bea43656e8a6dbdecfe3d997b520a2b002db41630e64c39b7e26f62f2980b`  
		Last Modified: Sat, 19 Oct 2024 20:43:14 GMT  
		Size: 10.9 KB (10859 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala`

```console
$ docker pull spark@sha256:01a940f8dd73f83bfa47b9d39e1fc564fccecf985ecc53651795aba8a1b7d2fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala` - linux; amd64

```console
$ docker pull spark@sha256:d967bdb37dfc18d69204620ac2565fb9cfc175790a44f0428bad89a93012caf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.1 MB (661084107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88a124ccccadf2777ffecec69386996d7cf8f1cde1c369c26ae495ea7aa9ccc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:57b625270f8a1a2ebb2d43c44cc969bcd58afafab90d90e88b8cde42fde3e7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4758013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42111e916a7469e0eade31797112ee73fb47596f5767f3a0bba38d8a05b91be5`

```dockerfile
```

-	Layers:
	-	`sha256:e52e7b06282b06ecad0eda765a8bef3284ee8401818eafcc63310ca34ed0f8aa`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 4.7 MB (4735014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:228dfec982d761925ee4be88a61a12db6930d51f181e86dc04d3553934d10bc4`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 23.0 KB (22999 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fde7fa85c59d80333b596e114ced4e194c95f64d2d9d3c6abce13e7c7364af29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.8 MB (658766638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07209c44a2d88ce3287809da9d8be96ab33a89387d428630864b147c0b04722`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:d21e82612acc5335a9e4e7d84cf853a2db774275e5a72ce1dbdd74f21e1b8d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4853738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245f50f9f1bf8475df66655026d0ab20533875c37b58963c4a2bf9a22b7c420`

```dockerfile
```

-	Layers:
	-	`sha256:9f619f340435ee8d50bfbb986053a779a41d00ee4cb6a97351116ab489c4d2fa`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 4.8 MB (4830629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d2069186133e49618ef40e2cee7dd2335ab0db3fd15644f14169daa6103b97b`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:a157692f6014d73b77d3701730ad9109aa7e0725ab598fa7ed983673e1b8a881
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:bbccf166e2e4241255299091f0794ff37666c9819a8bcf808c0a2461a3f1fa24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 MB (995078720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3369368b7c09d119c936b1a74bef44abacaf8740c57f50d83ab8c6882e6a877b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c00803a3fc11279b28af711f6ddd2d271d360e8ecc9f8d8d6069739c0d00231`  
		Last Modified: Sat, 19 Oct 2024 03:57:50 GMT  
		Size: 334.0 MB (333994613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:211e71252e8f9851e19d255d49b36d7073ac03640e30c54fefb2e8deed6247c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19184634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0b3039460369b5c5d81337694d9bc7d47deb9cb8f5bca62cab4b232f63b4ab`

```dockerfile
```

-	Layers:
	-	`sha256:7f8d98576392eb8859c11c57b0739c68ee53157dc083c31f581c6be585d4f454`  
		Last Modified: Sat, 19 Oct 2024 03:57:46 GMT  
		Size: 19.2 MB (19173996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9300e982c19286a6b910339cef517f7d330caee129820163c6225e231b2d6d`  
		Last Modified: Sat, 19 Oct 2024 03:57:46 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4eea5e12d379bdfe1f319bb2b440fa463855dd46c66d460114217b9fd604535a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.8 MB (975810276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a11a172032d050b6d4d5bf27222648370ceb507e6bf7174c66ab5fc8bc1eb9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6d8e61bdb5489cc0de17c41d6c352068cac14f6cbf69c4b60a6327f8f822f7`  
		Last Modified: Sat, 19 Oct 2024 20:15:49 GMT  
		Size: 317.0 MB (317043638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a15371447b4fd61b42cc42b8f6fc903fc91b0305a0e302e21e2163792221a8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19150118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e54ecc9514b149008f3029fdbef0a1f820d78e178fba4600e8be8eb9f3c906`

```dockerfile
```

-	Layers:
	-	`sha256:ee58c7a654ade9832980e90dc5855f77f6b7552e174e403c69eafa0d5c29e888`  
		Last Modified: Sat, 19 Oct 2024 20:15:43 GMT  
		Size: 19.1 MB (19139411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f96c4ea371cee90138185fe10aadcd22560970b98ab4006bc7a68eb7b0f2fcf`  
		Last Modified: Sat, 19 Oct 2024 20:15:42 GMT  
		Size: 10.7 KB (10707 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:52b391de693cb5e80e7de84ea27b25737c6fb004a0710a5147d8cb91c4794ea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:1a30e3efd2aeec024b3788ac35f5d482a60f1ec9e625a88b1f03bbf4c4b092d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.8 MB (774824098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc4c23ec7077bc95f2907d6a4ea1fe9c8b994c985ab35fd8c70ef7abdcb716a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f6366eecac5038cc46d463f38273eb242aa8dabb1ae4f2de2372c8144b0dc3`  
		Last Modified: Sat, 19 Oct 2024 03:56:49 GMT  
		Size: 113.7 MB (113739991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5740e66cf000c28c07c81e998d5505ee0c7dc2c801f248d6c102ce7c6f9b3724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10120584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0cb824ac7aef1084cf788f11ad2b402bfb3d0a27a80903f5c09e6ca31697b`

```dockerfile
```

-	Layers:
	-	`sha256:4a1584f030c6f008b49e59b70705a407a866f47132f7283fca431e5f1fac5157`  
		Last Modified: Sat, 19 Oct 2024 03:56:48 GMT  
		Size: 10.1 MB (10109483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5620ce8906725295fdbda4ad6d80a33bacf48e516ac901190b55e0b74fe79ae`  
		Last Modified: Sat, 19 Oct 2024 03:56:47 GMT  
		Size: 11.1 KB (11101 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9f10709da1dae6901a1b117b66591f596483739a950170432aa56d76f98e1fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **767.0 MB (767048025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0080c09d01598d6cf7729d3b5a3acaa6c079fd3e37c4d160b42c3a59ec3d0f91`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c460b6cc813335a293de06cbf1af1684e6c0869b5e8e38a578b596ccf86f242`  
		Last Modified: Sat, 19 Oct 2024 20:39:49 GMT  
		Size: 108.3 MB (108281387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:209ce8ee9fd1a23c2cfcaf621cafece15fe7289dad3bac77c4493cf7fb3b950b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10115111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f024458071ec6fd401220adda2afaa36e7d51b603b26b5636d1de958d35d2d5`

```dockerfile
```

-	Layers:
	-	`sha256:e1153b5d0bd1dbabc290ff37e4256b77355a5d8cb5b472cac148a7955612d82e`  
		Last Modified: Sat, 19 Oct 2024 20:39:47 GMT  
		Size: 10.1 MB (10103918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98075dfb713e33d02cd76ee8c8bf93effbbf12c3e2e57ca21075dcf741cd0f2a`  
		Last Modified: Sat, 19 Oct 2024 20:39:46 GMT  
		Size: 11.2 KB (11193 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu`

```console
$ docker pull spark@sha256:69fda212e1b079ced36ed84baeef0cb47c18485ba9627a80119b2b96033f1524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:bc366a36cc055612b85507934ab4cd1878af42e32dc84a88877298a5cab50e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.4 MB (980394455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e115dfd7ec28e8b5303db1321a7de5b51d801190b48ca52a0cdb83e1165dceb`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fa3b327f0b26d368aff6b633627233ce79ac5be96273786c0eeb5de8d7117e`  
		Last Modified: Sat, 19 Oct 2024 03:59:00 GMT  
		Size: 319.3 MB (319310348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:96710a4b3dfb4531ee89ea63182be82d530ee198c1985fb77fd454b67d253ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18171049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dbc120de2790ba810694143c03d76075e71d2c2a3b77c7f596f2c4271deb21`

```dockerfile
```

-	Layers:
	-	`sha256:d63dd1552f4e3a4b6ded1dee0b9122890c6c20c355115c1fb70b3d810491b277`  
		Last Modified: Sat, 19 Oct 2024 03:58:55 GMT  
		Size: 18.2 MB (18160270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0a2faad6eba76d5e1a71c2f1ba92e56aaa291289e3e1ffc876471275f4a062`  
		Last Modified: Sat, 19 Oct 2024 03:58:54 GMT  
		Size: 10.8 KB (10779 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2779b5935f42d79e1b31bc885f338135dcf018ac4b9b03436c021b912e778902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.2 MB (961244883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f4e38a6ebe31c9f5a9028049ac9b9a0694751805e8a0cccf6d729db1b9e98`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329d1f817b82d41dcd6fd1f6b2ab26d46e7fb95fd0eab5bcc75b188631f907a4`  
		Last Modified: Sat, 19 Oct 2024 20:43:22 GMT  
		Size: 302.5 MB (302478245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:836272be062ba3a9b4f395399b4ef642c90ec847dd0f18f3a213d00232250924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18136532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40dbe708955b9e71f1afc16bdc658a74dce453790ca20cf86ab5e9e5838195a`

```dockerfile
```

-	Layers:
	-	`sha256:e8066279d34ddff9d92057123a7fd3643031b747433f809280a38684898396ef`  
		Last Modified: Sat, 19 Oct 2024 20:43:15 GMT  
		Size: 18.1 MB (18125673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247bea43656e8a6dbdecfe3d997b520a2b002db41630e64c39b7e26f62f2980b`  
		Last Modified: Sat, 19 Oct 2024 20:43:14 GMT  
		Size: 10.9 KB (10859 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-ubuntu`

```console
$ docker pull spark@sha256:01a940f8dd73f83bfa47b9d39e1fc564fccecf985ecc53651795aba8a1b7d2fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:d967bdb37dfc18d69204620ac2565fb9cfc175790a44f0428bad89a93012caf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.1 MB (661084107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88a124ccccadf2777ffecec69386996d7cf8f1cde1c369c26ae495ea7aa9ccc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51aa7cad03bdd7ccb4c8bfd0722d1d9cbd14cfc1b7a6d92566833df97b6ad`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94b8db32fc0e5dea74d9e918a555fc123363b73e5b5e842773140eacef67b`  
		Last Modified: Sat, 19 Oct 2024 02:59:29 GMT  
		Size: 24.9 MB (24897155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cde48f8fb4422fd1232e49973c6fd155b230bfd04c67c197f8eb5da7630906`  
		Last Modified: Sat, 19 Oct 2024 02:59:35 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e45907aa06d91307cbb9919723e0aaaa393655bfc6310ff65c9a029dd1cc6`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:57b625270f8a1a2ebb2d43c44cc969bcd58afafab90d90e88b8cde42fde3e7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4758013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42111e916a7469e0eade31797112ee73fb47596f5767f3a0bba38d8a05b91be5`

```dockerfile
```

-	Layers:
	-	`sha256:e52e7b06282b06ecad0eda765a8bef3284ee8401818eafcc63310ca34ed0f8aa`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 4.7 MB (4735014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:228dfec982d761925ee4be88a61a12db6930d51f181e86dc04d3553934d10bc4`  
		Last Modified: Sat, 19 Oct 2024 02:59:28 GMT  
		Size: 23.0 KB (22999 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fde7fa85c59d80333b596e114ced4e194c95f64d2d9d3c6abce13e7c7364af29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.8 MB (658766638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07209c44a2d88ce3287809da9d8be96ab33a89387d428630864b147c0b04722`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea4d7ad418a2f130fef632e730e45ba9035427b243adac3ae94db7012a992f3`  
		Last Modified: Sat, 19 Oct 2024 10:25:14 GMT  
		Size: 444.0 MB (444032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bf04a9177cfab44b3827027d4f825e5a6fee04c549824189c0700636e4507`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d21e82612acc5335a9e4e7d84cf853a2db774275e5a72ce1dbdd74f21e1b8d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4853738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245f50f9f1bf8475df66655026d0ab20533875c37b58963c4a2bf9a22b7c420`

```dockerfile
```

-	Layers:
	-	`sha256:9f619f340435ee8d50bfbb986053a779a41d00ee4cb6a97351116ab489c4d2fa`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 4.8 MB (4830629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d2069186133e49618ef40e2cee7dd2335ab0db3fd15644f14169daa6103b97b`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu`

```console
$ docker pull spark@sha256:53a8178dc4d928458adf2f435ae8e016d6a91ca2dc165a58c22af323b30cd137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:1b5d9db27bd4a7515d66ce2abe5b40f89cd712fcbd54a24df696a65da4eb5dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1008487854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d41362f246b5d4ea0f77e1e4d792f5062822b4604f0683132289e50f332b056`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd240a603b44b22dcbc1c5a81a409ef38b5a050974b7f72f39d557dc0ee86eed`  
		Last Modified: Sat, 19 Oct 2024 03:57:28 GMT  
		Size: 334.0 MB (333993739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:44af5870e04906ae938a522d017ff20fe15da367e3e8c0b8b24d889e5e519c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19188375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dacf755a52f65113bbd3ccd6834fc903a7c1e17d4add07ede0417dd580917f`

```dockerfile
```

-	Layers:
	-	`sha256:ae154615177259bd01971e7cc1aa4fd4e9937fd058c8a7ebdbb3ca83488f09e9`  
		Last Modified: Sat, 19 Oct 2024 03:57:24 GMT  
		Size: 19.2 MB (19177737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d13f861cadd8fe9e822af7a6ad70536408f74ec17771ae962bad01f340189d`  
		Last Modified: Sat, 19 Oct 2024 03:57:24 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4a1705f5d9334f804778cf78c8dc2f2795a6fbd2eea33bd431910e48f7a03ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.6 MB (988601755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5704a4f900aef7b4fb724054df56e44aec0247c0876a73386a35106706b6abf`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67f47872555a8b108ee9097fbc76a9518ce44ea4404d443546c042ce4b9ffd`  
		Last Modified: Sat, 19 Oct 2024 20:11:50 GMT  
		Size: 317.0 MB (317044128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e10cebfce5645877ca19c5f8fdd97ae6bf7b9e72dd3ce54672956504d68bde2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19153858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862264fb6f1eabd9a5b2b84711aef3d32da5dd98417104b30051cf1071b26889`

```dockerfile
```

-	Layers:
	-	`sha256:9f0c8610f36216853a2cccd428f9bc567d3ed8e2963beb2ca54f7730abf94bee`  
		Last Modified: Sat, 19 Oct 2024 20:11:44 GMT  
		Size: 19.1 MB (19143152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573d6e76fddb6748e33d87a926a7545fa08642c1edafdb6d1ba64a859a4802e2`  
		Last Modified: Sat, 19 Oct 2024 20:11:43 GMT  
		Size: 10.7 KB (10706 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu`

```console
$ docker pull spark@sha256:ea1780d3cb461337719b71e5bb7f327a7d3988b7b6aa0213bcda381b955d27ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:232a2f0dcfd5af63a41a2e687f936cf5376fd202d8641acb0ad11323b4574a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **788.2 MB (788234220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26941152e9f92ffc847d06593f2ef1f2760dfd0bfdb8106678015464027f0c9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb568b1f16cfc59ac36c34713fdadb00b7be69fa8589dc1650c0cf124eec667`  
		Last Modified: Sat, 19 Oct 2024 03:56:39 GMT  
		Size: 113.7 MB (113740105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:68c752b188fa88e5a3267d90e66482acc31771f9a32da05bcd9bd943f6a66599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10124379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dfd1d98280f1b8c4cf1385ddb7e5f735b97cb7d2aed167e5ee6f831c42a8b5`

```dockerfile
```

-	Layers:
	-	`sha256:3b8257292aed961082977a06e8f465b0ca415811c1cea1a696eba631ff37717c`  
		Last Modified: Sat, 19 Oct 2024 03:56:38 GMT  
		Size: 10.1 MB (10113252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e75b1964d25843a363d8540b05c6c5eea599af4acc51d5d5310b59604d2a86`  
		Last Modified: Sat, 19 Oct 2024 03:56:37 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:decb03be71d6ff1a16ff1eb44d01c09edbbdfd2a3d0f7e215316865b5a5ce107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.8 MB (779838550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35c0cc1de09cda55a2ba01d372fe0214272e3abece54e28fe0a367d95c65c33`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed0abe4c9197505695967e1bd0774e45a6cf8ecf17a6e72080b3b06db24624`  
		Last Modified: Sat, 19 Oct 2024 20:32:55 GMT  
		Size: 108.3 MB (108280923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4de2f30a07ef5b4811728d681b0e07dc2d6dd52f9267468a8e8780867f89cef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf79b9da0aaaebc1209aaff44f4c1c17b6bf18013c743676760107e21e9165dd`

```dockerfile
```

-	Layers:
	-	`sha256:86f6fe782b55b0f236f0ffe447e2c01e72604f1357ba2b6d8f030fea1efcedb8`  
		Last Modified: Sat, 19 Oct 2024 20:32:53 GMT  
		Size: 10.1 MB (10107687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88707dd2a9b21a19e27d32a5cef563df5707524c007821173905eb568b5aa22a`  
		Last Modified: Sat, 19 Oct 2024 20:32:52 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu`

```console
$ docker pull spark@sha256:7f515f6ff01abb66c58d54f508903cba7647b73b107c1cd6717cb646814b81f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:846443e5bf999785c32ceb39a12986ae183836d1eea084bf52c583c88681e34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 MB (993804052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9cb59e090c2b931b4e99aa3fe218fdfc5b315f1822cd593a6d948e1480cc9a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60074dc72be9d1c6c0f8fb660bf6ea34f853e31479f8c70c28af15c6105cc9a`  
		Last Modified: Sat, 19 Oct 2024 03:57:22 GMT  
		Size: 319.3 MB (319309937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0896eeda3f9d44cf1079e7f7d03baa12bb1fddcd45cb5ab7c490894ecae760ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18174817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf2d107be3bbfcedfd057052dd00c42ee4005616c7d226ab14f88ac6f0d658`

```dockerfile
```

-	Layers:
	-	`sha256:608f682bf8b8c1b863b5a009d26bb6935f5d7be92a925342a2a0e0401ff2651f`  
		Last Modified: Sat, 19 Oct 2024 03:57:18 GMT  
		Size: 18.2 MB (18164025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546575844471803c1b5fb87405c84a67f8a78cd62459f19bc9c880f62dd77735`  
		Last Modified: Sat, 19 Oct 2024 03:57:17 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8473b5d99a7e7bcbe3a8585d3fac4d87f7c38f1c531f3c0bf257e48bc8b2abe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.0 MB (974035649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c25493059b4356b8425392f1e88b70e4228c3487bb3add68fda39cf7e0b819`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b00eba9b8684e5fd428eaf14d31ed635d00f5e78314545b7ce1964b9ede6af`  
		Last Modified: Sat, 19 Oct 2024 20:37:09 GMT  
		Size: 302.5 MB (302478022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:24b6e20517e4e4a7b4385b9e0402a1435cef73b838d694908bf34edbe3f8fa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18140300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c040820cf2fa6d9b84ce57dd159c7d95760003ef92f7e31bbe8b1e5fe8ca30b7`

```dockerfile
```

-	Layers:
	-	`sha256:e03d8e9b806aded4789304cdd53c77df3af37cb6cc1bdad2758bb5186731fa96`  
		Last Modified: Sat, 19 Oct 2024 20:37:02 GMT  
		Size: 18.1 MB (18129428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f973f9348d5efdcbbf0e3d1a6eaabaf58715a5ab2e4a865146eb7f3c64e9ea5`  
		Last Modified: Sat, 19 Oct 2024 20:37:02 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-ubuntu`

```console
$ docker pull spark@sha256:a0eb35459d5169fb25f376d7f7526dc39acbbdded9d855d9b5fd98e24448ec56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3b2cf351ea3c834a1030b220315c2020523ac4de46f18c41caf28d612eb80dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.5 MB (674494115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e2df853051d2432170aabb094d613d2c1004971c49003ad2c632c8dd742484`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9263f251fdb2652d2aaa8eb7b2ba14a36795f617df3002192053f7fa95e76`  
		Last Modified: Sat, 19 Oct 2024 02:07:04 GMT  
		Size: 17.4 MB (17435898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe511953013b981d08a2c88e01ee70c01be8b90a36cafb09037ef842be0b64`  
		Last Modified: Sat, 19 Oct 2024 02:07:07 GMT  
		Size: 158.6 MB (158587595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e0a7da09ca25723e652d90d2121e006565f7f908ed65c18325280fc51f00cd`  
		Last Modified: Sat, 19 Oct 2024 02:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26942146920a12673c773420b0fd165fe13ea9b9fc19a5e712d81fed72a58`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904b6143e613a3a971dd728bfbb4756723c6ef13c863c5dab9a178b814c714a`  
		Last Modified: Sat, 19 Oct 2024 02:59:24 GMT  
		Size: 24.9 MB (24897085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93361c72a9638af9737ef9edb5371f63a2e3203e6be1679699dd3ef12799cfbe`  
		Last Modified: Sat, 19 Oct 2024 02:59:30 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f387d8a4c4ab1809b4dc04511a60ce4689c2c1d101f06818ef33cc20af3e`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f8e3c62d6b748ecda7fa3ca637af87310e4e4d88e2089bd4e7a39518d77f5d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4761779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2797e71dc55e13ee3bb81f26a22141e8d5f51c4bd3b6dc0f508aa86ea1d40722`

```dockerfile
```

-	Layers:
	-	`sha256:a6e0f0d7b4a13927b9c6db21202acf477cb4f9552a697337eb9f6136978bcd32`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 4.7 MB (4738769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a225ba703472461350cb8cec82923c3dea69b0b0283927f69d337b558948157`  
		Last Modified: Sat, 19 Oct 2024 02:59:23 GMT  
		Size: 23.0 KB (23010 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b18c67d473a558a72f910cd3b6b1297254dbef0c87a3695416a601f4fb3d9f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 MB (671557627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e395971532bb0218d483f3d03ec10bd403c9b42ed93d54850c7f6feff6e9d5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2d659d84ebd02a1393cf32279fd8a0a21158cc4093ebd83f7d92e22cf09a`  
		Last Modified: Sat, 19 Oct 2024 05:39:52 GMT  
		Size: 156.8 MB (156757979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d984b96159524a5b0d21b585442e43e3c10ae61ec17b47cdbea16cb016a74`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee98b18a682b38297eb7b22f7d9fd9fddac9479e22bd28f7f4577dab80bc84`  
		Last Modified: Sat, 19 Oct 2024 05:39:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef36eb7234e721bf05055d18ca05dc14a0be3e68a5cb81015d73ae43b66aed5`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5142b1a4376cae54272ce0fb8ca5a76ada6db117c5ecf685f3e1663e22ee13`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 24.6 MB (24561196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a3f16ea08a11adfb604bedb9c9b91abc12394365659222b6d1244a09e116f`  
		Last Modified: Sat, 19 Oct 2024 10:21:53 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f089ef7fce62fb022a093ac19021827f582a28dcf5f65ac3b6eb663c993bc0`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6cd8082982db7db48d5ed6bcc5cbc0213d0a7484613a6d6960a7d05534a57761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4857504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae1eee6b1d09617c6530d5b86255a438fbfc6b2178982d0dafee33c3131437e`

```dockerfile
```

-	Layers:
	-	`sha256:a57ec99c46f52afcf2fe407678d9606b249248e166dabf48de18f3458b078f90`  
		Last Modified: Sat, 19 Oct 2024 10:21:43 GMT  
		Size: 4.8 MB (4834384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ab582e581f3d654585d04da83778c769d6db2bd2241d293acd64fcec0d017`  
		Last Modified: Sat, 19 Oct 2024 10:21:42 GMT  
		Size: 23.1 KB (23120 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:latest`

```console
$ docker pull spark@sha256:87e5072a66233acc33c5be87df97d9222ccf87506e3b1eb2f19ec67f3521fc7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:7c46e98893b0bea0b156073c6322fb604a1bc2bdafb57954df954b8919615392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.8 MB (534825450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bc5cb3030aeff035eaf4c15c14035a5125f28f914d68c109f4f0b4ab462a2e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e8a38f365b1833707603c7367696d82be7bb983e4e0936836c0a51df026714`  
		Last Modified: Sat, 19 Oct 2024 03:57:37 GMT  
		Size: 94.4 MB (94363522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:7ae027b5af20136b0184957fcf888c8154d63aa2ff1cd7077f0a006516b06c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9106683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c982bcc231f273161c8f8dcd4cbe0375a17d1aa6b2d891363b086e17152e20a`

```dockerfile
```

-	Layers:
	-	`sha256:19a0f54f98a6122660a2328daea08f2dc7fc1c7bbc512ece992ef01f2329447b`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 9.1 MB (9095120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7c35de4255da0356bbeeb2a652ed9db3d700eab73576dc65e19743a99290a1`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f2f38e8f17b215f7da238a52981c15f63066193714a2e9c301fbaaca163c22ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524182847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653c551918ee722d3d6378deb1d11458902ff12869999eaaaea39662c571e36c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e51a6d72775f54aa3319ab3dec66092f226a8d502996e5138b39cdfbca7a8`  
		Last Modified: Sat, 19 Oct 2024 20:51:33 GMT  
		Size: 87.3 MB (87319332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:c4a9ba3e01e8c0a5b71d3bbe10de6ea55f3011aaf2e0a6517ecbb783b5d2fe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9110623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fb126440a97a54cdd88a3b1a89cca93f15296a1e6744d0c0580f4402d31195`

```dockerfile
```

-	Layers:
	-	`sha256:3e4eb379fb63badbc4ed56a7b84e08446b5aeb31e2450375597b92aed80d3524`  
		Last Modified: Sat, 19 Oct 2024 20:51:31 GMT  
		Size: 9.1 MB (9098944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ebb3615f1f59c1390c20a4d87210c0ae6abf0fbbed9fb54533419685b36c96`  
		Last Modified: Sat, 19 Oct 2024 20:51:30 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:87e5072a66233acc33c5be87df97d9222ccf87506e3b1eb2f19ec67f3521fc7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:7c46e98893b0bea0b156073c6322fb604a1bc2bdafb57954df954b8919615392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.8 MB (534825450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bc5cb3030aeff035eaf4c15c14035a5125f28f914d68c109f4f0b4ab462a2e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e8a38f365b1833707603c7367696d82be7bb983e4e0936836c0a51df026714`  
		Last Modified: Sat, 19 Oct 2024 03:57:37 GMT  
		Size: 94.4 MB (94363522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:7ae027b5af20136b0184957fcf888c8154d63aa2ff1cd7077f0a006516b06c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9106683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c982bcc231f273161c8f8dcd4cbe0375a17d1aa6b2d891363b086e17152e20a`

```dockerfile
```

-	Layers:
	-	`sha256:19a0f54f98a6122660a2328daea08f2dc7fc1c7bbc512ece992ef01f2329447b`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 9.1 MB (9095120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7c35de4255da0356bbeeb2a652ed9db3d700eab73576dc65e19743a99290a1`  
		Last Modified: Sat, 19 Oct 2024 03:57:36 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f2f38e8f17b215f7da238a52981c15f63066193714a2e9c301fbaaca163c22ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524182847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653c551918ee722d3d6378deb1d11458902ff12869999eaaaea39662c571e36c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e51a6d72775f54aa3319ab3dec66092f226a8d502996e5138b39cdfbca7a8`  
		Last Modified: Sat, 19 Oct 2024 20:51:33 GMT  
		Size: 87.3 MB (87319332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:c4a9ba3e01e8c0a5b71d3bbe10de6ea55f3011aaf2e0a6517ecbb783b5d2fe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9110623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fb126440a97a54cdd88a3b1a89cca93f15296a1e6744d0c0580f4402d31195`

```dockerfile
```

-	Layers:
	-	`sha256:3e4eb379fb63badbc4ed56a7b84e08446b5aeb31e2450375597b92aed80d3524`  
		Last Modified: Sat, 19 Oct 2024 20:51:31 GMT  
		Size: 9.1 MB (9098944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ebb3615f1f59c1390c20a4d87210c0ae6abf0fbbed9fb54533419685b36c96`  
		Last Modified: Sat, 19 Oct 2024 20:51:30 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:d10996cb72671857b8f869f3deb35747d26d9ace217672cd355d31b8b51dfd14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:17a6e46ef5244773e6a24b3287c5b3410c4ac73d66c1c97704e98867d2ebea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 MB (655660457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f956d55d1819bce2c3e036856062f44ff1d3c7d034531c10f83e7bc912150626`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567ff6aa27aea279fc8313a4d6dfbafabb01f316cf62ae48fa57ee9b6faf98`  
		Last Modified: Sat, 19 Oct 2024 02:06:57 GMT  
		Size: 17.4 MB (17435940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257a17fabbfc51124c42a2849741c1fc5609f6c5694f47bc7694f19678acf89`  
		Last Modified: Sat, 19 Oct 2024 02:06:59 GMT  
		Size: 145.2 MB (145177477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96158271acb1346c5bf4d29c1171ad327f12fd55ffa0750ef8b0b3870329d69`  
		Last Modified: Sat, 19 Oct 2024 02:06:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242f31717fc5a266a71c608ce9d8891830261e0e1c12a9306958a6958356f10`  
		Last Modified: Sat, 19 Oct 2024 02:06:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca63140ff013eb67ac2e483f453dd7b0619b6ec2f93df69102f4e1723dd73393`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199270ff334c9822f8f5d4233c1ed3c8abb8f7ed3098b1fc3e01630524aae069`  
		Last Modified: Sat, 19 Oct 2024 02:59:08 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7968dea1bc42afad0ad296c483491479f502bca92a1cf2d68d510c914ccda`  
		Last Modified: Sat, 19 Oct 2024 02:59:13 GMT  
		Size: 324.9 MB (324868526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096ec1ab7ed40c7b0a539074641ea74e2e9391b8072ea8563e2b357d6d8b796`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b8f1cd0cbd7fb8685624dd7fa7b3cb436e6a8029bc2aa9957583684165d9a`  
		Last Modified: Sat, 19 Oct 2024 03:57:35 GMT  
		Size: 113.7 MB (113739864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:94241355b904f03bd7c0106eefe222a81866d45898bbdb94ad4578b0d91561c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9979324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb7f63984a0dc4cf67005bb454513db1a7c38f53b7afe520f2d1dbfc5b61b36`

```dockerfile
```

-	Layers:
	-	`sha256:6effb41ff2d222794841f7889cf8d189c8f53b6e7e561db1ede64b7be1263ddd`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 10.0 MB (9968012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6625829987fb97a0b2de6a8192018e365fa51ce446447ad66cae438fe1f6c54`  
		Last Modified: Sat, 19 Oct 2024 03:57:33 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07e09a83d6dd5d5b8ba62953ac271a8a4b9401e97df164182b94d3e3bec146ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647883758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c069feced92260d8423f5c0fdaeeaf4da8becc09b74acf3361827167c991a21`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4328c2660e2acfd7df28e6cce03f948be8bfd9bc327b3747dcbddc8199302b`  
		Last Modified: Sat, 19 Oct 2024 05:36:25 GMT  
		Size: 18.8 MB (18842272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b4f156363cc8751d4ca24fe1b36d8f3c4fc0335ce6e49a8123255d79912f0`  
		Last Modified: Sat, 19 Oct 2024 05:36:28 GMT  
		Size: 144.0 MB (143967033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a83363ff0741a526836ef065ab1bd42f1332ee3f997f5c2030f92a9c8c6ca`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c3705559939101aebca8ea7598e75955b991ff61cfce66869f1e790abd370`  
		Last Modified: Sat, 19 Oct 2024 05:36:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da19d50e7d22889fb962184eb4b0438d0f8f41a6fc745256204275fc7b9e0`  
		Last Modified: Sat, 19 Oct 2024 10:25:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4286d41f81c5a821ed3fa6475b3acb47de490829c6073bb0fdbd51e93b95be7`  
		Last Modified: Sat, 19 Oct 2024 10:25:06 GMT  
		Size: 24.6 MB (24561123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da093b506b19294aa58706b367bba9c50f6e56e0fb2ee20232f7e9f71a184c`  
		Last Modified: Sat, 19 Oct 2024 10:28:49 GMT  
		Size: 324.9 MB (324868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffc52ae401ed5010cdd020acc950ced8b628944012e71f40bec7b92bef6d46`  
		Last Modified: Sat, 19 Oct 2024 10:28:42 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de733cea9df4008028a83681c30b600f13b07b9ea301fe2a403f793bcd1de46`  
		Last Modified: Sat, 19 Oct 2024 20:45:43 GMT  
		Size: 108.3 MB (108280712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:9eca174b852c37ab632025400c05f5aac2e47b417669393213945db370d05be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9973873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8394dad5755ee38b22b7fe70ea8d33b907570ee27a3a3c4f5ae6855e680a0a5d`

```dockerfile
```

-	Layers:
	-	`sha256:41b639b112327c903e5f7c89d5f694a8bfaa9791441aa112d8319e36c6cb2b04`  
		Last Modified: Sat, 19 Oct 2024 20:45:41 GMT  
		Size: 10.0 MB (9962459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa0941162aba1dbd5021b7022bd92631fd7dd82e35f1f3b00120ff14517aa18`  
		Last Modified: Sat, 19 Oct 2024 20:45:40 GMT  
		Size: 11.4 KB (11414 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:r`

```console
$ docker pull spark@sha256:6b806b6db4d9a44f4efaa40e6b40687da0b0337702d99e2431a5bbe7236d6428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:d24f88385165563cb7587699b10fff3427980371499f68fec9dcbddc0b96ac9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672755890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf338e6d8f6e8c3098be0970fe3f0d067e47cca9d8b6c259a9c1679780e819`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d82af4f5e587c52a1d7d59a7c2744ed1df96042b8e3e8571d8d72cbc42e53`  
		Last Modified: Sat, 19 Oct 2024 03:58:15 GMT  
		Size: 232.3 MB (232293962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:6fdc9103345e74f956adac4f03d9382a446e2d55cd7e5f8e8e05f67bd0c361ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db881f47a3b618af5b200b67450c288d85535a3e74aae65a1b3954ed24fe9cbd`

```dockerfile
```

-	Layers:
	-	`sha256:67375003d3c76ff7cee5afa79883fc262225bbaac5a321e6a57e2d1579dc20cf`  
		Last Modified: Sat, 19 Oct 2024 03:58:11 GMT  
		Size: 11.3 MB (11268163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d10454e5ed40b9f9484da9afa4a4aea2302ded269581c0966a833adc8e43e9`  
		Last Modified: Sat, 19 Oct 2024 03:58:11 GMT  
		Size: 11.0 KB (10952 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8e236f0f77a8dffdc275b72b3751b0262c8c092da62f83c66cfacb36fc4c6fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.4 MB (650369967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2584d6821039f02aa7d39a10296488400cce7d441c1e32fd707a4c72f3ff3606`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c15203a3b832a6bf097eaadfe5334e323b7ede17afcdc939e3058f32343a3d0`  
		Last Modified: Sat, 19 Oct 2024 20:54:27 GMT  
		Size: 213.5 MB (213506452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:5d6e376f543068def7000626d6b77fcb1200cf7d18562db4f3291beec3a24655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11263340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356d79baf2ae3102256f7272c0f3d955c12ac7fab5217ea7ee900ec80be73b3`

```dockerfile
```

-	Layers:
	-	`sha256:92bcc3f3766a7aa49648110038062196e95eedab0bd883f2dc1dec6ad6534889`  
		Last Modified: Sat, 19 Oct 2024 20:54:22 GMT  
		Size: 11.3 MB (11252296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20897221290be9049ef264a1c290ab559375434844adbc463059c01c0123a092`  
		Last Modified: Sat, 19 Oct 2024 20:54:22 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:scala`

```console
$ docker pull spark@sha256:b6d253f9f5d758ed2ac967d042a6c793b0e41fbdd4612e19a16f10d7f63629bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:37369531ea1b50ca65070ed10d5be68fb307d5bf7bc5bfe5f520aaa8a40b58d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440461928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5e17d604f32589289c5b2e93e6c61d81ee591aec43353a19b906e2d57de553`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b513a2f2b3d19816bd0306bbf46c498689b5cb525a6a2b5fdd9ae41c41d9f7c`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 16.9 MB (16931659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81f0fde9d59863f1ceb0d1e4cfe6ee8f8675625c1462bcee0d5bcdee1bd1a`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 47.2 MB (47197647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba592c85d7591a5575d839f8cabe82480b92da8acb2b8a6e897f3b1d9dd9ce`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2070c4ceb9495f0358c82193cfd5618fbe955724c0613f03998d5f90453bed`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c23b1f8313d8aec8eb9e4bef3298f99f142a5c40e844f7fddd5ebf77b18717`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da51f3ff96751cd7a461d946c9b0c73e09c5631bc3f211367ced32b3ec112ed2`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 23.9 MB (23947303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bb6f823afb512714c1b1a8bc9be7371c09e639bafb67f0771deee06fa6f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:31 GMT  
		Size: 324.9 MB (324868406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9549e43fc998c00a2b37a937e022819ef4c1040b2b7c6b0e2b612c4dd180a6`  
		Last Modified: Sat, 19 Oct 2024 02:59:27 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:a42e4f5ad2684c05c877142b952e9b4b8ab238cdad13d0c28cc18fddfea71453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4387356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376c0a8d363021b6b3c604741971b6766ecc6717debe8b6921762622469ce0d`

```dockerfile
```

-	Layers:
	-	`sha256:d29c0bebb95290113ff07c8e3c10cbe63e323f97089f1e0e4196f10297e94b91`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 4.4 MB (4364209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c23d3a7313e1a3c52dd7052fbb48edd238b0d33b839fa2e72867b797524d2c`  
		Last Modified: Sat, 19 Oct 2024 02:59:26 GMT  
		Size: 23.1 KB (23147 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:514c6bf838f1a5f7152a85e27610ea70caf1eb403b68bc00633b57ecd372d07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436863515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac54614220459fe2fca66183fc248bd9b35fc5a3526bd8426dd91eb0187f7d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f166f79564266fc7a00d8e4e1231e8fec706b566396090805f105fd928bed8a`  
		Last Modified: Sat, 19 Oct 2024 05:33:11 GMT  
		Size: 45.6 MB (45557352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd735549983a952493de88bdcc122e7ae83a5e91c6a7cdb94ba6233e1b9d0af`  
		Last Modified: Sat, 19 Oct 2024 05:33:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef62dc7f50f2aa0a9196a02e1f06374db054f94b368b62e5afd2ac2506b5c8`  
		Last Modified: Sat, 19 Oct 2024 05:33:10 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1096f84595ee6f6e80cb95e43cdd0f96dd3e82456ab0ca65eb4dc7dcc7b712d`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02082fea91df25fea0040ec41e26052a9572f1da84658f0af0c03141f603d2`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 23.7 MB (23670333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203aa6bdaa02cec0ea42a74ad782eadcb556fd8afca1acc0592f56a35fbf19e`  
		Last Modified: Sat, 19 Oct 2024 10:32:01 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c183373c2f9dfd44876d40689a8ece8dda16812d0f4e4b13e1f94395d296`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:1418b1370fe1ff4cdc95385ad9f9963585d73417403ac1a7d52472c9718fc80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4387781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b42fb8becad584e32987757ee9ae862dfdb1abe173b96a63eeb1071ff95c4b`

```dockerfile
```

-	Layers:
	-	`sha256:99e16d310b094301529958980e972eda787ee77ca3fb3298837395bce204b0ec`  
		Last Modified: Sat, 19 Oct 2024 10:31:52 GMT  
		Size: 4.4 MB (4364512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc402ec52c7713eedd4489491145ddc10bceb1510f3fb4a6a63e5f8d90c9756b`  
		Last Modified: Sat, 19 Oct 2024 10:31:51 GMT  
		Size: 23.3 KB (23269 bytes)  
		MIME: application/vnd.in-toto+json
