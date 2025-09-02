<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spark`

-	[`spark:3.5.6`](#spark356)
-	[`spark:3.5.6-java17`](#spark356-java17)
-	[`spark:3.5.6-java17-python3`](#spark356-java17-python3)
-	[`spark:3.5.6-java17-r`](#spark356-java17-r)
-	[`spark:3.5.6-java17-scala`](#spark356-java17-scala)
-	[`spark:3.5.6-python3`](#spark356-python3)
-	[`spark:3.5.6-r`](#spark356-r)
-	[`spark:3.5.6-scala`](#spark356-scala)
-	[`spark:3.5.6-scala2.12-java11-python3-r-ubuntu`](#spark356-scala212-java11-python3-r-ubuntu)
-	[`spark:3.5.6-scala2.12-java11-python3-ubuntu`](#spark356-scala212-java11-python3-ubuntu)
-	[`spark:3.5.6-scala2.12-java11-r-ubuntu`](#spark356-scala212-java11-r-ubuntu)
-	[`spark:3.5.6-scala2.12-java11-ubuntu`](#spark356-scala212-java11-ubuntu)
-	[`spark:3.5.6-scala2.12-java17-python3-r-ubuntu`](#spark356-scala212-java17-python3-r-ubuntu)
-	[`spark:3.5.6-scala2.12-java17-python3-ubuntu`](#spark356-scala212-java17-python3-ubuntu)
-	[`spark:3.5.6-scala2.12-java17-r-ubuntu`](#spark356-scala212-java17-r-ubuntu)
-	[`spark:3.5.6-scala2.12-java17-ubuntu`](#spark356-scala212-java17-ubuntu)
-	[`spark:4.0.0`](#spark400)
-	[`spark:4.0.0-java21`](#spark400-java21)
-	[`spark:4.0.0-java21-python3`](#spark400-java21-python3)
-	[`spark:4.0.0-java21-r`](#spark400-java21-r)
-	[`spark:4.0.0-java21-scala`](#spark400-java21-scala)
-	[`spark:4.0.0-python3`](#spark400-python3)
-	[`spark:4.0.0-r`](#spark400-r)
-	[`spark:4.0.0-scala`](#spark400-scala)
-	[`spark:4.0.0-scala2.13-java17-python3-r-ubuntu`](#spark400-scala213-java17-python3-r-ubuntu)
-	[`spark:4.0.0-scala2.13-java17-python3-ubuntu`](#spark400-scala213-java17-python3-ubuntu)
-	[`spark:4.0.0-scala2.13-java17-r-ubuntu`](#spark400-scala213-java17-r-ubuntu)
-	[`spark:4.0.0-scala2.13-java17-ubuntu`](#spark400-scala213-java17-ubuntu)
-	[`spark:4.0.0-scala2.13-java21-python3-r-ubuntu`](#spark400-scala213-java21-python3-r-ubuntu)
-	[`spark:4.0.0-scala2.13-java21-python3-ubuntu`](#spark400-scala213-java21-python3-ubuntu)
-	[`spark:4.0.0-scala2.13-java21-r-ubuntu`](#spark400-scala213-java21-r-ubuntu)
-	[`spark:4.0.0-scala2.13-java21-ubuntu`](#spark400-scala213-java21-ubuntu)
-	[`spark:latest`](#sparklatest)
-	[`spark:python3`](#sparkpython3)
-	[`spark:python3-java17`](#sparkpython3-java17)
-	[`spark:r`](#sparkr)
-	[`spark:scala`](#sparkscala)

## `spark:3.5.6`

```console
$ docker pull spark@sha256:d8a757b4a4a07e3807a072b018be6b10d83370d14a5ae3426847b4674b9b9d54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6` - linux; amd64

```console
$ docker pull spark@sha256:39338d3b9bd63f69df00c83890cfb43dea97abb28e29422c139b762f463408e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540743218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2216eb2b1bf95cd859a5ea2c653a44264d61ead6e0e5beb1f68e89d075341c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ccc4f4e71e656f173089523ebb5c8a71534bf872dd0aa8137cd1d7bfa2e58`  
		Last Modified: Tue, 03 Jun 2025 20:17:59 GMT  
		Size: 94.4 MB (94373736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6` - unknown; unknown

```console
$ docker pull spark@sha256:0820a2c55efd7e22b4bf8cf3f82432f80619c585d6cd01ace26bfd3eeb96cba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9181659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257d3c6890deae99855f5cb5a74b7afa14f96a65efb201a79f7d51bf05eac0b2`

```dockerfile
```

-	Layers:
	-	`sha256:3836e91372c376b6cfb9f35e75b84f041fb34766c39281e7335b1ddd28c1abc8`  
		Last Modified: Sat, 07 Jun 2025 17:14:38 GMT  
		Size: 9.2 MB (9170690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c82b6923eca683b3e424b648780f53611cc55f2249facea83682e1af809be32`  
		Last Modified: Sat, 07 Jun 2025 17:14:26 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f8cfdb9560d4e892e18cc5bd92cb58c12a315b4afdc67e75933e5eb157f24a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529196531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c1ee2cb4e6a486cb1ce396c745ae19e1cfb8d1af743820ed7ed7003ba648f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fed4e2bdf55f6a5d78bc0392d23e2db809a04a116f228a5d941cf54a2e123`  
		Last Modified: Thu, 05 Jun 2025 08:47:34 GMT  
		Size: 87.3 MB (87311898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6` - unknown; unknown

```console
$ docker pull spark@sha256:4d78554d1f5ea665c6e75d29683628dedbc7a69940a92fa0d60e2d30f2055529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9185256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cd351eb039ad3d8b9125b0140847ad430746e36754942ad3634a81feb4777d`

```dockerfile
```

-	Layers:
	-	`sha256:a2d67c4f5db22e27405b340ef7c9378fe2bf5887eac02506277d53f42e523ab6`  
		Last Modified: Sat, 07 Jun 2025 17:14:01 GMT  
		Size: 9.2 MB (9174195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072bd581f37a35a134b9ccf6cd9848fc7673b2c06480fb6f315b05e8ef7008fc`  
		Last Modified: Sat, 07 Jun 2025 17:13:50 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-java17`

```console
$ docker pull spark@sha256:3d8dbf92e931b7c90d12a5184980f2e927ed5e800b6e9bb20687cf40a399eacd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-java17` - linux; amd64

```console
$ docker pull spark@sha256:85f5fbdaf6f30cdc645d974d89794b03841f56f397d3876a4587509bdf34feff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 MB (655305795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a51582bebaa9557d0f1f41c7d4a30ef0d7587ad47e72e1fa1f9a128ddb263b0`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ea3914807494138e249f2607629b22a381a1b7d716facfc68533af3990be4`  
		Last Modified: Tue, 02 Sep 2025 01:14:11 GMT  
		Size: 113.7 MB (113737025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17` - unknown; unknown

```console
$ docker pull spark@sha256:8c22e4082c88bd888a00ecc58094a39c58b04e3a386ae04a860326db9531a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b161b5b4bd3f03f36aec2b35a4a7c577180233a4186d862b39582626cdb5051`

```dockerfile
```

-	Layers:
	-	`sha256:645b6f52c32358b6976b8d68fbba9c451ec54124d18247a2bf6e184a5c7bc279`  
		Last Modified: Tue, 02 Sep 2025 05:10:22 GMT  
		Size: 10.3 MB (10287450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023104764c24270316e263757fabf6c3ed2f2fd288f557b81350c274da4d8ea0`  
		Last Modified: Tue, 02 Sep 2025 05:10:23 GMT  
		Size: 11.0 KB (11000 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cf81cbba1b828e95f69b9cf4eba4795e6614b4801053f1d5cf26a21524cb8c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.6 MB (647559229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b7b5a7eb196134f9ef8b39a98c15533db165df3fe0c75714bb2f2a6166c3fe`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731802779598cf7272bb9cef7e2800c1c23d8541bad7fb5ccf74d8c9f6522078`  
		Last Modified: Wed, 13 Aug 2025 03:33:46 GMT  
		Size: 324.9 MB (324927868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04f9e55075945fb216ac24ba38aa27d01d853c7cb112c42637bcde5374253e`  
		Last Modified: Wed, 13 Aug 2025 00:52:59 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa231ee19d55f9a9c86702103714e73e65683284b4cc99158af045f670026809`  
		Last Modified: Wed, 13 Aug 2025 15:10:13 GMT  
		Size: 108.3 MB (108284708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17` - unknown; unknown

```console
$ docker pull spark@sha256:e1d81cf15b4098a7c922f9090aa81c9ed85e19a393cb4277b7bc94c04f354720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4a7b7ed83f530e23c41d53a0a5ce5e5cd1e24c7695a80ec9087ef95954d66b`

```dockerfile
```

-	Layers:
	-	`sha256:850bb7930a7b5e05a73ed4db954e6ace99f0db0fa912912e31d7e37f52a23eb8`  
		Last Modified: Wed, 13 Aug 2025 17:10:24 GMT  
		Size: 10.3 MB (10281821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c25893bac0e55e4e3d34a87c1d934ccdbc1eb3219bf5bc4c028c925b300071c`  
		Last Modified: Wed, 13 Aug 2025 17:10:25 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-java17-python3`

```console
$ docker pull spark@sha256:3d8dbf92e931b7c90d12a5184980f2e927ed5e800b6e9bb20687cf40a399eacd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:85f5fbdaf6f30cdc645d974d89794b03841f56f397d3876a4587509bdf34feff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 MB (655305795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a51582bebaa9557d0f1f41c7d4a30ef0d7587ad47e72e1fa1f9a128ddb263b0`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ea3914807494138e249f2607629b22a381a1b7d716facfc68533af3990be4`  
		Last Modified: Tue, 02 Sep 2025 01:14:11 GMT  
		Size: 113.7 MB (113737025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:8c22e4082c88bd888a00ecc58094a39c58b04e3a386ae04a860326db9531a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b161b5b4bd3f03f36aec2b35a4a7c577180233a4186d862b39582626cdb5051`

```dockerfile
```

-	Layers:
	-	`sha256:645b6f52c32358b6976b8d68fbba9c451ec54124d18247a2bf6e184a5c7bc279`  
		Last Modified: Tue, 02 Sep 2025 05:10:22 GMT  
		Size: 10.3 MB (10287450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023104764c24270316e263757fabf6c3ed2f2fd288f557b81350c274da4d8ea0`  
		Last Modified: Tue, 02 Sep 2025 05:10:23 GMT  
		Size: 11.0 KB (11000 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cf81cbba1b828e95f69b9cf4eba4795e6614b4801053f1d5cf26a21524cb8c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.6 MB (647559229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b7b5a7eb196134f9ef8b39a98c15533db165df3fe0c75714bb2f2a6166c3fe`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731802779598cf7272bb9cef7e2800c1c23d8541bad7fb5ccf74d8c9f6522078`  
		Last Modified: Wed, 13 Aug 2025 03:33:46 GMT  
		Size: 324.9 MB (324927868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04f9e55075945fb216ac24ba38aa27d01d853c7cb112c42637bcde5374253e`  
		Last Modified: Wed, 13 Aug 2025 00:52:59 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa231ee19d55f9a9c86702103714e73e65683284b4cc99158af045f670026809`  
		Last Modified: Wed, 13 Aug 2025 15:10:13 GMT  
		Size: 108.3 MB (108284708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:e1d81cf15b4098a7c922f9090aa81c9ed85e19a393cb4277b7bc94c04f354720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4a7b7ed83f530e23c41d53a0a5ce5e5cd1e24c7695a80ec9087ef95954d66b`

```dockerfile
```

-	Layers:
	-	`sha256:850bb7930a7b5e05a73ed4db954e6ace99f0db0fa912912e31d7e37f52a23eb8`  
		Last Modified: Wed, 13 Aug 2025 17:10:24 GMT  
		Size: 10.3 MB (10281821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c25893bac0e55e4e3d34a87c1d934ccdbc1eb3219bf5bc4c028c925b300071c`  
		Last Modified: Wed, 13 Aug 2025 17:10:25 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-java17-r`

```console
$ docker pull spark@sha256:fbfa771aaabd423d3633c3031cb699b46d8428a01d8527e2c91f9b426de4625c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:a159c642e0edb83f6793dc5a35791ad4314fa026897f509e155fef28a048f74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.9 MB (860891789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226f23b8393e6df9eb264cda0956030ee84a9b8e692a6e5ec644fa5040d740d7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282fd6eec70c90644a2b089661ad06514afec2fd8ff2f85d139953e689464b04`  
		Last Modified: Tue, 02 Sep 2025 01:14:29 GMT  
		Size: 319.3 MB (319323019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:0e7c2cbd80863ee9e09ed409bc36f1c51bdfcf5994c015412e9d8e93dd13c14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18493679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aec9db907956b221d9f16c848664af31fa560a4e77117f4f87bb6c00eb1ed70`

```dockerfile
```

-	Layers:
	-	`sha256:eec5056d7aea42c4672feda8807e9442e0dad4ddf21aa4d3d4d0295a34cba268`  
		Last Modified: Tue, 02 Sep 2025 05:10:27 GMT  
		Size: 18.5 MB (18482997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16f18fe0993540b229092cdd9bf797b76697457689af6a4934dd1c726ac3a1a`  
		Last Modified: Tue, 02 Sep 2025 05:10:29 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:342235f875a17c5dbf6cbe180b7f5b028b56dd366ee3f3ca37a27e8ae9599670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.8 MB (841770703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5966b3897911e6e2d2ff06c37b5b8d92adf55a93b2a021734dbe0b2bffc138`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731802779598cf7272bb9cef7e2800c1c23d8541bad7fb5ccf74d8c9f6522078`  
		Last Modified: Wed, 13 Aug 2025 03:33:46 GMT  
		Size: 324.9 MB (324927868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04f9e55075945fb216ac24ba38aa27d01d853c7cb112c42637bcde5374253e`  
		Last Modified: Wed, 13 Aug 2025 00:52:59 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb59d18c9a4dc285d039ed495ea1d8c3d6b0e47128cc8e4bbfee368ae095b69`  
		Last Modified: Wed, 13 Aug 2025 18:18:07 GMT  
		Size: 302.5 MB (302496182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:a3009854cd8a810de040c966b51fbafebef2ddd9b6765faa0bd6b74d0c4b0f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18458223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac790ab4b6551a44ffe6778be85c54ed6adbe6a94f59d4d520982473f4e1bce`

```dockerfile
```

-	Layers:
	-	`sha256:c10c3b83c19b5588430b31578214e7e32b6af075750bea0efa306a468f808584`  
		Last Modified: Wed, 13 Aug 2025 17:10:39 GMT  
		Size: 18.4 MB (18447462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680bda6cf6f547c6dca572688c8cac1451a41232a10e5fb00a7d49c27407f730`  
		Last Modified: Wed, 13 Aug 2025 17:10:40 GMT  
		Size: 10.8 KB (10761 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-java17-scala`

```console
$ docker pull spark@sha256:4d54eb6add0ec3ce3d8c0cc326d14589e5d55321502aab6c483ff18dcf4a3cb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:db32bad2a16f15a2f4d51100aca2cb08d67ad9682beca65607196b031b79baca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.6 MB (541568770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dabd25618787909e5d4ccbed0c717bcce1abc7372a0404e4351a75dc63174a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:b569680a3cff0fb65b79e21eb214f0fc17af2747492f44722be863418ac8cddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4837197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a3a1e5eb6f957ffa9d8d775509c61f71c7466942bbbd107498f6e56c194af4`

```dockerfile
```

-	Layers:
	-	`sha256:928c93cee62977a06799d6f5a76031f5a616ccadde6cc64d77314ae784db5c1c`  
		Last Modified: Tue, 02 Sep 2025 02:10:22 GMT  
		Size: 4.8 MB (4814331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3914489c55a90bbd8ee683a1a81d1ba0d534eef65f6f4105788be80119557d3`  
		Last Modified: Tue, 02 Sep 2025 02:10:23 GMT  
		Size: 22.9 KB (22866 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9da24026a3496e7f74330c5c81dfb3c2b244a5d7010e984457d8d97517eeec1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.3 MB (539277013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4143fd6ca94b4b3e91e01b296c1e00bd2f7d90efed50bcadf712c3296feb61c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2d1bf87820e36d53f26b7cd674768abf44232e1496f26c39a0b8e513d4e8c`  
		Last Modified: Tue, 02 Sep 2025 01:03:42 GMT  
		Size: 22.1 MB (22075014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a562fdfee59db98ef10f59acb342e37698d1891b3f4608dab55a20e25c85093`  
		Last Modified: Tue, 02 Sep 2025 03:15:28 GMT  
		Size: 143.6 MB (143550948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6953a5f4a054b79b249f8f3bbd1be1a1c4f1873fa3be3cd054e0029f8a71087`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fd4799efced03c22e41b0e5ae8ece8022f4df5662e5b25352d453d8783892`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626a4a66c5c6a6908a2c062f2cc8209efbaeb14315a158a9e21a98144b4cad1d`  
		Last Modified: Tue, 02 Sep 2025 07:00:42 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d242d7a7a5680644c29be3300ebdcec7562015013b56c80b6ac0d7dc5142111`  
		Last Modified: Tue, 02 Sep 2025 07:00:45 GMT  
		Size: 21.4 MB (21355649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19ff606250fc7d01738c60958cd243dcd9716526a0e4982d11c356820dac75`  
		Last Modified: Tue, 02 Sep 2025 07:01:06 GMT  
		Size: 324.9 MB (324927897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5848a124ab4eae484508105150ee9efa4bfee3f1ea478f8a454730d9bf129d8`  
		Last Modified: Tue, 02 Sep 2025 07:01:00 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:0feaca3fa282bcb0a56958abadd2609ee1890c7d8e18737de154ac758e9f33c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb89d26291e2fdc9e892701bd6f8b95c045459aa7070cf8de315fe826d772ba6`

```dockerfile
```

-	Layers:
	-	`sha256:61814823bc481c7c4f26c3948a16c3ab556d5da4b380659ee28c6765209eee99`  
		Last Modified: Tue, 02 Sep 2025 08:10:27 GMT  
		Size: 4.9 MB (4909831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17110d023b3bfa87742dfba1e6587a5396a0d4fd4e671606f1d9198a24f21f9b`  
		Last Modified: Tue, 02 Sep 2025 08:10:28 GMT  
		Size: 23.0 KB (22976 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-python3`

```console
$ docker pull spark@sha256:d8a757b4a4a07e3807a072b018be6b10d83370d14a5ae3426847b4674b9b9d54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-python3` - linux; amd64

```console
$ docker pull spark@sha256:39338d3b9bd63f69df00c83890cfb43dea97abb28e29422c139b762f463408e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540743218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2216eb2b1bf95cd859a5ea2c653a44264d61ead6e0e5beb1f68e89d075341c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ccc4f4e71e656f173089523ebb5c8a71534bf872dd0aa8137cd1d7bfa2e58`  
		Last Modified: Tue, 03 Jun 2025 20:17:59 GMT  
		Size: 94.4 MB (94373736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-python3` - unknown; unknown

```console
$ docker pull spark@sha256:0820a2c55efd7e22b4bf8cf3f82432f80619c585d6cd01ace26bfd3eeb96cba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9181659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257d3c6890deae99855f5cb5a74b7afa14f96a65efb201a79f7d51bf05eac0b2`

```dockerfile
```

-	Layers:
	-	`sha256:3836e91372c376b6cfb9f35e75b84f041fb34766c39281e7335b1ddd28c1abc8`  
		Last Modified: Sat, 07 Jun 2025 17:14:38 GMT  
		Size: 9.2 MB (9170690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c82b6923eca683b3e424b648780f53611cc55f2249facea83682e1af809be32`  
		Last Modified: Sat, 07 Jun 2025 17:14:26 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f8cfdb9560d4e892e18cc5bd92cb58c12a315b4afdc67e75933e5eb157f24a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529196531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c1ee2cb4e6a486cb1ce396c745ae19e1cfb8d1af743820ed7ed7003ba648f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fed4e2bdf55f6a5d78bc0392d23e2db809a04a116f228a5d941cf54a2e123`  
		Last Modified: Thu, 05 Jun 2025 08:47:34 GMT  
		Size: 87.3 MB (87311898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-python3` - unknown; unknown

```console
$ docker pull spark@sha256:4d78554d1f5ea665c6e75d29683628dedbc7a69940a92fa0d60e2d30f2055529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9185256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cd351eb039ad3d8b9125b0140847ad430746e36754942ad3634a81feb4777d`

```dockerfile
```

-	Layers:
	-	`sha256:a2d67c4f5db22e27405b340ef7c9378fe2bf5887eac02506277d53f42e523ab6`  
		Last Modified: Sat, 07 Jun 2025 17:14:01 GMT  
		Size: 9.2 MB (9174195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072bd581f37a35a134b9ccf6cd9848fc7673b2c06480fb6f315b05e8ef7008fc`  
		Last Modified: Sat, 07 Jun 2025 17:13:50 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-r`

```console
$ docker pull spark@sha256:975681c9c0e8240befd2896bfe5b5d1c00370392f9cb2d458e94cf79a4bd15aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-r` - linux; amd64

```console
$ docker pull spark@sha256:5473c27a52c098ed0d1f165bdedaa490520c54658860623bba25de8d8f80a8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.6 MB (678633662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a318ac5d0c8973793cb18d098056c15810820316152f3b64e1d3a0e2649908`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e130ea817bf4e5e154638297cbd2571eacb975cfcf233309c40c5e2b21ba1031`  
		Last Modified: Wed, 04 Jun 2025 01:12:47 GMT  
		Size: 232.3 MB (232264180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-r` - unknown; unknown

```console
$ docker pull spark@sha256:eb38fc36b47b6911de4f23f58bfa2b009c907bcbf23d2df63c38be0a1c1be3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11384404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4b0885379a01c5806fff69c1e2b99b1ce496cc50df5e3da4a2178258d4559f`

```dockerfile
```

-	Layers:
	-	`sha256:a9f4f3962e07f3fa31a2cfeaf662a91d39cb6e97db907042c38fa22d60082691`  
		Last Modified: Sat, 07 Jun 2025 17:15:49 GMT  
		Size: 11.4 MB (11373738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed136716b896c006abb01632e3a9820bc13dc65dc607a2e63cebb43858225592`  
		Last Modified: Sat, 07 Jun 2025 17:15:35 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:989df9cfc389a284c689fb76f8816b498e3b7fad1ab1053a72997cb1e3c3e9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 MB (655368468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39d040f9365e7df8507be5fa719195efe4d7852c6cdea80c330db75a2b1c221`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c2b94117383896be58931fa3f63b6077bbfba8d1117c3dbac300ff729416d`  
		Last Modified: Sat, 07 Jun 2025 17:15:27 GMT  
		Size: 213.5 MB (213483835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-r` - unknown; unknown

```console
$ docker pull spark@sha256:fcc609356cd9885c4ccf2e371c0b06dfeab9217fb569dc017834c6471cae4873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11367767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50f02016d5125b637a2f4bfee0bdd32d3627b2234d13742f2b68b5579e5a7ef`

```dockerfile
```

-	Layers:
	-	`sha256:f17efe31b024138e2e188aba49112336577f6222abd805c8c5814a4290e666b3`  
		Last Modified: Sat, 07 Jun 2025 17:15:27 GMT  
		Size: 11.4 MB (11357021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2314662077c436b5211764dbdd2fa4bed529291bc49222fdfb7434e0efd299ac`  
		Last Modified: Sat, 07 Jun 2025 17:15:13 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala`

```console
$ docker pull spark@sha256:bc9119c0249e2f48d75da4938f9fbc47e6ed75670d7e8f8baad0c1a643120a1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala` - linux; amd64

```console
$ docker pull spark@sha256:3d1dbf6e9c76a17bef2d9642d8f321b41fdf4598f8d3d9a9f0b01b23bfd6d2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.4 MB (446369482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19766744f729c4dcd105b0da416f51016f8ea000d26db98d236cfd5c7695e14a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala` - unknown; unknown

```console
$ docker pull spark@sha256:3cd03d70fc093e7a8e87b57d7508a8377c831a1867cbfd02dce9b296ca528cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c45f36fe5e766507a9d44056f00b63daee605660f6fb9d334f122e9b5407bb3`

```dockerfile
```

-	Layers:
	-	`sha256:e4656e613e28d31835659c72627cc62693b8620a33f59889d26ad16d3468c390`  
		Last Modified: Sat, 07 Jun 2025 17:16:16 GMT  
		Size: 4.4 MB (4431589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837717b77d831ad6781016d2621bdcd0f786475f9ff7a702dc3210e693639b8f`  
		Last Modified: Sat, 07 Jun 2025 17:16:05 GMT  
		Size: 22.9 KB (22854 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8fee2a56fb778348169e1a35b67197409184d82fc78aabd4bf23b6be063d2a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441884633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88be5d8ee54142c3c12451fce213f6f3107f2e37366e1ccde3562d1bb423d52`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala` - unknown; unknown

```console
$ docker pull spark@sha256:372b847950a5abbf8d3b71c4485b800368795dd43bf02f740e4cbd236210c2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fb715e6aba506b3f8be12292079195c46a2ab7fd567667049d8df330aa3c81`

```dockerfile
```

-	Layers:
	-	`sha256:5a2342104725defb38e1c9f8a601838cfa772ffaf440e18d57804160b42b8f74`  
		Last Modified: Sat, 07 Jun 2025 17:15:57 GMT  
		Size: 4.4 MB (4431881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b179d198e9200bfc8a1a9fd6be6b80df9a0b5a5554bf26ce53e4b3ba7b5e2be2`  
		Last Modified: Sat, 07 Jun 2025 17:13:47 GMT  
		Size: 23.0 KB (22964 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:c499c1c245c2cc4212f791805196adf907d8428698c48dbcda709fa69d0967c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:4c1986dbc64097641f1ca6ddb0359fbc475a5b5a29d9b4d432a3a467e97a565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700264489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f32f46ee37d47f748d811fd395c47c2be4b78d024d66756a93baeb7c765072`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add4135cc6914a85134fdddcdc06dffee559a7dd077d816407403754483e0195`  
		Last Modified: Wed, 04 Jun 2025 01:26:27 GMT  
		Size: 253.9 MB (253895007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f1337e3aa95d79cd8f3fb389ab9f5f93f49fdf868b4432fb523ed0f0b435d888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12513672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93bc58cf9edad5db70b14983914bbfbc0a4ae807f3edd1793048d59bc5aca92`

```dockerfile
```

-	Layers:
	-	`sha256:0fefc1dead6421c30597b7d7002175e948fde82115f5333c80a9358e097552d4`  
		Last Modified: Sat, 07 Jun 2025 17:17:36 GMT  
		Size: 12.5 MB (12503128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81aad3c714cb6e5fd4145ebbec2017322c3c431ea3dfed0f58c1bea741c42c69`  
		Last Modified: Sat, 07 Jun 2025 17:17:30 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:edd0968b3ebb295e540c806ef157b5178958ef7b3e3fd75c0d35b53b1f53f160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (677012709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabd8e52a4e6bc518f96081bc5fa5e5f09ba128c28c361ba3c75adfb2b4a47ab`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6e920707b41588d4f2bdf2c4d0380edb3244b5510116d33bab4f88ba0f833a`  
		Last Modified: Fri, 06 Jun 2025 05:19:49 GMT  
		Size: 235.1 MB (235128076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0199cd97122f12d934988f6efe2762890e480d3b1b466bc69677f94d4298ab87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12497078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e96dee3c6a4d2356f90a0b2cab1a5c2a3e23390a64e396cedc35d69db0ad66`

```dockerfile
```

-	Layers:
	-	`sha256:f16bc29da63024c90b91bcec9be7fb5b5949b0b36077e1fe5e8de8c26eef0de4`  
		Last Modified: Sat, 07 Jun 2025 17:17:00 GMT  
		Size: 12.5 MB (12486466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6b1c057b239c30fc1aa79438b765f6ffef2f19f6f243650eba7f7d19c70c4a`  
		Last Modified: Sat, 07 Jun 2025 17:16:55 GMT  
		Size: 10.6 KB (10612 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:d8a757b4a4a07e3807a072b018be6b10d83370d14a5ae3426847b4674b9b9d54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:39338d3b9bd63f69df00c83890cfb43dea97abb28e29422c139b762f463408e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540743218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2216eb2b1bf95cd859a5ea2c653a44264d61ead6e0e5beb1f68e89d075341c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ccc4f4e71e656f173089523ebb5c8a71534bf872dd0aa8137cd1d7bfa2e58`  
		Last Modified: Tue, 03 Jun 2025 20:17:59 GMT  
		Size: 94.4 MB (94373736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0820a2c55efd7e22b4bf8cf3f82432f80619c585d6cd01ace26bfd3eeb96cba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9181659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257d3c6890deae99855f5cb5a74b7afa14f96a65efb201a79f7d51bf05eac0b2`

```dockerfile
```

-	Layers:
	-	`sha256:3836e91372c376b6cfb9f35e75b84f041fb34766c39281e7335b1ddd28c1abc8`  
		Last Modified: Sat, 07 Jun 2025 17:14:38 GMT  
		Size: 9.2 MB (9170690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c82b6923eca683b3e424b648780f53611cc55f2249facea83682e1af809be32`  
		Last Modified: Sat, 07 Jun 2025 17:14:26 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f8cfdb9560d4e892e18cc5bd92cb58c12a315b4afdc67e75933e5eb157f24a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529196531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c1ee2cb4e6a486cb1ce396c745ae19e1cfb8d1af743820ed7ed7003ba648f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fed4e2bdf55f6a5d78bc0392d23e2db809a04a116f228a5d941cf54a2e123`  
		Last Modified: Thu, 05 Jun 2025 08:47:34 GMT  
		Size: 87.3 MB (87311898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4d78554d1f5ea665c6e75d29683628dedbc7a69940a92fa0d60e2d30f2055529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9185256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cd351eb039ad3d8b9125b0140847ad430746e36754942ad3634a81feb4777d`

```dockerfile
```

-	Layers:
	-	`sha256:a2d67c4f5db22e27405b340ef7c9378fe2bf5887eac02506277d53f42e523ab6`  
		Last Modified: Sat, 07 Jun 2025 17:14:01 GMT  
		Size: 9.2 MB (9174195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072bd581f37a35a134b9ccf6cd9848fc7673b2c06480fb6f315b05e8ef7008fc`  
		Last Modified: Sat, 07 Jun 2025 17:13:50 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:975681c9c0e8240befd2896bfe5b5d1c00370392f9cb2d458e94cf79a4bd15aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:5473c27a52c098ed0d1f165bdedaa490520c54658860623bba25de8d8f80a8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.6 MB (678633662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a318ac5d0c8973793cb18d098056c15810820316152f3b64e1d3a0e2649908`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e130ea817bf4e5e154638297cbd2571eacb975cfcf233309c40c5e2b21ba1031`  
		Last Modified: Wed, 04 Jun 2025 01:12:47 GMT  
		Size: 232.3 MB (232264180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:eb38fc36b47b6911de4f23f58bfa2b009c907bcbf23d2df63c38be0a1c1be3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11384404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4b0885379a01c5806fff69c1e2b99b1ce496cc50df5e3da4a2178258d4559f`

```dockerfile
```

-	Layers:
	-	`sha256:a9f4f3962e07f3fa31a2cfeaf662a91d39cb6e97db907042c38fa22d60082691`  
		Last Modified: Sat, 07 Jun 2025 17:15:49 GMT  
		Size: 11.4 MB (11373738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed136716b896c006abb01632e3a9820bc13dc65dc607a2e63cebb43858225592`  
		Last Modified: Sat, 07 Jun 2025 17:15:35 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:989df9cfc389a284c689fb76f8816b498e3b7fad1ab1053a72997cb1e3c3e9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 MB (655368468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39d040f9365e7df8507be5fa719195efe4d7852c6cdea80c330db75a2b1c221`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c2b94117383896be58931fa3f63b6077bbfba8d1117c3dbac300ff729416d`  
		Last Modified: Sat, 07 Jun 2025 17:15:27 GMT  
		Size: 213.5 MB (213483835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:fcc609356cd9885c4ccf2e371c0b06dfeab9217fb569dc017834c6471cae4873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11367767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50f02016d5125b637a2f4bfee0bdd32d3627b2234d13742f2b68b5579e5a7ef`

```dockerfile
```

-	Layers:
	-	`sha256:f17efe31b024138e2e188aba49112336577f6222abd805c8c5814a4290e666b3`  
		Last Modified: Sat, 07 Jun 2025 17:15:27 GMT  
		Size: 11.4 MB (11357021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2314662077c436b5211764dbdd2fa4bed529291bc49222fdfb7434e0efd299ac`  
		Last Modified: Sat, 07 Jun 2025 17:15:13 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:bc9119c0249e2f48d75da4938f9fbc47e6ed75670d7e8f8baad0c1a643120a1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3d1dbf6e9c76a17bef2d9642d8f321b41fdf4598f8d3d9a9f0b01b23bfd6d2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.4 MB (446369482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19766744f729c4dcd105b0da416f51016f8ea000d26db98d236cfd5c7695e14a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220469d844e19eca09db130c299b6e8a76d512de640cbdb1105f5f2569172f4`  
		Last Modified: Tue, 03 Jun 2025 20:17:54 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ef0489f6eb9f38e09061b8671a7d27ca5b0d9737c50849cce44b6cf7298a3`  
		Last Modified: Tue, 03 Jun 2025 20:17:56 GMT  
		Size: 26.4 MB (26440326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7d27ae26907775ccc9e4caa47aa8f254c7ca8ca4dd907954b35baa43e6c79`  
		Last Modified: Tue, 03 Jun 2025 20:18:28 GMT  
		Size: 324.9 MB (324927921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b044d78f89baaabf675bd351170ef0f57c92f1899c7d212f770f3d038c53ac`  
		Last Modified: Tue, 03 Jun 2025 20:17:52 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:3cd03d70fc093e7a8e87b57d7508a8377c831a1867cbfd02dce9b296ca528cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c45f36fe5e766507a9d44056f00b63daee605660f6fb9d334f122e9b5407bb3`

```dockerfile
```

-	Layers:
	-	`sha256:e4656e613e28d31835659c72627cc62693b8620a33f59889d26ad16d3468c390`  
		Last Modified: Sat, 07 Jun 2025 17:16:16 GMT  
		Size: 4.4 MB (4431589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837717b77d831ad6781016d2621bdcd0f786475f9ff7a702dc3210e693639b8f`  
		Last Modified: Sat, 07 Jun 2025 17:16:05 GMT  
		Size: 22.9 KB (22854 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8fee2a56fb778348169e1a35b67197409184d82fc78aabd4bf23b6be063d2a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441884633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88be5d8ee54142c3c12451fce213f6f3107f2e37366e1ccde3562d1bb423d52`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39eb0d0a576c0268a01f10e7a3335eabc2227245484075a5294dee777b755a5`  
		Last Modified: Thu, 08 May 2025 17:15:01 GMT  
		Size: 45.6 MB (45586195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9369e90a6ef48c9c267202dc47cb67bc92c3f1ab2d2aa12667c863842b8ea31`  
		Last Modified: Thu, 08 May 2025 17:15:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012db027792ddab2aed48b0ab00f656c39c4337188ef68b7228d4352c6c6b4`  
		Last Modified: Thu, 08 May 2025 17:15:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d4b199c434bf7108988be075f23ad9ef05abf165ab4f88048c4ba77290af`  
		Last Modified: Thu, 05 Jun 2025 07:36:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79448685bb6967240eb791c4c77125d9ed306d7d874d4ca15d546c988397fe56`  
		Last Modified: Thu, 05 Jun 2025 07:36:32 GMT  
		Size: 25.3 MB (25293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fb987619e0a57cb7b6471acc4b4e10ff2a9f7287fde06a9609f852ac58e1c`  
		Last Modified: Thu, 05 Jun 2025 07:36:42 GMT  
		Size: 324.9 MB (324927848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694bf7d4c82732da03688b575e3646723c58710ff3975232e5a27c75e7a1a8f8`  
		Last Modified: Thu, 05 Jun 2025 07:36:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:372b847950a5abbf8d3b71c4485b800368795dd43bf02f740e4cbd236210c2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fb715e6aba506b3f8be12292079195c46a2ab7fd567667049d8df330aa3c81`

```dockerfile
```

-	Layers:
	-	`sha256:5a2342104725defb38e1c9f8a601838cfa772ffaf440e18d57804160b42b8f74`  
		Last Modified: Sat, 07 Jun 2025 17:15:57 GMT  
		Size: 4.4 MB (4431881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b179d198e9200bfc8a1a9fd6be6b80df9a0b5a5554bf26ce53e4b3ba7b5e2be2`  
		Last Modified: Sat, 07 Jun 2025 17:13:47 GMT  
		Size: 23.0 KB (22964 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:6c6f3118a27930e0b02d5a9f936f9f8eb344ec7e70a36079471f824fc74c895b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:dc66393d0d41e80b4b37b50f76a31f82c026c347369722454f612bb0571d6f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.6 MB (875561389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7241a797ec01bcc99cd3e2c7e9eba71077dfdffb15adb6bf8d51e690191b4fc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3237e6b5286648d9140fd37cfc647d901df03707fb160ab669986de8539c22`  
		Last Modified: Tue, 02 Sep 2025 01:14:18 GMT  
		Size: 334.0 MB (333992619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2034cd3a4edda197c093fda44b136bcb6c8c6fb8876708d0af0c8e79974e2675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5198bb676085fdd2acd9cf5d9c4a9c2aec0c8ca75af232e1e4f33ab82de469`

```dockerfile
```

-	Layers:
	-	`sha256:8aa1bda17f1963739c72aa52b6e2192e11125318e7f5d5a1438a5c4fd7f35a52`  
		Last Modified: Tue, 02 Sep 2025 05:10:36 GMT  
		Size: 19.5 MB (19529142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41e197f40f1f8eccf78ce74e0cbae39b154b613cb1c6fa4245a29c853057b2c1`  
		Last Modified: Tue, 02 Sep 2025 05:10:37 GMT  
		Size: 10.5 KB (10546 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:41ace4fa39abc8701c52c6b0c3a95f00ce1e65a67e6ca8cbf86024d5ca7b65e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.3 MB (856299175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc92e52357c6f767f80852c09d9b568acadab146a67faa46208836e38d51c69`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731802779598cf7272bb9cef7e2800c1c23d8541bad7fb5ccf74d8c9f6522078`  
		Last Modified: Wed, 13 Aug 2025 03:33:46 GMT  
		Size: 324.9 MB (324927868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04f9e55075945fb216ac24ba38aa27d01d853c7cb112c42637bcde5374253e`  
		Last Modified: Wed, 13 Aug 2025 00:52:59 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764786f8bedab433611ce3eed3ab8ca937cc334dc5b2cfb422bba7c0003e5fa6`  
		Last Modified: Fri, 15 Aug 2025 05:14:35 GMT  
		Size: 317.0 MB (317024654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c817a9d31afafc3c56eaf98bfe781123b3a25a288aaf29f10b020a893fccb244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19504233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d13d87f8b3b34458959ef8a332ce2d887cda17f73c05a513761bc90a819daf2`

```dockerfile
```

-	Layers:
	-	`sha256:15f7d276aeb14a7b372a20fca8e14896e4c04242e240b4a497aae14878b70932`  
		Last Modified: Wed, 13 Aug 2025 17:10:50 GMT  
		Size: 19.5 MB (19493619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4249e549464c116aba4acdc187aa6e55e3375fc892fa00d58d918165605b05a6`  
		Last Modified: Wed, 13 Aug 2025 17:10:51 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:3d8dbf92e931b7c90d12a5184980f2e927ed5e800b6e9bb20687cf40a399eacd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:85f5fbdaf6f30cdc645d974d89794b03841f56f397d3876a4587509bdf34feff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 MB (655305795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a51582bebaa9557d0f1f41c7d4a30ef0d7587ad47e72e1fa1f9a128ddb263b0`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ea3914807494138e249f2607629b22a381a1b7d716facfc68533af3990be4`  
		Last Modified: Tue, 02 Sep 2025 01:14:11 GMT  
		Size: 113.7 MB (113737025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8c22e4082c88bd888a00ecc58094a39c58b04e3a386ae04a860326db9531a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b161b5b4bd3f03f36aec2b35a4a7c577180233a4186d862b39582626cdb5051`

```dockerfile
```

-	Layers:
	-	`sha256:645b6f52c32358b6976b8d68fbba9c451ec54124d18247a2bf6e184a5c7bc279`  
		Last Modified: Tue, 02 Sep 2025 05:10:22 GMT  
		Size: 10.3 MB (10287450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023104764c24270316e263757fabf6c3ed2f2fd288f557b81350c274da4d8ea0`  
		Last Modified: Tue, 02 Sep 2025 05:10:23 GMT  
		Size: 11.0 KB (11000 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cf81cbba1b828e95f69b9cf4eba4795e6614b4801053f1d5cf26a21524cb8c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.6 MB (647559229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b7b5a7eb196134f9ef8b39a98c15533db165df3fe0c75714bb2f2a6166c3fe`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731802779598cf7272bb9cef7e2800c1c23d8541bad7fb5ccf74d8c9f6522078`  
		Last Modified: Wed, 13 Aug 2025 03:33:46 GMT  
		Size: 324.9 MB (324927868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04f9e55075945fb216ac24ba38aa27d01d853c7cb112c42637bcde5374253e`  
		Last Modified: Wed, 13 Aug 2025 00:52:59 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa231ee19d55f9a9c86702103714e73e65683284b4cc99158af045f670026809`  
		Last Modified: Wed, 13 Aug 2025 15:10:13 GMT  
		Size: 108.3 MB (108284708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e1d81cf15b4098a7c922f9090aa81c9ed85e19a393cb4277b7bc94c04f354720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4a7b7ed83f530e23c41d53a0a5ce5e5cd1e24c7695a80ec9087ef95954d66b`

```dockerfile
```

-	Layers:
	-	`sha256:850bb7930a7b5e05a73ed4db954e6ace99f0db0fa912912e31d7e37f52a23eb8`  
		Last Modified: Wed, 13 Aug 2025 17:10:24 GMT  
		Size: 10.3 MB (10281821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c25893bac0e55e4e3d34a87c1d934ccdbc1eb3219bf5bc4c028c925b300071c`  
		Last Modified: Wed, 13 Aug 2025 17:10:25 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:fbfa771aaabd423d3633c3031cb699b46d8428a01d8527e2c91f9b426de4625c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a159c642e0edb83f6793dc5a35791ad4314fa026897f509e155fef28a048f74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.9 MB (860891789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226f23b8393e6df9eb264cda0956030ee84a9b8e692a6e5ec644fa5040d740d7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282fd6eec70c90644a2b089661ad06514afec2fd8ff2f85d139953e689464b04`  
		Last Modified: Tue, 02 Sep 2025 01:14:29 GMT  
		Size: 319.3 MB (319323019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0e7c2cbd80863ee9e09ed409bc36f1c51bdfcf5994c015412e9d8e93dd13c14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18493679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aec9db907956b221d9f16c848664af31fa560a4e77117f4f87bb6c00eb1ed70`

```dockerfile
```

-	Layers:
	-	`sha256:eec5056d7aea42c4672feda8807e9442e0dad4ddf21aa4d3d4d0295a34cba268`  
		Last Modified: Tue, 02 Sep 2025 05:10:27 GMT  
		Size: 18.5 MB (18482997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16f18fe0993540b229092cdd9bf797b76697457689af6a4934dd1c726ac3a1a`  
		Last Modified: Tue, 02 Sep 2025 05:10:29 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:342235f875a17c5dbf6cbe180b7f5b028b56dd366ee3f3ca37a27e8ae9599670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.8 MB (841770703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5966b3897911e6e2d2ff06c37b5b8d92adf55a93b2a021734dbe0b2bffc138`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
USER root
# Wed, 28 May 2025 20:13:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV R_HOME=/usr/lib/R
# Wed, 28 May 2025 20:13:50 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731802779598cf7272bb9cef7e2800c1c23d8541bad7fb5ccf74d8c9f6522078`  
		Last Modified: Wed, 13 Aug 2025 03:33:46 GMT  
		Size: 324.9 MB (324927868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04f9e55075945fb216ac24ba38aa27d01d853c7cb112c42637bcde5374253e`  
		Last Modified: Wed, 13 Aug 2025 00:52:59 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb59d18c9a4dc285d039ed495ea1d8c3d6b0e47128cc8e4bbfee368ae095b69`  
		Last Modified: Wed, 13 Aug 2025 18:18:07 GMT  
		Size: 302.5 MB (302496182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a3009854cd8a810de040c966b51fbafebef2ddd9b6765faa0bd6b74d0c4b0f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18458223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac790ab4b6551a44ffe6778be85c54ed6adbe6a94f59d4d520982473f4e1bce`

```dockerfile
```

-	Layers:
	-	`sha256:c10c3b83c19b5588430b31578214e7e32b6af075750bea0efa306a468f808584`  
		Last Modified: Wed, 13 Aug 2025 17:10:39 GMT  
		Size: 18.4 MB (18447462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680bda6cf6f547c6dca572688c8cac1451a41232a10e5fb00a7d49c27407f730`  
		Last Modified: Wed, 13 Aug 2025 17:10:40 GMT  
		Size: 10.8 KB (10761 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.6-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:4d54eb6add0ec3ce3d8c0cc326d14589e5d55321502aab6c483ff18dcf4a3cb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.6-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:db32bad2a16f15a2f4d51100aca2cb08d67ad9682beca65607196b031b79baca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.6 MB (541568770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dabd25618787909e5d4ccbed0c717bcce1abc7372a0404e4351a75dc63174a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ce00fff7ade76c921fba335b5a9b4d82dd0f6a9d664817bd34b76d50bc657`  
		Last Modified: Tue, 02 Sep 2025 01:12:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d0acd1904b3e85e4cb58bc86399522ae8feb343a06df9ea1cb64330edc2c7`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3784acf8b7504851c443452be37e8c508f3e60dca14016d83857dc809b833`  
		Last Modified: Tue, 02 Sep 2025 01:12:27 GMT  
		Size: 324.9 MB (324927916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816df8334bc4a0404a332f3d817eb57fad023d14a5157de32791feef4f168bd6`  
		Last Modified: Tue, 02 Sep 2025 01:12:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b569680a3cff0fb65b79e21eb214f0fc17af2747492f44722be863418ac8cddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4837197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a3a1e5eb6f957ffa9d8d775509c61f71c7466942bbbd107498f6e56c194af4`

```dockerfile
```

-	Layers:
	-	`sha256:928c93cee62977a06799d6f5a76031f5a616ccadde6cc64d77314ae784db5c1c`  
		Last Modified: Tue, 02 Sep 2025 02:10:22 GMT  
		Size: 4.8 MB (4814331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3914489c55a90bbd8ee683a1a81d1ba0d534eef65f6f4105788be80119557d3`  
		Last Modified: Tue, 02 Sep 2025 02:10:23 GMT  
		Size: 22.9 KB (22866 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.6-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9da24026a3496e7f74330c5c81dfb3c2b244a5d7010e984457d8d97517eeec1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.3 MB (539277013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4143fd6ca94b4b3e91e01b296c1e00bd2f7d90efed50bcadf712c3296feb61c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 28 May 2025 20:13:50 GMT
ARG RELEASE
# Wed, 28 May 2025 20:13:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 20:13:50 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 20:13:50 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Wed, 28 May 2025 20:13:50 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 May 2025 20:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 20:13:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 May 2025 20:13:50 GMT
CMD ["jshell"]
# Wed, 28 May 2025 20:13:50 GMT
ARG spark_uid=185
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.6/spark-3.5.6-bin-hadoop3.tgz.asc GPG_KEY=0FE4571297AB84440673665669600C8338F65970
# Wed, 28 May 2025 20:13:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Wed, 28 May 2025 20:13:50 GMT
COPY entrypoint.sh /opt/ # buildkit
# Wed, 28 May 2025 20:13:50 GMT
ENV SPARK_HOME=/opt/spark
# Wed, 28 May 2025 20:13:50 GMT
WORKDIR /opt/spark/work-dir
# Wed, 28 May 2025 20:13:50 GMT
USER spark
# Wed, 28 May 2025 20:13:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2d1bf87820e36d53f26b7cd674768abf44232e1496f26c39a0b8e513d4e8c`  
		Last Modified: Tue, 02 Sep 2025 01:03:42 GMT  
		Size: 22.1 MB (22075014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a562fdfee59db98ef10f59acb342e37698d1891b3f4608dab55a20e25c85093`  
		Last Modified: Tue, 02 Sep 2025 03:15:28 GMT  
		Size: 143.6 MB (143550948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6953a5f4a054b79b249f8f3bbd1be1a1c4f1873fa3be3cd054e0029f8a71087`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fd4799efced03c22e41b0e5ae8ece8022f4df5662e5b25352d453d8783892`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626a4a66c5c6a6908a2c062f2cc8209efbaeb14315a158a9e21a98144b4cad1d`  
		Last Modified: Tue, 02 Sep 2025 07:00:42 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d242d7a7a5680644c29be3300ebdcec7562015013b56c80b6ac0d7dc5142111`  
		Last Modified: Tue, 02 Sep 2025 07:00:45 GMT  
		Size: 21.4 MB (21355649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19ff606250fc7d01738c60958cd243dcd9716526a0e4982d11c356820dac75`  
		Last Modified: Tue, 02 Sep 2025 07:01:06 GMT  
		Size: 324.9 MB (324927897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5848a124ab4eae484508105150ee9efa4bfee3f1ea478f8a454730d9bf129d8`  
		Last Modified: Tue, 02 Sep 2025 07:01:00 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.6-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0feaca3fa282bcb0a56958abadd2609ee1890c7d8e18737de154ac758e9f33c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb89d26291e2fdc9e892701bd6f8b95c045459aa7070cf8de315fe826d772ba6`

```dockerfile
```

-	Layers:
	-	`sha256:61814823bc481c7c4f26c3948a16c3ab556d5da4b380659ee28c6765209eee99`  
		Last Modified: Tue, 02 Sep 2025 08:10:27 GMT  
		Size: 4.9 MB (4909831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17110d023b3bfa87742dfba1e6587a5396a0d4fd4e671606f1d9198a24f21f9b`  
		Last Modified: Tue, 02 Sep 2025 08:10:28 GMT  
		Size: 23.0 KB (22976 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0`

```console
$ docker pull spark@sha256:691da856a4850e805e9f8159b561f73563e61177aa93cc704784ffec6b72f2b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0` - linux; amd64

```console
$ docker pull spark@sha256:d5bce90d34c2e1a7bf7db379ad4d1860d6767cfb44b1b0f0c0d2c44a3c6d358d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.0 MB (771981589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251d8601d5996fa44b9dd7caf9e40d5172397d205e6ce7231716048b7256a1f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bccd088697078423b39d9fa3fee2b0bd81c6054963ea8f75e9a32f534522df7`  
		Last Modified: Tue, 02 Sep 2025 01:14:18 GMT  
		Size: 113.7 MB (113737217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0` - unknown; unknown

```console
$ docker pull spark@sha256:ee2807454b1a876d2f570ccef8f445803205fe8a54fda77946af9920a9987095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10424557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd094fdba819db96f2fe680c2724cf0d4ba76b295760e4b344e65bf55feefd`

```dockerfile
```

-	Layers:
	-	`sha256:c7042d9867d51a6fc47987283bfab4ce47ea55672da6750f3706ae7693ced1bf`  
		Last Modified: Tue, 02 Sep 2025 05:10:44 GMT  
		Size: 10.4 MB (10413273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f8e54b05e474c5554173813d6e78a0c7823b8566776bc400b928e484289113`  
		Last Modified: Tue, 02 Sep 2025 05:10:45 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:c53ce7d96abe93941ee368817d75458a8f043c8900b237b2b8e3eab326792aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.2 MB (764234819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3328874d1663502e1ebcfa2b191efac9ee2f242f0f52ace5356b294e52abd0b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df465001054084ae59e670d1a7dacd9337d9c52ebe59b603a1e7540ddf1796da`  
		Last Modified: Wed, 13 Aug 2025 17:31:33 GMT  
		Size: 108.3 MB (108284696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0` - unknown; unknown

```console
$ docker pull spark@sha256:1895afa3ea75c05896135466e4729dc3d6aa6212fa6bbe557f0606621bab45df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10419043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa26ee4060b7fb8e8c0dc774c9ec08d0a7f0a95c4826522763e07b84452cf83b`

```dockerfile
```

-	Layers:
	-	`sha256:535a6f5dd2b67426cafcea76ca9939215aad15cb8993c29ad7d173ff2da978a8`  
		Last Modified: Wed, 13 Aug 2025 17:10:47 GMT  
		Size: 10.4 MB (10407656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b46aa45a8d57d8e0dfd935a9508a8b1e744e976390512a3c45d2f314893fd24`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 11.4 KB (11387 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-java21`

```console
$ docker pull spark@sha256:5409c7039f5672f193124cf4c3a94a1136850beb7e21748114a276c94ac9b2ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-java21` - linux; amd64

```console
$ docker pull spark@sha256:35af73a453d003db92c648d147d45a8b5253d846d9bd7b4fef18c3593bda44ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.1 MB (785081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310540296d12c1d2c3dcbeb1b50524f67883de2a71dc23f2e98d89a7677e09e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f094bb0f37e2860636270e58dbde64c8b2d7cf105eee9c889c43aa9aef4751c1`  
		Last Modified: Tue, 02 Sep 2025 01:14:22 GMT  
		Size: 113.7 MB (113736996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21` - unknown; unknown

```console
$ docker pull spark@sha256:8032964da95fea1053c92cf3dc4de4510ee9b796457dfa442b9cc976ebb30feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccf5eaccb8500e96cc38cb3e11dc6e7a3a3e797ea4dceb056ae1c003dd1bad`

```dockerfile
```

-	Layers:
	-	`sha256:b687018df3865b0fb32fc8b0b515548542e29d66199e7467212296249e137d2b`  
		Last Modified: Tue, 02 Sep 2025 05:10:47 GMT  
		Size: 10.4 MB (10416685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89da161ab1aa927a0068b41e716ae165bc5ff1461c723888aca1155931d2b921`  
		Last Modified: Tue, 02 Sep 2025 05:10:48 GMT  
		Size: 11.6 KB (11593 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-java21` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:30d8b5f2ec937010906cdc74839f17fdd9ee07d9286ac80a8b3b367ef039b725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776772693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a75554b5ba2d05771ffcc4b3b09a9b72826fd1b5e94be01c6b89b27076a06f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcfd4e0cba096b00bb08cd252b3e87a526d52f54cd02deb630a45ffe3f30754`  
		Last Modified: Wed, 13 Aug 2025 17:30:36 GMT  
		Size: 108.3 MB (108284844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21` - unknown; unknown

```console
$ docker pull spark@sha256:1d472bfd54095eded3e79b9e9277b19800d8168149e9a0e2e5f441d587515cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10422789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc0518a8998734cff1e09033310f47961d83d374fa97f2ebad854ade1831798`

```dockerfile
```

-	Layers:
	-	`sha256:5a414e511c6387bc253fc6cdf57519de1387038b1c69f33657e15febafa96050`  
		Last Modified: Wed, 13 Aug 2025 17:10:51 GMT  
		Size: 10.4 MB (10411080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cca7556260799ff49d80fc2b3bb9f7428b57f8fb2da62558f0341d1383b65a3`  
		Last Modified: Wed, 13 Aug 2025 17:10:52 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-java21-python3`

```console
$ docker pull spark@sha256:5409c7039f5672f193124cf4c3a94a1136850beb7e21748114a276c94ac9b2ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-java21-python3` - linux; amd64

```console
$ docker pull spark@sha256:35af73a453d003db92c648d147d45a8b5253d846d9bd7b4fef18c3593bda44ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.1 MB (785081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310540296d12c1d2c3dcbeb1b50524f67883de2a71dc23f2e98d89a7677e09e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f094bb0f37e2860636270e58dbde64c8b2d7cf105eee9c889c43aa9aef4751c1`  
		Last Modified: Tue, 02 Sep 2025 01:14:22 GMT  
		Size: 113.7 MB (113736996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:8032964da95fea1053c92cf3dc4de4510ee9b796457dfa442b9cc976ebb30feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccf5eaccb8500e96cc38cb3e11dc6e7a3a3e797ea4dceb056ae1c003dd1bad`

```dockerfile
```

-	Layers:
	-	`sha256:b687018df3865b0fb32fc8b0b515548542e29d66199e7467212296249e137d2b`  
		Last Modified: Tue, 02 Sep 2025 05:10:47 GMT  
		Size: 10.4 MB (10416685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89da161ab1aa927a0068b41e716ae165bc5ff1461c723888aca1155931d2b921`  
		Last Modified: Tue, 02 Sep 2025 05:10:48 GMT  
		Size: 11.6 KB (11593 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-java21-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:30d8b5f2ec937010906cdc74839f17fdd9ee07d9286ac80a8b3b367ef039b725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776772693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a75554b5ba2d05771ffcc4b3b09a9b72826fd1b5e94be01c6b89b27076a06f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcfd4e0cba096b00bb08cd252b3e87a526d52f54cd02deb630a45ffe3f30754`  
		Last Modified: Wed, 13 Aug 2025 17:30:36 GMT  
		Size: 108.3 MB (108284844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:1d472bfd54095eded3e79b9e9277b19800d8168149e9a0e2e5f441d587515cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10422789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc0518a8998734cff1e09033310f47961d83d374fa97f2ebad854ade1831798`

```dockerfile
```

-	Layers:
	-	`sha256:5a414e511c6387bc253fc6cdf57519de1387038b1c69f33657e15febafa96050`  
		Last Modified: Wed, 13 Aug 2025 17:10:51 GMT  
		Size: 10.4 MB (10411080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cca7556260799ff49d80fc2b3bb9f7428b57f8fb2da62558f0341d1383b65a3`  
		Last Modified: Wed, 13 Aug 2025 17:10:52 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-java21-r`

```console
$ docker pull spark@sha256:0f61924de409cc52affd076be53667c4e0d39a0a55f793b26194e60fba0603d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-java21-r` - linux; amd64

```console
$ docker pull spark@sha256:dc660ef3300ba3fb9c68f8bbd390da582be86768d17c29c97480cc3a8d50308a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.7 MB (990666981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171317fcd8a15f98ad3b6e6732e736329c3b6015781462c299e0ca182fe2d5e6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ba0b36700883852dde418b67edc917790c4d1323a2c6097405f42c4183ce5`  
		Last Modified: Tue, 02 Sep 2025 01:14:25 GMT  
		Size: 319.3 MB (319322183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:931916cfecd0dda772b00f70e8239dbe11b2e2e2da0b0c3f9e3e622e06f16bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18622319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1292157ff91f065a1401f832025520d619ad3dc8dce083a1e94973119f1826c8`

```dockerfile
```

-	Layers:
	-	`sha256:46904661233d5b817a7ebb1571690592b4b3e44542eda45a12d6d18f44a34adf`  
		Last Modified: Tue, 02 Sep 2025 05:10:55 GMT  
		Size: 18.6 MB (18611638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178662f90af41b6e4c1ec7438742923cbdfeffcafd01bbd8d8e53bd9703a70d4`  
		Last Modified: Tue, 02 Sep 2025 05:10:56 GMT  
		Size: 10.7 KB (10681 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-java21-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:941369ba4b6a1ada47955f3c04cab67404a68aaa86200cda68044f3fa0a48fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **971.0 MB (970984137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e86beff05bfb55b05c865da56a0654c93c09d95215337ffd57b18539483059`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fe9b72f1eeec213e51dc0276989e68068929c0a6ae0a0acebb2d2a83c22e`  
		Last Modified: Fri, 15 Aug 2025 05:14:36 GMT  
		Size: 302.5 MB (302496288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:9ddbf4950b5231264cd8542dbac5253e249383cf4970871be2acb187d924180e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18586864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8419f7e7a37e3d65eb37ce24154e3e080ae6a4e54f93af7808a3048e19004a4c`

```dockerfile
```

-	Layers:
	-	`sha256:9e748571c49a8206b30db6fe2c18b9e644bca66c367a89bc81913d0cb3662300`  
		Last Modified: Wed, 13 Aug 2025 17:11:08 GMT  
		Size: 18.6 MB (18576103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a33b380f81b62f164b48510ac4b797401f440dbde74acc6cf9830cab30be44c1`  
		Last Modified: Wed, 13 Aug 2025 17:11:09 GMT  
		Size: 10.8 KB (10761 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-java21-scala`

```console
$ docker pull spark@sha256:e2a820d15e0e00c7fe0e514a8aaca8ca95e9ac74b14ddbfebe9dc49ea6f8d4de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-java21-scala` - linux; amd64

```console
$ docker pull spark@sha256:66ea345a7c41b1bb45ce918e0e06764cc6151234eab7f3c522d39c1b8bdf4f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.3 MB (671344798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6275d127295b16c8215aba2e363a2574ca712040b8f3d059867e7b9be014a6f2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:a392c1972301c29d6cdfc519c28b0f22c6bfd2015d2dbab6dc9de11db06ad20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b338dbd2d339e404aea99449bbb429b04c5c6a8562883e20748a45ea497f3900`

```dockerfile
```

-	Layers:
	-	`sha256:8282f0351827b2281ac8c8e8d33ce7841d5ad71a995b244d853782b44c1e4ffc`  
		Last Modified: Tue, 02 Sep 2025 02:10:37 GMT  
		Size: 4.9 MB (4942972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c089a00e202b04369845dfd7deca3eb5421ae46d5e486ab7042ab6b87028d3dc`  
		Last Modified: Tue, 02 Sep 2025 02:10:38 GMT  
		Size: 22.9 KB (22863 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-java21-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5520dff09c6f84089a25f1ae5a711ac448769d4b7dbfc4dc2ed6286ffdc6eeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668490277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac089b9d8dbd728802d267970ac698817a4d97fc6d360672c967bb1543992a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2d1bf87820e36d53f26b7cd674768abf44232e1496f26c39a0b8e513d4e8c`  
		Last Modified: Tue, 02 Sep 2025 01:03:42 GMT  
		Size: 22.1 MB (22075014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff1d73afae4335a270591ef7c88aa60b4ecc7ac613f31fd49c20a3ad8dcab31`  
		Last Modified: Tue, 02 Sep 2025 03:19:07 GMT  
		Size: 156.1 MB (156088648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf0ef9945e728aa240386ce5491d5283ef22addc9850089ed350aa4dbf0a1dc`  
		Last Modified: Tue, 02 Sep 2025 01:05:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b647f909bb99678b70897a2ec6f8c6370788f632f9c519b5a573c07eef7dd19b`  
		Last Modified: Tue, 02 Sep 2025 01:05:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c16c4d601c5ddf934270bcdc8912d40b31468398ef01d3e68f2e28739abf00`  
		Last Modified: Tue, 02 Sep 2025 06:18:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453439ae78e36a742ada02fd737d263d0b8cc9b0d761b24bc31fe78b2dda5d43`  
		Last Modified: Tue, 02 Sep 2025 06:18:41 GMT  
		Size: 21.4 MB (21355689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6b7a0eb389156db9a5bd1278889aed3ba0dc3e34b32b90c187eb453134d29`  
		Last Modified: Tue, 02 Sep 2025 06:18:34 GMT  
		Size: 441.6 MB (441603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978df6ed235afca534c14be69117e4d2d3c5e84c5eec44d213ae0362ae734db5`  
		Last Modified: Tue, 02 Sep 2025 06:18:40 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:d6e48f23eb4ca990a6e374aa92e04a62954498877e0d0a2869e462c06d2a389f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5061445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559c08d504bf6877fb76e8826c4bc84cf5ee7cc7f1ec6b5a4f801e69b764f91a`

```dockerfile
```

-	Layers:
	-	`sha256:5f7c04c947de97e3b35e936f8ccbc17dfc29809eeb1ef874ddb44d0fbb5e6b55`  
		Last Modified: Tue, 02 Sep 2025 08:10:49 GMT  
		Size: 5.0 MB (5038472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0fe3dca8051b6174fd31ce3118993a841ba443114f5bddde2edbe0667e85e3`  
		Last Modified: Tue, 02 Sep 2025 08:10:50 GMT  
		Size: 23.0 KB (22973 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-python3`

```console
$ docker pull spark@sha256:691da856a4850e805e9f8159b561f73563e61177aa93cc704784ffec6b72f2b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-python3` - linux; amd64

```console
$ docker pull spark@sha256:d5bce90d34c2e1a7bf7db379ad4d1860d6767cfb44b1b0f0c0d2c44a3c6d358d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.0 MB (771981589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251d8601d5996fa44b9dd7caf9e40d5172397d205e6ce7231716048b7256a1f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bccd088697078423b39d9fa3fee2b0bd81c6054963ea8f75e9a32f534522df7`  
		Last Modified: Tue, 02 Sep 2025 01:14:18 GMT  
		Size: 113.7 MB (113737217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-python3` - unknown; unknown

```console
$ docker pull spark@sha256:ee2807454b1a876d2f570ccef8f445803205fe8a54fda77946af9920a9987095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10424557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd094fdba819db96f2fe680c2724cf0d4ba76b295760e4b344e65bf55feefd`

```dockerfile
```

-	Layers:
	-	`sha256:c7042d9867d51a6fc47987283bfab4ce47ea55672da6750f3706ae7693ced1bf`  
		Last Modified: Tue, 02 Sep 2025 05:10:44 GMT  
		Size: 10.4 MB (10413273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f8e54b05e474c5554173813d6e78a0c7823b8566776bc400b928e484289113`  
		Last Modified: Tue, 02 Sep 2025 05:10:45 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:c53ce7d96abe93941ee368817d75458a8f043c8900b237b2b8e3eab326792aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.2 MB (764234819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3328874d1663502e1ebcfa2b191efac9ee2f242f0f52ace5356b294e52abd0b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df465001054084ae59e670d1a7dacd9337d9c52ebe59b603a1e7540ddf1796da`  
		Last Modified: Wed, 13 Aug 2025 17:31:33 GMT  
		Size: 108.3 MB (108284696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-python3` - unknown; unknown

```console
$ docker pull spark@sha256:1895afa3ea75c05896135466e4729dc3d6aa6212fa6bbe557f0606621bab45df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10419043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa26ee4060b7fb8e8c0dc774c9ec08d0a7f0a95c4826522763e07b84452cf83b`

```dockerfile
```

-	Layers:
	-	`sha256:535a6f5dd2b67426cafcea76ca9939215aad15cb8993c29ad7d173ff2da978a8`  
		Last Modified: Wed, 13 Aug 2025 17:10:47 GMT  
		Size: 10.4 MB (10407656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b46aa45a8d57d8e0dfd935a9508a8b1e744e976390512a3c45d2f314893fd24`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 11.4 KB (11387 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-r`

```console
$ docker pull spark@sha256:afa432ca3c54f1ef1d865bbf24292f86ef92f0fa91527302db083cbd00d40639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-r` - linux; amd64

```console
$ docker pull spark@sha256:6c4ed92d67b04b6ff4bf46b5ac7e6f5181571cd391747cc6f5f77aa69d79850f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.6 MB (977566865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdafb5c36df361e533264ab6d20ada54a53c63851833bc35eeffd0108b9c752`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf63213fb3473f8fd12d5023d0d20539dfa4a1aaa67f0bf643628a8b64fafc77`  
		Last Modified: Tue, 02 Sep 2025 05:12:26 GMT  
		Size: 319.3 MB (319322493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-r` - unknown; unknown

```console
$ docker pull spark@sha256:2a0e3e8426ee0767050c77bcd36f73eed343efdb3c6e1011dda9f32a2fd667cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18619761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef66dcc5195557c3e72469fb46a24b6ef64b94668044de4c600b3c2b954d56`

```dockerfile
```

-	Layers:
	-	`sha256:8ae250c81b4cc244f501fe4859718a2f36a658d5b8b797225a4d97a0595b6499`  
		Last Modified: Tue, 02 Sep 2025 05:10:59 GMT  
		Size: 18.6 MB (18608808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c21776ba02312d1a6e2f7add42d3eaf083db5ef72ba5697e8edfed08874bf6b`  
		Last Modified: Tue, 02 Sep 2025 05:11:00 GMT  
		Size: 11.0 KB (10953 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:667a772a00958d8e117c3b24919f7cc7b5c958523a13df9300fa0a8bdc0fac9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.4 MB (958446537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395efdce75be75403f3d906483ea0c9100f8f45eaac66f2234134c875aa811e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff980efb92480747419cb3d7eb2f4b13104a7a47a5f786a208d83bf5ab3b34b`  
		Last Modified: Fri, 15 Aug 2025 05:14:32 GMT  
		Size: 302.5 MB (302496414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-r` - unknown; unknown

```console
$ docker pull spark@sha256:06f74422141527eb6d8c60b4b43a953ffd27295b06c60d41e7953679e5d80d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18584330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36a1584d19be6a35f69ca95ac856fd42b1bbb3ade7588812e47f7468b1298b4`

```dockerfile
```

-	Layers:
	-	`sha256:7712511fdb3d9aceff9d18cf6081de00628ea8ec9b148fea7fd99781764a03f9`  
		Last Modified: Wed, 13 Aug 2025 17:11:09 GMT  
		Size: 18.6 MB (18573285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c3d51023fb23665200279ef01f8b078d56e15a2111527bf53cd2b2b43cf9cb`  
		Last Modified: Wed, 13 Aug 2025 17:11:10 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala`

```console
$ docker pull spark@sha256:bec33899f38b9cce395dedac861830baa285450824cf644a0d555546f542236b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala` - linux; amd64

```console
$ docker pull spark@sha256:fea501e7d8b625863d6f5cfc0f67224e4c6985c61aeaf5fb9a030fe16fb67e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658244372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6133148f409294c1c0738efad15af0f60d247c5c72b0d1fddd90ee6c3c862b59`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala` - unknown; unknown

```console
$ docker pull spark@sha256:65c9ee7e5bdaf26508ac195cb5770c983bbc9130dffb6a92442d3c8279be5e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423446de67d5937db6d9eea2b5c220fedbe122b44be4819ba15cc615ff02f5ce`

```dockerfile
```

-	Layers:
	-	`sha256:a87a7828b0178c768ac1706ac74163e1c5953d8d2c926ce5786b5b811142e3aa`  
		Last Modified: Tue, 02 Sep 2025 02:10:44 GMT  
		Size: 4.9 MB (4940150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8ef5c5b8343cb1acab240fccc83a8c4947624464aac2373e9ef61cb5d1c4d5`  
		Last Modified: Tue, 02 Sep 2025 02:10:45 GMT  
		Size: 23.1 KB (23146 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e30a9e898cd983f139697e0a051635afc3549a4aee0c75b4b92399f7ccea3fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.0 MB (655952508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae00545b1b4b856cba7d370b87987cc43bd80aed1a8f7248a060858b129250ff`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2d1bf87820e36d53f26b7cd674768abf44232e1496f26c39a0b8e513d4e8c`  
		Last Modified: Tue, 02 Sep 2025 01:03:42 GMT  
		Size: 22.1 MB (22075014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a562fdfee59db98ef10f59acb342e37698d1891b3f4608dab55a20e25c85093`  
		Last Modified: Tue, 02 Sep 2025 03:15:28 GMT  
		Size: 143.6 MB (143550948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6953a5f4a054b79b249f8f3bbd1be1a1c4f1873fa3be3cd054e0029f8a71087`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fd4799efced03c22e41b0e5ae8ece8022f4df5662e5b25352d453d8783892`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626a4a66c5c6a6908a2c062f2cc8209efbaeb14315a158a9e21a98144b4cad1d`  
		Last Modified: Tue, 02 Sep 2025 07:00:42 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d242d7a7a5680644c29be3300ebdcec7562015013b56c80b6ac0d7dc5142111`  
		Last Modified: Tue, 02 Sep 2025 07:00:45 GMT  
		Size: 21.4 MB (21355649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c3598999f7b5e24b38b389f12edfed3da513cd86ba5aff282b7636e2bd9ac`  
		Last Modified: Tue, 02 Sep 2025 06:41:54 GMT  
		Size: 441.6 MB (441603392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a58f7daf2c27e8ef2a2572ea196fe27b166f47a81b3db0cabe308e8e654086`  
		Last Modified: Tue, 02 Sep 2025 07:15:57 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala` - unknown; unknown

```console
$ docker pull spark@sha256:02b43f83a3ed41c6016d7eac27ee2a0de8ad4f2cb7c447bf425a12e4b9ca3d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e002a1359bc96383a2c4d7775e6237a6c69523b36a910b4eb80018bd35a6197`

```dockerfile
```

-	Layers:
	-	`sha256:d3ed6730efabbaf7fb55861864901f5af99138771d2dd9849b9ba3842d7ad9ba`  
		Last Modified: Tue, 02 Sep 2025 08:10:45 GMT  
		Size: 5.0 MB (5035662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3295631c72c3b889ca63542528f34cd8ae86bb3ba1cf23cc70746f8a1388e884`  
		Last Modified: Tue, 02 Sep 2025 08:10:46 GMT  
		Size: 23.3 KB (23268 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:d1a61c9a70f8f530b26de78338a9d5ed9ede5a1d934d2e2a4bda3ce57a60ab86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:b59d0a76550bc73fb072ca1d47ce3dd4aa371dbdf15c5ea34a6c6f26be2902e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.2 MB (992238521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd124f6e9488848f2181e4c16399984fddfa399c2f08a97de7285c8d7ba421e3`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d593235e1b72b88a0c57c345c58f7927162ea9e44588504d5fc59ff4c29e9f35`  
		Last Modified: Tue, 02 Sep 2025 01:14:11 GMT  
		Size: 334.0 MB (333994149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b09c18efdd53699a1a43c08d396a3ed001b55c094e987f77d1f5b5c7a133415b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19665227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44911c5d8714cf07af9d1af03b3643158fa7aa86792b11ab573df809d086f2`

```dockerfile
```

-	Layers:
	-	`sha256:96e7662c8444c025570b53f08003f3ab2950242515a900a54187d6593795d63c`  
		Last Modified: Tue, 02 Sep 2025 05:11:07 GMT  
		Size: 19.7 MB (19654681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043ab17067cde06ab76d2e0582b53981aa324e0b4d202087c156db84aa91167b`  
		Last Modified: Tue, 02 Sep 2025 05:11:08 GMT  
		Size: 10.5 KB (10546 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7f10e239ba6641b270c8ddf8ec45174ba3487071562d57f7d04168c182182680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.0 MB (972974554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f012389d5c6b0399620f4fcaa5e3d472c3cf92209731d805dca3d6ee3e6c23a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622464772379d193857c9496349fea42c56b52ac8d17af2b3df1b0b0ee400d90`  
		Last Modified: Fri, 15 Aug 2025 05:14:27 GMT  
		Size: 317.0 MB (317024431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:3a9e77da15761687cf034d6f6e13a1695b0b0248e30ff22935658d8530c79f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19629772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a588eeae11562a3db2d205b04b7e63b12e4d1f977317644254fb58226aa4eb`

```dockerfile
```

-	Layers:
	-	`sha256:2ff6a632dbbcd9fe30a57df4b10d11e4885ac18940da04dd095f32a31daa8fe7`  
		Last Modified: Wed, 13 Aug 2025 17:11:22 GMT  
		Size: 19.6 MB (19619158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908a1c06f58b2e321f613887e51384b2ac65174412afd42f6261bac7387ace6b`  
		Last Modified: Wed, 13 Aug 2025 17:11:23 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:691da856a4850e805e9f8159b561f73563e61177aa93cc704784ffec6b72f2b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:d5bce90d34c2e1a7bf7db379ad4d1860d6767cfb44b1b0f0c0d2c44a3c6d358d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.0 MB (771981589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251d8601d5996fa44b9dd7caf9e40d5172397d205e6ce7231716048b7256a1f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bccd088697078423b39d9fa3fee2b0bd81c6054963ea8f75e9a32f534522df7`  
		Last Modified: Tue, 02 Sep 2025 01:14:18 GMT  
		Size: 113.7 MB (113737217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:ee2807454b1a876d2f570ccef8f445803205fe8a54fda77946af9920a9987095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10424557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd094fdba819db96f2fe680c2724cf0d4ba76b295760e4b344e65bf55feefd`

```dockerfile
```

-	Layers:
	-	`sha256:c7042d9867d51a6fc47987283bfab4ce47ea55672da6750f3706ae7693ced1bf`  
		Last Modified: Tue, 02 Sep 2025 05:10:44 GMT  
		Size: 10.4 MB (10413273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f8e54b05e474c5554173813d6e78a0c7823b8566776bc400b928e484289113`  
		Last Modified: Tue, 02 Sep 2025 05:10:45 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:c53ce7d96abe93941ee368817d75458a8f043c8900b237b2b8e3eab326792aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.2 MB (764234819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3328874d1663502e1ebcfa2b191efac9ee2f242f0f52ace5356b294e52abd0b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df465001054084ae59e670d1a7dacd9337d9c52ebe59b603a1e7540ddf1796da`  
		Last Modified: Wed, 13 Aug 2025 17:31:33 GMT  
		Size: 108.3 MB (108284696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:1895afa3ea75c05896135466e4729dc3d6aa6212fa6bbe557f0606621bab45df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10419043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa26ee4060b7fb8e8c0dc774c9ec08d0a7f0a95c4826522763e07b84452cf83b`

```dockerfile
```

-	Layers:
	-	`sha256:535a6f5dd2b67426cafcea76ca9939215aad15cb8993c29ad7d173ff2da978a8`  
		Last Modified: Wed, 13 Aug 2025 17:10:47 GMT  
		Size: 10.4 MB (10407656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b46aa45a8d57d8e0dfd935a9508a8b1e744e976390512a3c45d2f314893fd24`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 11.4 KB (11387 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java17-r-ubuntu`

```console
$ docker pull spark@sha256:afa432ca3c54f1ef1d865bbf24292f86ef92f0fa91527302db083cbd00d40639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:6c4ed92d67b04b6ff4bf46b5ac7e6f5181571cd391747cc6f5f77aa69d79850f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.6 MB (977566865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdafb5c36df361e533264ab6d20ada54a53c63851833bc35eeffd0108b9c752`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf63213fb3473f8fd12d5023d0d20539dfa4a1aaa67f0bf643628a8b64fafc77`  
		Last Modified: Tue, 02 Sep 2025 05:12:26 GMT  
		Size: 319.3 MB (319322493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2a0e3e8426ee0767050c77bcd36f73eed343efdb3c6e1011dda9f32a2fd667cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18619761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef66dcc5195557c3e72469fb46a24b6ef64b94668044de4c600b3c2b954d56`

```dockerfile
```

-	Layers:
	-	`sha256:8ae250c81b4cc244f501fe4859718a2f36a658d5b8b797225a4d97a0595b6499`  
		Last Modified: Tue, 02 Sep 2025 05:10:59 GMT  
		Size: 18.6 MB (18608808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c21776ba02312d1a6e2f7add42d3eaf083db5ef72ba5697e8edfed08874bf6b`  
		Last Modified: Tue, 02 Sep 2025 05:11:00 GMT  
		Size: 11.0 KB (10953 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:667a772a00958d8e117c3b24919f7cc7b5c958523a13df9300fa0a8bdc0fac9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.4 MB (958446537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395efdce75be75403f3d906483ea0c9100f8f45eaac66f2234134c875aa811e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff980efb92480747419cb3d7eb2f4b13104a7a47a5f786a208d83bf5ab3b34b`  
		Last Modified: Fri, 15 Aug 2025 05:14:32 GMT  
		Size: 302.5 MB (302496414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:06f74422141527eb6d8c60b4b43a953ffd27295b06c60d41e7953679e5d80d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18584330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36a1584d19be6a35f69ca95ac856fd42b1bbb3ade7588812e47f7468b1298b4`

```dockerfile
```

-	Layers:
	-	`sha256:7712511fdb3d9aceff9d18cf6081de00628ea8ec9b148fea7fd99781764a03f9`  
		Last Modified: Wed, 13 Aug 2025 17:11:09 GMT  
		Size: 18.6 MB (18573285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c3d51023fb23665200279ef01f8b078d56e15a2111527bf53cd2b2b43cf9cb`  
		Last Modified: Wed, 13 Aug 2025 17:11:10 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java17-ubuntu`

```console
$ docker pull spark@sha256:bec33899f38b9cce395dedac861830baa285450824cf644a0d555546f542236b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:fea501e7d8b625863d6f5cfc0f67224e4c6985c61aeaf5fb9a030fe16fb67e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658244372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6133148f409294c1c0738efad15af0f60d247c5c72b0d1fddd90ee6c3c862b59`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:65c9ee7e5bdaf26508ac195cb5770c983bbc9130dffb6a92442d3c8279be5e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423446de67d5937db6d9eea2b5c220fedbe122b44be4819ba15cc615ff02f5ce`

```dockerfile
```

-	Layers:
	-	`sha256:a87a7828b0178c768ac1706ac74163e1c5953d8d2c926ce5786b5b811142e3aa`  
		Last Modified: Tue, 02 Sep 2025 02:10:44 GMT  
		Size: 4.9 MB (4940150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8ef5c5b8343cb1acab240fccc83a8c4947624464aac2373e9ef61cb5d1c4d5`  
		Last Modified: Tue, 02 Sep 2025 02:10:45 GMT  
		Size: 23.1 KB (23146 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e30a9e898cd983f139697e0a051635afc3549a4aee0c75b4b92399f7ccea3fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.0 MB (655952508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae00545b1b4b856cba7d370b87987cc43bd80aed1a8f7248a060858b129250ff`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2d1bf87820e36d53f26b7cd674768abf44232e1496f26c39a0b8e513d4e8c`  
		Last Modified: Tue, 02 Sep 2025 01:03:42 GMT  
		Size: 22.1 MB (22075014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a562fdfee59db98ef10f59acb342e37698d1891b3f4608dab55a20e25c85093`  
		Last Modified: Tue, 02 Sep 2025 03:15:28 GMT  
		Size: 143.6 MB (143550948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6953a5f4a054b79b249f8f3bbd1be1a1c4f1873fa3be3cd054e0029f8a71087`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fd4799efced03c22e41b0e5ae8ece8022f4df5662e5b25352d453d8783892`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626a4a66c5c6a6908a2c062f2cc8209efbaeb14315a158a9e21a98144b4cad1d`  
		Last Modified: Tue, 02 Sep 2025 07:00:42 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d242d7a7a5680644c29be3300ebdcec7562015013b56c80b6ac0d7dc5142111`  
		Last Modified: Tue, 02 Sep 2025 07:00:45 GMT  
		Size: 21.4 MB (21355649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c3598999f7b5e24b38b389f12edfed3da513cd86ba5aff282b7636e2bd9ac`  
		Last Modified: Tue, 02 Sep 2025 06:41:54 GMT  
		Size: 441.6 MB (441603392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a58f7daf2c27e8ef2a2572ea196fe27b166f47a81b3db0cabe308e8e654086`  
		Last Modified: Tue, 02 Sep 2025 07:15:57 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:02b43f83a3ed41c6016d7eac27ee2a0de8ad4f2cb7c447bf425a12e4b9ca3d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e002a1359bc96383a2c4d7775e6237a6c69523b36a910b4eb80018bd35a6197`

```dockerfile
```

-	Layers:
	-	`sha256:d3ed6730efabbaf7fb55861864901f5af99138771d2dd9849b9ba3842d7ad9ba`  
		Last Modified: Tue, 02 Sep 2025 08:10:45 GMT  
		Size: 5.0 MB (5035662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3295631c72c3b889ca63542528f34cd8ae86bb3ba1cf23cc70746f8a1388e884`  
		Last Modified: Tue, 02 Sep 2025 08:10:46 GMT  
		Size: 23.3 KB (23268 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java21-python3-r-ubuntu`

```console
$ docker pull spark@sha256:c5b488a583301673e4812ebc5c267dd432a44657b7c02589b58b05c5cad91804
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java21-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:4cf98b12e3a0d99aea1e00af2007097cb35aaa7e9d72568dedd60ca4d475f787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1005337455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8193f8835afe474ce46fcfa8a465e217f42d31c185e2aec1da367822448594`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb68950483bdea469991d785623c8894cd9bd339b2960426ec57b8f6779b429`  
		Last Modified: Tue, 02 Sep 2025 01:15:07 GMT  
		Size: 334.0 MB (333992657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c26586c21e9b1061b1189b99d3fb6bebe414a36505b3c4b3733b32d5bcfd3e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19668328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcfadb010b4f981bc9c7c31951a985ae057c64ce7def2379eb7fcc1b1cc9fd9`

```dockerfile
```

-	Layers:
	-	`sha256:33e7d04626c0f1ef4788ffa713fd4f76b38dcefdbf33fcc2b3d5b6af8dd4b996`  
		Last Modified: Tue, 02 Sep 2025 05:11:10 GMT  
		Size: 19.7 MB (19657783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69a5bc3a989f48252e7bd029c674783fc850caa00cf8d57027ca30980b8554b`  
		Last Modified: Tue, 02 Sep 2025 05:11:11 GMT  
		Size: 10.5 KB (10545 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java21-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a74fda83b7812e8faeb9973c49bb1c03407507e65cdc828a9f0564a861702e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.5 MB (985513669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1da3fe9cb3a7570fb0fa797b8f41bc7d2143f7ecba12310f5252bee7eecefe`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f9944586fef4ac3acc76f455008a7372eb13f39a1bbd0a5a83a0614eab882c`  
		Last Modified: Thu, 14 Aug 2025 10:12:50 GMT  
		Size: 317.0 MB (317025820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:193001dcf22452414dfa3c625c45c8e19cfd8c8e6c804dadda37250609825865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19632873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0772d337a6b0ffe73fd63fbd50288858fa93af88f50a12428dc8fb7d2c910eb0`

```dockerfile
```

-	Layers:
	-	`sha256:fd82f5ec146bbb2a4639f44294c3b1f6104c6ebe008ffeca0afd1eb0c64afe58`  
		Last Modified: Wed, 13 Aug 2025 17:11:27 GMT  
		Size: 19.6 MB (19622260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a932a98ff74054b89a4e5124d52349261be192ee8c5bccec70ec7d2e39887d5d`  
		Last Modified: Wed, 13 Aug 2025 17:11:28 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java21-python3-ubuntu`

```console
$ docker pull spark@sha256:5409c7039f5672f193124cf4c3a94a1136850beb7e21748114a276c94ac9b2ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java21-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:35af73a453d003db92c648d147d45a8b5253d846d9bd7b4fef18c3593bda44ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.1 MB (785081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310540296d12c1d2c3dcbeb1b50524f67883de2a71dc23f2e98d89a7677e09e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f094bb0f37e2860636270e58dbde64c8b2d7cf105eee9c889c43aa9aef4751c1`  
		Last Modified: Tue, 02 Sep 2025 01:14:22 GMT  
		Size: 113.7 MB (113736996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8032964da95fea1053c92cf3dc4de4510ee9b796457dfa442b9cc976ebb30feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccf5eaccb8500e96cc38cb3e11dc6e7a3a3e797ea4dceb056ae1c003dd1bad`

```dockerfile
```

-	Layers:
	-	`sha256:b687018df3865b0fb32fc8b0b515548542e29d66199e7467212296249e137d2b`  
		Last Modified: Tue, 02 Sep 2025 05:10:47 GMT  
		Size: 10.4 MB (10416685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89da161ab1aa927a0068b41e716ae165bc5ff1461c723888aca1155931d2b921`  
		Last Modified: Tue, 02 Sep 2025 05:10:48 GMT  
		Size: 11.6 KB (11593 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java21-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:30d8b5f2ec937010906cdc74839f17fdd9ee07d9286ac80a8b3b367ef039b725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776772693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a75554b5ba2d05771ffcc4b3b09a9b72826fd1b5e94be01c6b89b27076a06f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcfd4e0cba096b00bb08cd252b3e87a526d52f54cd02deb630a45ffe3f30754`  
		Last Modified: Wed, 13 Aug 2025 17:30:36 GMT  
		Size: 108.3 MB (108284844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:1d472bfd54095eded3e79b9e9277b19800d8168149e9a0e2e5f441d587515cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10422789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc0518a8998734cff1e09033310f47961d83d374fa97f2ebad854ade1831798`

```dockerfile
```

-	Layers:
	-	`sha256:5a414e511c6387bc253fc6cdf57519de1387038b1c69f33657e15febafa96050`  
		Last Modified: Wed, 13 Aug 2025 17:10:51 GMT  
		Size: 10.4 MB (10411080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cca7556260799ff49d80fc2b3bb9f7428b57f8fb2da62558f0341d1383b65a3`  
		Last Modified: Wed, 13 Aug 2025 17:10:52 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java21-r-ubuntu`

```console
$ docker pull spark@sha256:0f61924de409cc52affd076be53667c4e0d39a0a55f793b26194e60fba0603d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java21-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:dc660ef3300ba3fb9c68f8bbd390da582be86768d17c29c97480cc3a8d50308a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.7 MB (990666981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171317fcd8a15f98ad3b6e6732e736329c3b6015781462c299e0ca182fe2d5e6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ba0b36700883852dde418b67edc917790c4d1323a2c6097405f42c4183ce5`  
		Last Modified: Tue, 02 Sep 2025 01:14:25 GMT  
		Size: 319.3 MB (319322183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:931916cfecd0dda772b00f70e8239dbe11b2e2e2da0b0c3f9e3e622e06f16bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18622319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1292157ff91f065a1401f832025520d619ad3dc8dce083a1e94973119f1826c8`

```dockerfile
```

-	Layers:
	-	`sha256:46904661233d5b817a7ebb1571690592b4b3e44542eda45a12d6d18f44a34adf`  
		Last Modified: Tue, 02 Sep 2025 05:10:55 GMT  
		Size: 18.6 MB (18611638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178662f90af41b6e4c1ec7438742923cbdfeffcafd01bbd8d8e53bd9703a70d4`  
		Last Modified: Tue, 02 Sep 2025 05:10:56 GMT  
		Size: 10.7 KB (10681 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java21-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:941369ba4b6a1ada47955f3c04cab67404a68aaa86200cda68044f3fa0a48fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **971.0 MB (970984137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e86beff05bfb55b05c865da56a0654c93c09d95215337ffd57b18539483059`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018fe9b72f1eeec213e51dc0276989e68068929c0a6ae0a0acebb2d2a83c22e`  
		Last Modified: Fri, 15 Aug 2025 05:14:36 GMT  
		Size: 302.5 MB (302496288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:9ddbf4950b5231264cd8542dbac5253e249383cf4970871be2acb187d924180e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18586864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8419f7e7a37e3d65eb37ce24154e3e080ae6a4e54f93af7808a3048e19004a4c`

```dockerfile
```

-	Layers:
	-	`sha256:9e748571c49a8206b30db6fe2c18b9e644bca66c367a89bc81913d0cb3662300`  
		Last Modified: Wed, 13 Aug 2025 17:11:08 GMT  
		Size: 18.6 MB (18576103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a33b380f81b62f164b48510ac4b797401f440dbde74acc6cf9830cab30be44c1`  
		Last Modified: Wed, 13 Aug 2025 17:11:09 GMT  
		Size: 10.8 KB (10761 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-scala2.13-java21-ubuntu`

```console
$ docker pull spark@sha256:e2a820d15e0e00c7fe0e514a8aaca8ca95e9ac74b14ddbfebe9dc49ea6f8d4de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-scala2.13-java21-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:66ea345a7c41b1bb45ce918e0e06764cc6151234eab7f3c522d39c1b8bdf4f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.3 MB (671344798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6275d127295b16c8215aba2e363a2574ca712040b8f3d059867e7b9be014a6f2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a392c1972301c29d6cdfc519c28b0f22c6bfd2015d2dbab6dc9de11db06ad20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b338dbd2d339e404aea99449bbb429b04c5c6a8562883e20748a45ea497f3900`

```dockerfile
```

-	Layers:
	-	`sha256:8282f0351827b2281ac8c8e8d33ce7841d5ad71a995b244d853782b44c1e4ffc`  
		Last Modified: Tue, 02 Sep 2025 02:10:37 GMT  
		Size: 4.9 MB (4942972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c089a00e202b04369845dfd7deca3eb5421ae46d5e486ab7042ab6b87028d3dc`  
		Last Modified: Tue, 02 Sep 2025 02:10:38 GMT  
		Size: 22.9 KB (22863 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-scala2.13-java21-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5520dff09c6f84089a25f1ae5a711ac448769d4b7dbfc4dc2ed6286ffdc6eeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668490277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac089b9d8dbd728802d267970ac698817a4d97fc6d360672c967bb1543992a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2d1bf87820e36d53f26b7cd674768abf44232e1496f26c39a0b8e513d4e8c`  
		Last Modified: Tue, 02 Sep 2025 01:03:42 GMT  
		Size: 22.1 MB (22075014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff1d73afae4335a270591ef7c88aa60b4ecc7ac613f31fd49c20a3ad8dcab31`  
		Last Modified: Tue, 02 Sep 2025 03:19:07 GMT  
		Size: 156.1 MB (156088648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf0ef9945e728aa240386ce5491d5283ef22addc9850089ed350aa4dbf0a1dc`  
		Last Modified: Tue, 02 Sep 2025 01:05:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b647f909bb99678b70897a2ec6f8c6370788f632f9c519b5a573c07eef7dd19b`  
		Last Modified: Tue, 02 Sep 2025 01:05:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c16c4d601c5ddf934270bcdc8912d40b31468398ef01d3e68f2e28739abf00`  
		Last Modified: Tue, 02 Sep 2025 06:18:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453439ae78e36a742ada02fd737d263d0b8cc9b0d761b24bc31fe78b2dda5d43`  
		Last Modified: Tue, 02 Sep 2025 06:18:41 GMT  
		Size: 21.4 MB (21355689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6b7a0eb389156db9a5bd1278889aed3ba0dc3e34b32b90c187eb453134d29`  
		Last Modified: Tue, 02 Sep 2025 06:18:34 GMT  
		Size: 441.6 MB (441603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978df6ed235afca534c14be69117e4d2d3c5e84c5eec44d213ae0362ae734db5`  
		Last Modified: Tue, 02 Sep 2025 06:18:40 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d6e48f23eb4ca990a6e374aa92e04a62954498877e0d0a2869e462c06d2a389f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5061445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559c08d504bf6877fb76e8826c4bc84cf5ee7cc7f1ec6b5a4f801e69b764f91a`

```dockerfile
```

-	Layers:
	-	`sha256:5f7c04c947de97e3b35e936f8ccbc17dfc29809eeb1ef874ddb44d0fbb5e6b55`  
		Last Modified: Tue, 02 Sep 2025 08:10:49 GMT  
		Size: 5.0 MB (5038472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0fe3dca8051b6174fd31ce3118993a841ba443114f5bddde2edbe0667e85e3`  
		Last Modified: Tue, 02 Sep 2025 08:10:50 GMT  
		Size: 23.0 KB (22973 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:latest`

```console
$ docker pull spark@sha256:5409c7039f5672f193124cf4c3a94a1136850beb7e21748114a276c94ac9b2ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:35af73a453d003db92c648d147d45a8b5253d846d9bd7b4fef18c3593bda44ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.1 MB (785081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310540296d12c1d2c3dcbeb1b50524f67883de2a71dc23f2e98d89a7677e09e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f094bb0f37e2860636270e58dbde64c8b2d7cf105eee9c889c43aa9aef4751c1`  
		Last Modified: Tue, 02 Sep 2025 01:14:22 GMT  
		Size: 113.7 MB (113736996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:8032964da95fea1053c92cf3dc4de4510ee9b796457dfa442b9cc976ebb30feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccf5eaccb8500e96cc38cb3e11dc6e7a3a3e797ea4dceb056ae1c003dd1bad`

```dockerfile
```

-	Layers:
	-	`sha256:b687018df3865b0fb32fc8b0b515548542e29d66199e7467212296249e137d2b`  
		Last Modified: Tue, 02 Sep 2025 05:10:47 GMT  
		Size: 10.4 MB (10416685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89da161ab1aa927a0068b41e716ae165bc5ff1461c723888aca1155931d2b921`  
		Last Modified: Tue, 02 Sep 2025 05:10:48 GMT  
		Size: 11.6 KB (11593 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:30d8b5f2ec937010906cdc74839f17fdd9ee07d9286ac80a8b3b367ef039b725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776772693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a75554b5ba2d05771ffcc4b3b09a9b72826fd1b5e94be01c6b89b27076a06f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcfd4e0cba096b00bb08cd252b3e87a526d52f54cd02deb630a45ffe3f30754`  
		Last Modified: Wed, 13 Aug 2025 17:30:36 GMT  
		Size: 108.3 MB (108284844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:1d472bfd54095eded3e79b9e9277b19800d8168149e9a0e2e5f441d587515cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10422789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc0518a8998734cff1e09033310f47961d83d374fa97f2ebad854ade1831798`

```dockerfile
```

-	Layers:
	-	`sha256:5a414e511c6387bc253fc6cdf57519de1387038b1c69f33657e15febafa96050`  
		Last Modified: Wed, 13 Aug 2025 17:10:51 GMT  
		Size: 10.4 MB (10411080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cca7556260799ff49d80fc2b3bb9f7428b57f8fb2da62558f0341d1383b65a3`  
		Last Modified: Wed, 13 Aug 2025 17:10:52 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:5409c7039f5672f193124cf4c3a94a1136850beb7e21748114a276c94ac9b2ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:35af73a453d003db92c648d147d45a8b5253d846d9bd7b4fef18c3593bda44ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.1 MB (785081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310540296d12c1d2c3dcbeb1b50524f67883de2a71dc23f2e98d89a7677e09e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a2170938342ed5aea6b687b88b3221b8b59c01d5db743d2f414a845efe5cd`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646425edf4ff4729b1648fd5834f6a0c28eda334e0dd84fd3ba9ed19ae678fb`  
		Last Modified: Tue, 02 Sep 2025 01:12:24 GMT  
		Size: 21.7 MB (21688311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e6f2c04f8af425c17f66f3ab2d6bb30f1c0e2ea16ed7e26cca440b5ff78aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:40 GMT  
		Size: 441.6 MB (441603477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd76a3891790e4420eae92def3ec66060223a8ae26545e5170bb9bafc2e16d`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f094bb0f37e2860636270e58dbde64c8b2d7cf105eee9c889c43aa9aef4751c1`  
		Last Modified: Tue, 02 Sep 2025 01:14:22 GMT  
		Size: 113.7 MB (113736996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:8032964da95fea1053c92cf3dc4de4510ee9b796457dfa442b9cc976ebb30feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccf5eaccb8500e96cc38cb3e11dc6e7a3a3e797ea4dceb056ae1c003dd1bad`

```dockerfile
```

-	Layers:
	-	`sha256:b687018df3865b0fb32fc8b0b515548542e29d66199e7467212296249e137d2b`  
		Last Modified: Tue, 02 Sep 2025 05:10:47 GMT  
		Size: 10.4 MB (10416685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89da161ab1aa927a0068b41e716ae165bc5ff1461c723888aca1155931d2b921`  
		Last Modified: Tue, 02 Sep 2025 05:10:48 GMT  
		Size: 11.6 KB (11593 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:30d8b5f2ec937010906cdc74839f17fdd9ee07d9286ac80a8b3b367ef039b725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776772693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a75554b5ba2d05771ffcc4b3b09a9b72826fd1b5e94be01c6b89b27076a06f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286389b95d27c4831ef5179b41ca6e679a716bf60e67fdfdd6ef762d1db2466c`  
		Last Modified: Tue, 12 Aug 2025 21:21:57 GMT  
		Size: 156.1 MB (156088655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ba34a98b51feef6a4364f712d7c097444d688b9fa96fb00d314348518b7e7`  
		Last Modified: Tue, 12 Aug 2025 18:37:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5e13f97f68f08658239fc6618609df4d297c8c625f322021c57d5569a26f`  
		Last Modified: Tue, 12 Aug 2025 18:37:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014de39138869ba7685b56a43c94d61253fb5627788dcf52489a55f149aed6a`  
		Last Modified: Wed, 13 Aug 2025 00:49:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ba77b38cc321f97bf15b70b5ae6160dd6baabee1962cf3f53e65ccefb2b26`  
		Last Modified: Wed, 13 Aug 2025 00:49:38 GMT  
		Size: 21.4 MB (21355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5fc23cb58423bf9207176759df45e10f1932f2de1809bb97ac09a9b012c382`  
		Last Modified: Wed, 13 Aug 2025 17:31:30 GMT  
		Size: 441.6 MB (441603391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cddf769ec524c483dc12e9985d69293f3a81415d4accfb4dc718e21c21ff16d`  
		Last Modified: Wed, 13 Aug 2025 00:49:35 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcfd4e0cba096b00bb08cd252b3e87a526d52f54cd02deb630a45ffe3f30754`  
		Last Modified: Wed, 13 Aug 2025 17:30:36 GMT  
		Size: 108.3 MB (108284844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:1d472bfd54095eded3e79b9e9277b19800d8168149e9a0e2e5f441d587515cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10422789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc0518a8998734cff1e09033310f47961d83d374fa97f2ebad854ade1831798`

```dockerfile
```

-	Layers:
	-	`sha256:5a414e511c6387bc253fc6cdf57519de1387038b1c69f33657e15febafa96050`  
		Last Modified: Wed, 13 Aug 2025 17:10:51 GMT  
		Size: 10.4 MB (10411080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cca7556260799ff49d80fc2b3bb9f7428b57f8fb2da62558f0341d1383b65a3`  
		Last Modified: Wed, 13 Aug 2025 17:10:52 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:691da856a4850e805e9f8159b561f73563e61177aa93cc704784ffec6b72f2b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:d5bce90d34c2e1a7bf7db379ad4d1860d6767cfb44b1b0f0c0d2c44a3c6d358d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.0 MB (771981589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251d8601d5996fa44b9dd7caf9e40d5172397d205e6ce7231716048b7256a1f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bccd088697078423b39d9fa3fee2b0bd81c6054963ea8f75e9a32f534522df7`  
		Last Modified: Tue, 02 Sep 2025 01:14:18 GMT  
		Size: 113.7 MB (113737217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:ee2807454b1a876d2f570ccef8f445803205fe8a54fda77946af9920a9987095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10424557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd094fdba819db96f2fe680c2724cf0d4ba76b295760e4b344e65bf55feefd`

```dockerfile
```

-	Layers:
	-	`sha256:c7042d9867d51a6fc47987283bfab4ce47ea55672da6750f3706ae7693ced1bf`  
		Last Modified: Tue, 02 Sep 2025 05:10:44 GMT  
		Size: 10.4 MB (10413273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f8e54b05e474c5554173813d6e78a0c7823b8566776bc400b928e484289113`  
		Last Modified: Tue, 02 Sep 2025 05:10:45 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:c53ce7d96abe93941ee368817d75458a8f043c8900b237b2b8e3eab326792aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.2 MB (764234819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3328874d1663502e1ebcfa2b191efac9ee2f242f0f52ace5356b294e52abd0b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df465001054084ae59e670d1a7dacd9337d9c52ebe59b603a1e7540ddf1796da`  
		Last Modified: Wed, 13 Aug 2025 17:31:33 GMT  
		Size: 108.3 MB (108284696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:1895afa3ea75c05896135466e4729dc3d6aa6212fa6bbe557f0606621bab45df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10419043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa26ee4060b7fb8e8c0dc774c9ec08d0a7f0a95c4826522763e07b84452cf83b`

```dockerfile
```

-	Layers:
	-	`sha256:535a6f5dd2b67426cafcea76ca9939215aad15cb8993c29ad7d173ff2da978a8`  
		Last Modified: Wed, 13 Aug 2025 17:10:47 GMT  
		Size: 10.4 MB (10407656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b46aa45a8d57d8e0dfd935a9508a8b1e744e976390512a3c45d2f314893fd24`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 11.4 KB (11387 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:r`

```console
$ docker pull spark@sha256:afa432ca3c54f1ef1d865bbf24292f86ef92f0fa91527302db083cbd00d40639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:6c4ed92d67b04b6ff4bf46b5ac7e6f5181571cd391747cc6f5f77aa69d79850f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.6 MB (977566865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdafb5c36df361e533264ab6d20ada54a53c63851833bc35eeffd0108b9c752`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf63213fb3473f8fd12d5023d0d20539dfa4a1aaa67f0bf643628a8b64fafc77`  
		Last Modified: Tue, 02 Sep 2025 05:12:26 GMT  
		Size: 319.3 MB (319322493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:2a0e3e8426ee0767050c77bcd36f73eed343efdb3c6e1011dda9f32a2fd667cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18619761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef66dcc5195557c3e72469fb46a24b6ef64b94668044de4c600b3c2b954d56`

```dockerfile
```

-	Layers:
	-	`sha256:8ae250c81b4cc244f501fe4859718a2f36a658d5b8b797225a4d97a0595b6499`  
		Last Modified: Tue, 02 Sep 2025 05:10:59 GMT  
		Size: 18.6 MB (18608808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c21776ba02312d1a6e2f7add42d3eaf083db5ef72ba5697e8edfed08874bf6b`  
		Last Modified: Tue, 02 Sep 2025 05:11:00 GMT  
		Size: 11.0 KB (10953 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:667a772a00958d8e117c3b24919f7cc7b5c958523a13df9300fa0a8bdc0fac9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.4 MB (958446537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395efdce75be75403f3d906483ea0c9100f8f45eaac66f2234134c875aa811e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
USER root
# Tue, 27 May 2025 15:48:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV R_HOME=/usr/lib/R
# Tue, 27 May 2025 15:48:12 GMT
USER spark
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e10f8cd8cdc3d1611314774ec47f0d26949f6cea62e7d2794a2238ceb337a`  
		Last Modified: Wed, 13 Aug 2025 00:51:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294822506d194fd4373a4a346f304987cdb3316a8aa479ff2effc4c3c7d07d19`  
		Last Modified: Wed, 13 Aug 2025 00:51:57 GMT  
		Size: 21.4 MB (21355376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79ee3086de758ba2cddd5aff81024789d9842e6fd169237d4ac372a1738ae8`  
		Last Modified: Wed, 13 Aug 2025 02:39:50 GMT  
		Size: 441.6 MB (441603471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cfce891c1a415cf8626c3483afa1603a9f4b8290043cab1a79b782362c9aee`  
		Last Modified: Wed, 13 Aug 2025 00:51:55 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff980efb92480747419cb3d7eb2f4b13104a7a47a5f786a208d83bf5ab3b34b`  
		Last Modified: Fri, 15 Aug 2025 05:14:32 GMT  
		Size: 302.5 MB (302496414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:06f74422141527eb6d8c60b4b43a953ffd27295b06c60d41e7953679e5d80d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18584330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36a1584d19be6a35f69ca95ac856fd42b1bbb3ade7588812e47f7468b1298b4`

```dockerfile
```

-	Layers:
	-	`sha256:7712511fdb3d9aceff9d18cf6081de00628ea8ec9b148fea7fd99781764a03f9`  
		Last Modified: Wed, 13 Aug 2025 17:11:09 GMT  
		Size: 18.6 MB (18573285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c3d51023fb23665200279ef01f8b078d56e15a2111527bf53cd2b2b43cf9cb`  
		Last Modified: Wed, 13 Aug 2025 17:11:10 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:scala`

```console
$ docker pull spark@sha256:bec33899f38b9cce395dedac861830baa285450824cf644a0d555546f542236b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:fea501e7d8b625863d6f5cfc0f67224e4c6985c61aeaf5fb9a030fe16fb67e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658244372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6133148f409294c1c0738efad15af0f60d247c5c72b0d1fddd90ee6c3c862b59`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586682f08740b35c8526f86fdb26e69bc289c02cc4fd645d13c6f179b9a53043`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179be122863dae68264044e6ffaebeb6f6853cd746b620126968d31e54d5463`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 21.7 MB (21688318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a4813d7e16870d81265c7f6796d06282c632a563b33d8d5fd9098d5b89f1a`  
		Last Modified: Tue, 02 Sep 2025 01:12:15 GMT  
		Size: 441.6 MB (441603468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0efbad9694907e76dabdf0681f71ca77312a16cb442b71a5aacbab426546aa`  
		Last Modified: Tue, 02 Sep 2025 01:12:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:65c9ee7e5bdaf26508ac195cb5770c983bbc9130dffb6a92442d3c8279be5e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423446de67d5937db6d9eea2b5c220fedbe122b44be4819ba15cc615ff02f5ce`

```dockerfile
```

-	Layers:
	-	`sha256:a87a7828b0178c768ac1706ac74163e1c5953d8d2c926ce5786b5b811142e3aa`  
		Last Modified: Tue, 02 Sep 2025 02:10:44 GMT  
		Size: 4.9 MB (4940150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8ef5c5b8343cb1acab240fccc83a8c4947624464aac2373e9ef61cb5d1c4d5`  
		Last Modified: Tue, 02 Sep 2025 02:10:45 GMT  
		Size: 23.1 KB (23146 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e30a9e898cd983f139697e0a051635afc3549a4aee0c75b4b92399f7ccea3fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.0 MB (655952508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae00545b1b4b856cba7d370b87987cc43bd80aed1a8f7248a060858b129250ff`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 27 May 2025 15:48:12 GMT
ARG RELEASE
# Tue, 27 May 2025 15:48:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 15:48:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 May 2025 15:48:12 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 27 May 2025 15:48:12 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 15:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 15:48:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 May 2025 15:48:12 GMT
CMD ["jshell"]
# Tue, 27 May 2025 15:48:12 GMT
ARG spark_uid=185
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz.asc GPG_KEY=4DC9676CEF9A83E98FCA02784D6620843CD87F5A
# Tue, 27 May 2025 15:48:12 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 27 May 2025 15:48:12 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 27 May 2025 15:48:12 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 27 May 2025 15:48:12 GMT
WORKDIR /opt/spark/work-dir
# Tue, 27 May 2025 15:48:12 GMT
USER spark
# Tue, 27 May 2025 15:48:12 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2d1bf87820e36d53f26b7cd674768abf44232e1496f26c39a0b8e513d4e8c`  
		Last Modified: Tue, 02 Sep 2025 01:03:42 GMT  
		Size: 22.1 MB (22075014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a562fdfee59db98ef10f59acb342e37698d1891b3f4608dab55a20e25c85093`  
		Last Modified: Tue, 02 Sep 2025 03:15:28 GMT  
		Size: 143.6 MB (143550948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6953a5f4a054b79b249f8f3bbd1be1a1c4f1873fa3be3cd054e0029f8a71087`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fd4799efced03c22e41b0e5ae8ece8022f4df5662e5b25352d453d8783892`  
		Last Modified: Tue, 02 Sep 2025 01:03:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626a4a66c5c6a6908a2c062f2cc8209efbaeb14315a158a9e21a98144b4cad1d`  
		Last Modified: Tue, 02 Sep 2025 07:00:42 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d242d7a7a5680644c29be3300ebdcec7562015013b56c80b6ac0d7dc5142111`  
		Last Modified: Tue, 02 Sep 2025 07:00:45 GMT  
		Size: 21.4 MB (21355649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c3598999f7b5e24b38b389f12edfed3da513cd86ba5aff282b7636e2bd9ac`  
		Last Modified: Tue, 02 Sep 2025 06:41:54 GMT  
		Size: 441.6 MB (441603392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a58f7daf2c27e8ef2a2572ea196fe27b166f47a81b3db0cabe308e8e654086`  
		Last Modified: Tue, 02 Sep 2025 07:15:57 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:02b43f83a3ed41c6016d7eac27ee2a0de8ad4f2cb7c447bf425a12e4b9ca3d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e002a1359bc96383a2c4d7775e6237a6c69523b36a910b4eb80018bd35a6197`

```dockerfile
```

-	Layers:
	-	`sha256:d3ed6730efabbaf7fb55861864901f5af99138771d2dd9849b9ba3842d7ad9ba`  
		Last Modified: Tue, 02 Sep 2025 08:10:45 GMT  
		Size: 5.0 MB (5035662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3295631c72c3b889ca63542528f34cd8ae86bb3ba1cf23cc70746f8a1388e884`  
		Last Modified: Tue, 02 Sep 2025 08:10:46 GMT  
		Size: 23.3 KB (23268 bytes)  
		MIME: application/vnd.in-toto+json
