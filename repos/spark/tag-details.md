<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spark`

-	[`spark:3.5.7`](#spark357)
-	[`spark:3.5.7-java17`](#spark357-java17)
-	[`spark:3.5.7-java17-python3`](#spark357-java17-python3)
-	[`spark:3.5.7-java17-r`](#spark357-java17-r)
-	[`spark:3.5.7-java17-scala`](#spark357-java17-scala)
-	[`spark:3.5.7-python3`](#spark357-python3)
-	[`spark:3.5.7-r`](#spark357-r)
-	[`spark:3.5.7-scala`](#spark357-scala)
-	[`spark:3.5.7-scala2.12-java11-python3-r-ubuntu`](#spark357-scala212-java11-python3-r-ubuntu)
-	[`spark:3.5.7-scala2.12-java11-python3-ubuntu`](#spark357-scala212-java11-python3-ubuntu)
-	[`spark:3.5.7-scala2.12-java11-r-ubuntu`](#spark357-scala212-java11-r-ubuntu)
-	[`spark:3.5.7-scala2.12-java11-ubuntu`](#spark357-scala212-java11-ubuntu)
-	[`spark:3.5.7-scala2.12-java17-python3-r-ubuntu`](#spark357-scala212-java17-python3-r-ubuntu)
-	[`spark:3.5.7-scala2.12-java17-python3-ubuntu`](#spark357-scala212-java17-python3-ubuntu)
-	[`spark:3.5.7-scala2.12-java17-r-ubuntu`](#spark357-scala212-java17-r-ubuntu)
-	[`spark:3.5.7-scala2.12-java17-ubuntu`](#spark357-scala212-java17-ubuntu)
-	[`spark:4.0.1`](#spark401)
-	[`spark:4.0.1-java21`](#spark401-java21)
-	[`spark:4.0.1-java21-python3`](#spark401-java21-python3)
-	[`spark:4.0.1-java21-r`](#spark401-java21-r)
-	[`spark:4.0.1-java21-scala`](#spark401-java21-scala)
-	[`spark:4.0.1-python3`](#spark401-python3)
-	[`spark:4.0.1-r`](#spark401-r)
-	[`spark:4.0.1-scala`](#spark401-scala)
-	[`spark:4.0.1-scala2.13-java17-python3-r-ubuntu`](#spark401-scala213-java17-python3-r-ubuntu)
-	[`spark:4.0.1-scala2.13-java17-python3-ubuntu`](#spark401-scala213-java17-python3-ubuntu)
-	[`spark:4.0.1-scala2.13-java17-r-ubuntu`](#spark401-scala213-java17-r-ubuntu)
-	[`spark:4.0.1-scala2.13-java17-ubuntu`](#spark401-scala213-java17-ubuntu)
-	[`spark:4.0.1-scala2.13-java21-python3-r-ubuntu`](#spark401-scala213-java21-python3-r-ubuntu)
-	[`spark:4.0.1-scala2.13-java21-python3-ubuntu`](#spark401-scala213-java21-python3-ubuntu)
-	[`spark:4.0.1-scala2.13-java21-r-ubuntu`](#spark401-scala213-java21-r-ubuntu)
-	[`spark:4.0.1-scala2.13-java21-ubuntu`](#spark401-scala213-java21-ubuntu)
-	[`spark:latest`](#sparklatest)
-	[`spark:python3`](#sparkpython3)
-	[`spark:python3-java17`](#sparkpython3-java17)
-	[`spark:r`](#sparkr)
-	[`spark:scala`](#sparkscala)

## `spark:3.5.7`

```console
$ docker pull spark@sha256:bc10f25ccbac0e6e9f131a3f369da6e865a2765300ca0c171b81c7d4499ff727
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7` - linux; amd64

```console
$ docker pull spark@sha256:c1148460dd3cb5e42475c6dba634a267074af65bea2c78736367bb5f5eff41da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 MB (655675169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd92d38b1d5d9ab51dbeffa29dbb1fea953f34f30147b60c6b93c68087706d4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:43 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:07 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:07 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:23 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:23 GMT
USER spark
# Fri, 14 Nov 2025 00:40:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:21:15 GMT
USER root
# Fri, 14 Nov 2025 01:21:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:21:15 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9997af0184af5a3eec8b9c31e521431f71ab4219764f54025bded4ac95f540`  
		Last Modified: Tue, 13 Jan 2026 00:58:35 GMT  
		Size: 16.2 MB (16150551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0b6ef10bde275888f1e4eabdf96bf1fb39810178fe9e45884c8d0ee37a6ed`  
		Last Modified: Tue, 13 Jan 2026 00:58:43 GMT  
		Size: 145.0 MB (144977425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc12bfa2e7919efde5fc34c1cf3018da75e1cf252fd1bfee26a392fe8a452b`  
		Last Modified: Tue, 13 Jan 2026 00:58:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d3b3f4cbc4ce873ec58088f789c93e489f329e1ae73f2c915a75412c3179`  
		Last Modified: Tue, 13 Jan 2026 00:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712adf158431f9946962fb99ccd9ef1c1684cbd51303ee663e707fe7565cdd3e`  
		Last Modified: Tue, 13 Jan 2026 01:55:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14953853692245e7b11cea4c9c3caadc89c72d6fa8110f8634ddb49021d861f3`  
		Last Modified: Tue, 13 Jan 2026 01:55:54 GMT  
		Size: 21.8 MB (21847512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb90fd3aceeed484813737477c0b17c4c45184571577f29932a10e8c0d6f534`  
		Last Modified: Tue, 13 Jan 2026 07:26:14 GMT  
		Size: 324.9 MB (324927696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe664390b099dce484c7ab57f87a10495026606ed3f8cfe5be8ceff1fa00658`  
		Last Modified: Tue, 13 Jan 2026 01:56:00 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ed2b86389774845b228ee3dbbaa75b2a9ad02b0d137b40e9f7e5645221c35`  
		Last Modified: Tue, 13 Jan 2026 07:32:46 GMT  
		Size: 118.2 MB (118229155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7` - unknown; unknown

```console
$ docker pull spark@sha256:e2198b677a650ec51500f2ac5ec7815a8e2e3fb042cae368c50fc8f45d2f02b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694f5b39362d28c5c51169c890921318e71657ca2d059e5977d171aae23cfbc1`

```dockerfile
```

-	Layers:
	-	`sha256:d6fad832c733c1b30ffa034ae8dd6d65a626b8aa44df1e6b2235f48ef59df244`  
		Last Modified: Thu, 15 Jan 2026 12:09:32 GMT  
		Size: 10.3 MB (10314925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23935aa857de4c5bb5428ee4219f5e1611b2339db5274e77f41676035de4befc`  
		Last Modified: Thu, 15 Jan 2026 12:09:10 GMT  
		Size: 11.0 KB (10973 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:27ace266cd2f246ada7833718da5585188286f114bb10f9826d1e6735444a1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (645970486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9c45e5e577a47f98cbe67943f8c5a91b75360b19fc6757fc60ad6857cfd18`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:20 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:42:10 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:42:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:42:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:42:30 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:42:30 GMT
USER spark
# Fri, 14 Nov 2025 00:42:30 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:37 GMT
USER root
# Fri, 14 Nov 2025 01:37:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:37 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a970ce4b07b68726d7c7d9cf4c1e5c250d429307c71e724a001234cd82c44`  
		Last Modified: Tue, 13 Jan 2026 00:54:38 GMT  
		Size: 16.1 MB (16066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed77fd8d2627057e424752b07749af4fa46c9166dfa1dae49b863c328c34bdb`  
		Last Modified: Tue, 13 Jan 2026 01:54:22 GMT  
		Size: 141.7 MB (141737442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0ad7672facc935673ae17b0ba9af4eb1ff8de6b6f1c320abc46fed0abde8f`  
		Last Modified: Tue, 13 Jan 2026 00:54:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798f1e93315ead6c0269bdaf161c652aad5255cb384e63988571c2f70282579`  
		Last Modified: Tue, 13 Jan 2026 00:54:29 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209a7fd8d4b98af73c15edbfc79a5cc873a8542e09f2a057b32f4b064813e6af`  
		Last Modified: Tue, 13 Jan 2026 12:13:28 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e170feba31806d42f2d3a62ae70d7d795e1b2ac53d80738eff85625e64c41`  
		Last Modified: Tue, 13 Jan 2026 12:13:30 GMT  
		Size: 21.5 MB (21535516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa290ce8600b5f293443b39b35c28288864711e31c5d03feeee2bf3b8f0b5d`  
		Last Modified: Tue, 13 Jan 2026 12:13:45 GMT  
		Size: 324.9 MB (324927648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359710dc95aad6630f000289520cf6d48fb2fba73335ee78b5c2d6c2bc3c17f0`  
		Last Modified: Tue, 13 Jan 2026 12:13:29 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189236b7ecdb4dc58b9dc29a37baa7010a4995bdd34be08f3659e9f9dbd60477`  
		Last Modified: Tue, 13 Jan 2026 12:13:36 GMT  
		Size: 114.3 MB (114313785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7` - unknown; unknown

```console
$ docker pull spark@sha256:c4f0897e460c6385d069a2c86b8deb6bc20a636f23ec1e33f191296a3dd6ae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88e64e7fc2da084a64711cbf7f72da0e5cff3e0406675a2c31fed239bb4b5f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec28110373922cd55696179774b8fc7ace61db34ab3b2d94ea990c55fc4f9439`  
		Last Modified: Fri, 14 Nov 2025 01:38:10 GMT  
		Size: 10.3 MB (10309991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edcd4a44dde40b09a1799152ba053058af588b7b2f439fc6c7882e3af5c616ee`  
		Last Modified: Thu, 15 Jan 2026 04:20:29 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-java17`

```console
$ docker pull spark@sha256:31a8c385283050d7a756634f23e0f3cddde0131a6c8ad6a6b20b05d94bc1d472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-java17` - linux; amd64

```console
$ docker pull spark@sha256:def686569eaa28c79f23f92c6eb2a711248c113a028a3f20eafeb9474fe96104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 MB (655560130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a841694b4855726107822e6155eccff688aa2cef6a9a47ddaded82f5f22b6c2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:03 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:03 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:03 GMT
USER spark
# Fri, 14 Nov 2025 00:40:03 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:36 GMT
USER root
# Fri, 14 Nov 2025 01:20:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:36 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ddc142dbd294d1861ba917801969cddd78edae3050e0abe0153b39ea3722e0`  
		Last Modified: Tue, 13 Jan 2026 02:27:44 GMT  
		Size: 21.9 MB (21850558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6f43adf3d8d5ac8048ad3d28d3140461ab08ff548611f3e549653bcf0f86e`  
		Last Modified: Tue, 13 Jan 2026 03:41:33 GMT  
		Size: 324.9 MB (324927670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21d6393c00ceffcb23b76c01584309a96fb6e976dd6aa974e27772112dde9d`  
		Last Modified: Tue, 13 Jan 2026 02:27:51 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c70143cbc33471a2d273161de97a0e5ce788172c6f8b44262cfb154b91547`  
		Last Modified: Tue, 13 Jan 2026 10:34:50 GMT  
		Size: 113.7 MB (113686705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17` - unknown; unknown

```console
$ docker pull spark@sha256:dea25b3a982b7474158dfe3ae8278bb987bf074e6db6b9c5f20c7c0ac4f5d678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10305816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91c26477fd08846992db26a04f02c1b4cc5f3661c2e2041a622d26398495b97`

```dockerfile
```

-	Layers:
	-	`sha256:dba2eda3687c44598cb2a42f9d2da8a020028d197aa4ea4453de756d4c1fd6da`  
		Last Modified: Tue, 13 Jan 2026 09:44:51 GMT  
		Size: 10.3 MB (10294814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef959e21a2d3d01e2a605e0a2f463587b3c2a983b51971f0e8a122ab514f510`  
		Last Modified: Tue, 13 Jan 2026 09:44:40 GMT  
		Size: 11.0 KB (11002 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7d2eeaf6eae957e80e281db027921cb528c0a508d550cc9a01a644939f5b9d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647906249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12282df21256323007b4623b516ac4113f97dc91d029232ed96e2d1014cc0c9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:41:52 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:52 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:52 GMT
USER spark
# Fri, 14 Nov 2025 00:41:52 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:02 GMT
USER root
# Fri, 14 Nov 2025 01:37:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:02 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a2d7b006aa25763b9e6edd46f17d2069567773314a5077991ec87d2b170a6`  
		Last Modified: Tue, 13 Jan 2026 11:29:15 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b3dbef2ce366da1ade8376fcad6bff5e0d39d87b4a7d9e6e635bbfeb30a173`  
		Last Modified: Tue, 13 Jan 2026 11:29:35 GMT  
		Size: 21.5 MB (21537971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035bcc6536920fedae222ca7c8add833bd67dc5739c25cdd7caaadd09249a18`  
		Last Modified: Tue, 13 Jan 2026 11:30:08 GMT  
		Size: 324.9 MB (324927659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134b18b042cae2e6c65253efcb1add53663a5cc729b915923070f36487e141b2`  
		Last Modified: Tue, 13 Jan 2026 11:29:16 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f210fb2984de57ceb6b469a3dec2876da4300d19fe07f76ca013ca7637e661`  
		Last Modified: Tue, 13 Jan 2026 14:45:03 GMT  
		Size: 108.3 MB (108276513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17` - unknown; unknown

```console
$ docker pull spark@sha256:60445b1fee7882c31f552cce280beb025af5bc3758a715a66d6e18d1ff72b7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10300356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910d492fe9de2da09de3a6d0fa881d5f8739b295ee3e1e4bbdf6b11dc4617d42`

```dockerfile
```

-	Layers:
	-	`sha256:d586568f1813d1f8d5f52ad544a4dc15ccd1578faba729ddb1a546d2e47d2eed`  
		Last Modified: Fri, 14 Nov 2025 01:37:30 GMT  
		Size: 10.3 MB (10289262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f5a3acd0e7bc34e04e814f1f889c20aa45f10cdd173c444b1b39899dcdf270`  
		Last Modified: Fri, 14 Nov 2025 01:37:29 GMT  
		Size: 11.1 KB (11094 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-java17-python3`

```console
$ docker pull spark@sha256:31a8c385283050d7a756634f23e0f3cddde0131a6c8ad6a6b20b05d94bc1d472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:def686569eaa28c79f23f92c6eb2a711248c113a028a3f20eafeb9474fe96104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 MB (655560130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a841694b4855726107822e6155eccff688aa2cef6a9a47ddaded82f5f22b6c2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:03 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:03 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:03 GMT
USER spark
# Fri, 14 Nov 2025 00:40:03 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:36 GMT
USER root
# Fri, 14 Nov 2025 01:20:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:36 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ddc142dbd294d1861ba917801969cddd78edae3050e0abe0153b39ea3722e0`  
		Last Modified: Tue, 13 Jan 2026 02:27:44 GMT  
		Size: 21.9 MB (21850558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6f43adf3d8d5ac8048ad3d28d3140461ab08ff548611f3e549653bcf0f86e`  
		Last Modified: Tue, 13 Jan 2026 03:41:33 GMT  
		Size: 324.9 MB (324927670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21d6393c00ceffcb23b76c01584309a96fb6e976dd6aa974e27772112dde9d`  
		Last Modified: Tue, 13 Jan 2026 02:27:51 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c70143cbc33471a2d273161de97a0e5ce788172c6f8b44262cfb154b91547`  
		Last Modified: Tue, 13 Jan 2026 10:34:50 GMT  
		Size: 113.7 MB (113686705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:dea25b3a982b7474158dfe3ae8278bb987bf074e6db6b9c5f20c7c0ac4f5d678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10305816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91c26477fd08846992db26a04f02c1b4cc5f3661c2e2041a622d26398495b97`

```dockerfile
```

-	Layers:
	-	`sha256:dba2eda3687c44598cb2a42f9d2da8a020028d197aa4ea4453de756d4c1fd6da`  
		Last Modified: Tue, 13 Jan 2026 09:44:51 GMT  
		Size: 10.3 MB (10294814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef959e21a2d3d01e2a605e0a2f463587b3c2a983b51971f0e8a122ab514f510`  
		Last Modified: Tue, 13 Jan 2026 09:44:40 GMT  
		Size: 11.0 KB (11002 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7d2eeaf6eae957e80e281db027921cb528c0a508d550cc9a01a644939f5b9d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647906249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12282df21256323007b4623b516ac4113f97dc91d029232ed96e2d1014cc0c9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:41:52 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:52 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:52 GMT
USER spark
# Fri, 14 Nov 2025 00:41:52 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:02 GMT
USER root
# Fri, 14 Nov 2025 01:37:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:02 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a2d7b006aa25763b9e6edd46f17d2069567773314a5077991ec87d2b170a6`  
		Last Modified: Tue, 13 Jan 2026 11:29:15 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b3dbef2ce366da1ade8376fcad6bff5e0d39d87b4a7d9e6e635bbfeb30a173`  
		Last Modified: Tue, 13 Jan 2026 11:29:35 GMT  
		Size: 21.5 MB (21537971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035bcc6536920fedae222ca7c8add833bd67dc5739c25cdd7caaadd09249a18`  
		Last Modified: Tue, 13 Jan 2026 11:30:08 GMT  
		Size: 324.9 MB (324927659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134b18b042cae2e6c65253efcb1add53663a5cc729b915923070f36487e141b2`  
		Last Modified: Tue, 13 Jan 2026 11:29:16 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f210fb2984de57ceb6b469a3dec2876da4300d19fe07f76ca013ca7637e661`  
		Last Modified: Tue, 13 Jan 2026 14:45:03 GMT  
		Size: 108.3 MB (108276513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:60445b1fee7882c31f552cce280beb025af5bc3758a715a66d6e18d1ff72b7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10300356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910d492fe9de2da09de3a6d0fa881d5f8739b295ee3e1e4bbdf6b11dc4617d42`

```dockerfile
```

-	Layers:
	-	`sha256:d586568f1813d1f8d5f52ad544a4dc15ccd1578faba729ddb1a546d2e47d2eed`  
		Last Modified: Fri, 14 Nov 2025 01:37:30 GMT  
		Size: 10.3 MB (10289262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f5a3acd0e7bc34e04e814f1f889c20aa45f10cdd173c444b1b39899dcdf270`  
		Last Modified: Fri, 14 Nov 2025 01:37:29 GMT  
		Size: 11.1 KB (11094 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-java17-r`

```console
$ docker pull spark@sha256:ac9ae5af06250e70d3bb8f2ad15d16704aed47d2a0c8f09d764ea0dea52cd198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:5be26a067968db84328419943a1b89764682b40980b53ce6d0004d1514f2de6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.0 MB (861020614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f243213f525acff42b9182c21d4a70d889e3bc4ce3e65c5bbf328fb614b875`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:03 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:03 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:03 GMT
USER spark
# Fri, 14 Nov 2025 00:40:03 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:21:34 GMT
USER root
# Fri, 14 Nov 2025 01:21:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:21:34 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:21:34 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ddc142dbd294d1861ba917801969cddd78edae3050e0abe0153b39ea3722e0`  
		Last Modified: Tue, 13 Jan 2026 02:27:44 GMT  
		Size: 21.9 MB (21850558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6f43adf3d8d5ac8048ad3d28d3140461ab08ff548611f3e549653bcf0f86e`  
		Last Modified: Tue, 13 Jan 2026 03:41:33 GMT  
		Size: 324.9 MB (324927670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21d6393c00ceffcb23b76c01584309a96fb6e976dd6aa974e27772112dde9d`  
		Last Modified: Tue, 13 Jan 2026 02:27:51 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b44b3a53a6157dd4f6f5cec0315fd41402e0756bfdcd9826537e873174f5702`  
		Last Modified: Fri, 14 Nov 2025 01:22:31 GMT  
		Size: 319.1 MB (319147189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:3bb23fa662fbbd29ec0b490d5621f5bc6bf7ab1f68b2ae3bcc7d9ce0f31ac595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18493769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c61df2ae57c77c34f331c43cef8489ae82dd9b850b4aa4a12a669cc3e72f67`

```dockerfile
```

-	Layers:
	-	`sha256:5c813313a5dc936472fbb2e5eceef2466df4ab720a54d856b5b8793c77b4b570`  
		Last Modified: Fri, 14 Nov 2025 01:22:25 GMT  
		Size: 18.5 MB (18483085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e02c8abe2bb91a2148190d700e9437489c9dcebd50b37db2db253196f7f8ce`  
		Last Modified: Fri, 14 Nov 2025 01:22:24 GMT  
		Size: 10.7 KB (10684 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:68f800e24abfc9710ed538d3c0c6a719208bca6932a742909be9bb32670b842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.0 MB (842007725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fcc0b353a058ffb31b2d06e15ee66080e2b41b044c7590ad4d0f27c14f57d1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:41:52 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:52 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:52 GMT
USER spark
# Fri, 14 Nov 2025 00:41:52 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:59 GMT
USER root
# Fri, 14 Nov 2025 01:37:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:59 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:37:59 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a2d7b006aa25763b9e6edd46f17d2069567773314a5077991ec87d2b170a6`  
		Last Modified: Tue, 13 Jan 2026 11:29:15 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b3dbef2ce366da1ade8376fcad6bff5e0d39d87b4a7d9e6e635bbfeb30a173`  
		Last Modified: Tue, 13 Jan 2026 11:29:35 GMT  
		Size: 21.5 MB (21537971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035bcc6536920fedae222ca7c8add833bd67dc5739c25cdd7caaadd09249a18`  
		Last Modified: Tue, 13 Jan 2026 11:30:08 GMT  
		Size: 324.9 MB (324927659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134b18b042cae2e6c65253efcb1add53663a5cc729b915923070f36487e141b2`  
		Last Modified: Tue, 13 Jan 2026 11:29:16 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1807a6df26343c6fbd03b2cbc60d970d29aca3529ebe4a7d9a4be6eddbf3bc`  
		Last Modified: Fri, 14 Nov 2025 01:39:12 GMT  
		Size: 302.4 MB (302377989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:2d20252b04eedd3bdfda10fff2954915e3e16f02f338ada54cc0e4a4462a28fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18458402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c51bfabb6f43ca700974558bcdd4fb6652ebd2173a0a41cd943a0f33c4d2f56`

```dockerfile
```

-	Layers:
	-	`sha256:b0f27d88476698da3b19025f43545ccb349c8e0eac7ef869e4fbf345789bdc99`  
		Last Modified: Fri, 14 Nov 2025 01:38:53 GMT  
		Size: 18.4 MB (18447638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dced6e36914f837a9c0168edd79aa52e651fc11e246fe1a89cfd1321ad14885e`  
		Last Modified: Fri, 14 Nov 2025 01:38:52 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-java17-scala`

```console
$ docker pull spark@sha256:a98f634ebbfbc563a05eb915db55bb760cfb9a8670afa1ce4ecd2fbcf67ae1c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:0687f5aea29cd047c36649cdc979e27bc05a6b21efebce90ab8578a187fbba3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541860517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ab6f56713d867309191b865acf7d468e2c6c0ca812f5a0af94913e71824e9f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:52 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:09:19 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:09:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:09:30 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:09:30 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:09:53 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:09:53 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:09:53 GMT
USER spark
# Fri, 16 Jan 2026 01:09:53 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ede50ffae3ced1f5ffed35549b8bac68387426b88ec95cdbcc82baf2fd33f`  
		Last Modified: Thu, 15 Jan 2026 22:20:18 GMT  
		Size: 20.7 MB (20688694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227b76b41c25c5c0ce948a17f2d8308398b5dc827c545c7142ca20f30b1cb256`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 144.9 MB (144850896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589743ef81c842f54b86e7e96cf9a3ce388b1e8e676068f5d16a511dd91fccfb`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70ee470d498578f3f261d731c31f16ca9c9f5f583ac83347ec39bc91ed183dc`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4366d7e804bd53e52548a58e956a5efcb2cd46a2e4c55fd5f4c0ed1b53503f4`  
		Last Modified: Fri, 16 Jan 2026 01:10:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82576562d168916fca66911ab14611c93a942588e4826774dfd3b3f96ef40432`  
		Last Modified: Fri, 16 Jan 2026 01:10:29 GMT  
		Size: 21.9 MB (21850522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b9c14222bf58edb5bb5cfd6d119d581ed29ba6fc921384433f7425efb37d2a`  
		Last Modified: Fri, 16 Jan 2026 01:13:00 GMT  
		Size: 324.9 MB (324927712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bddc1e58d0f4cf586898891621c317f4d4d6eb0d1aa7003d559030c715da1e`  
		Last Modified: Fri, 16 Jan 2026 01:26:34 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:addf68a9151384e7913fc568cdee26c296a52a143e4c13b42b2e4094458c2c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4858150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b01cd2d7ce9ddf52dfc677deab096d47a42d7db1f88316562a0647c97a97d7`

```dockerfile
```

-	Layers:
	-	`sha256:ae3f545ac1f8d273de7577493ea71e9561eeba6360f4617aa1233569f9cdd317`  
		Last Modified: Fri, 16 Jan 2026 03:12:34 GMT  
		Size: 4.8 MB (4835184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79dcd826100976968c375f221ac5d20538176b24205b841aff2d1d4ab381781`  
		Last Modified: Fri, 16 Jan 2026 03:12:35 GMT  
		Size: 23.0 KB (22966 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:78ba004d6bde8ad5a03fb76b7d1abcf5bbe8f56d84c6fc4bc883342fa23c596b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539643827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be73312d8fb0e9f932d7bcd15b6ce8c0bc4ea7cb2c85d66c853a0dfeafab779c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:18 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:13:34 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:13:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:13:42 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:13:42 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:13:51 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:13:51 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:13:51 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:13:51 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:13:51 GMT
USER spark
# Fri, 16 Jan 2026 01:13:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f84e430918f56b2a3b21400c38155cc3747e29ae43bf89ec7bd1a2d206b818`  
		Last Modified: Thu, 15 Jan 2026 22:19:47 GMT  
		Size: 22.1 MB (22107474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adfc04002164e831afd68d878fa3bbe3cc04f413d131d3222fbedebb7dda33`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 143.7 MB (143681283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b23fdceb460806f1b4d37e8e1d0a03126441b8a0d1efe1ad54d2d05fce4d1`  
		Last Modified: Thu, 15 Jan 2026 22:19:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7feaec1b5ae6c7e6e38638d964d4991ce35f3a13191880a163bdef3d12c7312`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6798439e682e845c9714243eb0cb4fca1a0ece43f8e3f3f27af8a0c870074a`  
		Last Modified: Fri, 16 Jan 2026 01:14:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dbbccc0cdb73db88c9d082dd42755d1d35fc974a0e17fc9e87479a416aa0b4`  
		Last Modified: Fri, 16 Jan 2026 01:14:32 GMT  
		Size: 21.5 MB (21537886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49017c17b48ad3771d968afcb5848cc73c1d3451839294635fe71c6bb10f0e13`  
		Last Modified: Fri, 16 Jan 2026 01:14:38 GMT  
		Size: 324.9 MB (324927655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232ccd192c997a9d999d7bebad3523792f2f7faf2bb7ed5185279ca4a8250d28`  
		Last Modified: Fri, 16 Jan 2026 01:14:28 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:20eb85aca3ae6886c8a8ddc4d35d1a0d2cec8c54073928ac1a800e69af5d8e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71e513f81ef9c6a3d7255347af1de780f4f78c9a345e31bbd04e7149f9c747`

```dockerfile
```

-	Layers:
	-	`sha256:8875f74694af27a94dacff08815f4c3a7fe8629cc45e30b668ea437890ebd3bf`  
		Last Modified: Fri, 16 Jan 2026 03:12:40 GMT  
		Size: 4.9 MB (4930687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8985a775bbdfa7a4004fa4b15b6b0d8fe3482af227e23db7184de17b0388b0c`  
		Last Modified: Fri, 16 Jan 2026 03:12:41 GMT  
		Size: 23.1 KB (23076 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-python3`

```console
$ docker pull spark@sha256:bc10f25ccbac0e6e9f131a3f369da6e865a2765300ca0c171b81c7d4499ff727
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-python3` - linux; amd64

```console
$ docker pull spark@sha256:c1148460dd3cb5e42475c6dba634a267074af65bea2c78736367bb5f5eff41da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 MB (655675169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd92d38b1d5d9ab51dbeffa29dbb1fea953f34f30147b60c6b93c68087706d4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:43 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:07 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:07 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:23 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:23 GMT
USER spark
# Fri, 14 Nov 2025 00:40:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:21:15 GMT
USER root
# Fri, 14 Nov 2025 01:21:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:21:15 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9997af0184af5a3eec8b9c31e521431f71ab4219764f54025bded4ac95f540`  
		Last Modified: Tue, 13 Jan 2026 00:58:35 GMT  
		Size: 16.2 MB (16150551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0b6ef10bde275888f1e4eabdf96bf1fb39810178fe9e45884c8d0ee37a6ed`  
		Last Modified: Tue, 13 Jan 2026 00:58:43 GMT  
		Size: 145.0 MB (144977425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc12bfa2e7919efde5fc34c1cf3018da75e1cf252fd1bfee26a392fe8a452b`  
		Last Modified: Tue, 13 Jan 2026 00:58:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d3b3f4cbc4ce873ec58088f789c93e489f329e1ae73f2c915a75412c3179`  
		Last Modified: Tue, 13 Jan 2026 00:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712adf158431f9946962fb99ccd9ef1c1684cbd51303ee663e707fe7565cdd3e`  
		Last Modified: Tue, 13 Jan 2026 01:55:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14953853692245e7b11cea4c9c3caadc89c72d6fa8110f8634ddb49021d861f3`  
		Last Modified: Tue, 13 Jan 2026 01:55:54 GMT  
		Size: 21.8 MB (21847512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb90fd3aceeed484813737477c0b17c4c45184571577f29932a10e8c0d6f534`  
		Last Modified: Tue, 13 Jan 2026 07:26:14 GMT  
		Size: 324.9 MB (324927696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe664390b099dce484c7ab57f87a10495026606ed3f8cfe5be8ceff1fa00658`  
		Last Modified: Tue, 13 Jan 2026 01:56:00 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ed2b86389774845b228ee3dbbaa75b2a9ad02b0d137b40e9f7e5645221c35`  
		Last Modified: Tue, 13 Jan 2026 07:32:46 GMT  
		Size: 118.2 MB (118229155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-python3` - unknown; unknown

```console
$ docker pull spark@sha256:e2198b677a650ec51500f2ac5ec7815a8e2e3fb042cae368c50fc8f45d2f02b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694f5b39362d28c5c51169c890921318e71657ca2d059e5977d171aae23cfbc1`

```dockerfile
```

-	Layers:
	-	`sha256:d6fad832c733c1b30ffa034ae8dd6d65a626b8aa44df1e6b2235f48ef59df244`  
		Last Modified: Thu, 15 Jan 2026 12:09:32 GMT  
		Size: 10.3 MB (10314925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23935aa857de4c5bb5428ee4219f5e1611b2339db5274e77f41676035de4befc`  
		Last Modified: Thu, 15 Jan 2026 12:09:10 GMT  
		Size: 11.0 KB (10973 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:27ace266cd2f246ada7833718da5585188286f114bb10f9826d1e6735444a1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (645970486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9c45e5e577a47f98cbe67943f8c5a91b75360b19fc6757fc60ad6857cfd18`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:20 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:42:10 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:42:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:42:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:42:30 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:42:30 GMT
USER spark
# Fri, 14 Nov 2025 00:42:30 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:37 GMT
USER root
# Fri, 14 Nov 2025 01:37:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:37 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a970ce4b07b68726d7c7d9cf4c1e5c250d429307c71e724a001234cd82c44`  
		Last Modified: Tue, 13 Jan 2026 00:54:38 GMT  
		Size: 16.1 MB (16066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed77fd8d2627057e424752b07749af4fa46c9166dfa1dae49b863c328c34bdb`  
		Last Modified: Tue, 13 Jan 2026 01:54:22 GMT  
		Size: 141.7 MB (141737442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0ad7672facc935673ae17b0ba9af4eb1ff8de6b6f1c320abc46fed0abde8f`  
		Last Modified: Tue, 13 Jan 2026 00:54:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798f1e93315ead6c0269bdaf161c652aad5255cb384e63988571c2f70282579`  
		Last Modified: Tue, 13 Jan 2026 00:54:29 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209a7fd8d4b98af73c15edbfc79a5cc873a8542e09f2a057b32f4b064813e6af`  
		Last Modified: Tue, 13 Jan 2026 12:13:28 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e170feba31806d42f2d3a62ae70d7d795e1b2ac53d80738eff85625e64c41`  
		Last Modified: Tue, 13 Jan 2026 12:13:30 GMT  
		Size: 21.5 MB (21535516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa290ce8600b5f293443b39b35c28288864711e31c5d03feeee2bf3b8f0b5d`  
		Last Modified: Tue, 13 Jan 2026 12:13:45 GMT  
		Size: 324.9 MB (324927648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359710dc95aad6630f000289520cf6d48fb2fba73335ee78b5c2d6c2bc3c17f0`  
		Last Modified: Tue, 13 Jan 2026 12:13:29 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189236b7ecdb4dc58b9dc29a37baa7010a4995bdd34be08f3659e9f9dbd60477`  
		Last Modified: Tue, 13 Jan 2026 12:13:36 GMT  
		Size: 114.3 MB (114313785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-python3` - unknown; unknown

```console
$ docker pull spark@sha256:c4f0897e460c6385d069a2c86b8deb6bc20a636f23ec1e33f191296a3dd6ae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88e64e7fc2da084a64711cbf7f72da0e5cff3e0406675a2c31fed239bb4b5f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec28110373922cd55696179774b8fc7ace61db34ab3b2d94ea990c55fc4f9439`  
		Last Modified: Fri, 14 Nov 2025 01:38:10 GMT  
		Size: 10.3 MB (10309991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edcd4a44dde40b09a1799152ba053058af588b7b2f439fc6c7882e3af5c616ee`  
		Last Modified: Thu, 15 Jan 2026 04:20:29 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-r`

```console
$ docker pull spark@sha256:8527c1782ed6b13043424451e4d5f618a65c4fe81c0f18efaf823d2b6a402d54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-r` - linux; amd64

```console
$ docker pull spark@sha256:efd244a376602e4a4eac471afbeda3a5d1c651dd4ea98d5fdbd4d6c8d0cb1774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.1 MB (861121172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd94dce41fb06c09a0e238157e60f1f107d611b8090e2930a9362bd2fd629036`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:43 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:07 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:07 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:23 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:23 GMT
USER spark
# Fri, 14 Nov 2025 00:40:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:22:20 GMT
USER root
# Fri, 14 Nov 2025 01:22:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:22:20 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:22:20 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9997af0184af5a3eec8b9c31e521431f71ab4219764f54025bded4ac95f540`  
		Last Modified: Tue, 13 Jan 2026 00:58:35 GMT  
		Size: 16.2 MB (16150551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0b6ef10bde275888f1e4eabdf96bf1fb39810178fe9e45884c8d0ee37a6ed`  
		Last Modified: Tue, 13 Jan 2026 00:58:43 GMT  
		Size: 145.0 MB (144977425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc12bfa2e7919efde5fc34c1cf3018da75e1cf252fd1bfee26a392fe8a452b`  
		Last Modified: Tue, 13 Jan 2026 00:58:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d3b3f4cbc4ce873ec58088f789c93e489f329e1ae73f2c915a75412c3179`  
		Last Modified: Tue, 13 Jan 2026 00:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712adf158431f9946962fb99ccd9ef1c1684cbd51303ee663e707fe7565cdd3e`  
		Last Modified: Tue, 13 Jan 2026 01:55:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14953853692245e7b11cea4c9c3caadc89c72d6fa8110f8634ddb49021d861f3`  
		Last Modified: Tue, 13 Jan 2026 01:55:54 GMT  
		Size: 21.8 MB (21847512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb90fd3aceeed484813737477c0b17c4c45184571577f29932a10e8c0d6f534`  
		Last Modified: Tue, 13 Jan 2026 07:26:14 GMT  
		Size: 324.9 MB (324927696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe664390b099dce484c7ab57f87a10495026606ed3f8cfe5be8ceff1fa00658`  
		Last Modified: Tue, 13 Jan 2026 01:56:00 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cd7fe6629e29c03494e2c429f3de27ad8cc2ccb00788db11501c7f77663922`  
		Last Modified: Fri, 14 Nov 2025 01:23:18 GMT  
		Size: 323.7 MB (323675158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-r` - unknown; unknown

```console
$ docker pull spark@sha256:17e6df8a8c31d7d4121ff1d4ec43587c447c3111c8bf8bf9e84d5e910230c4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18513879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c6f67b8c63a5af4949cda24d5e4632795d38d74fe2a0b5d099253251177dc1`

```dockerfile
```

-	Layers:
	-	`sha256:8ff5aafb5d9f18234b7ac1a6ea344ed10086b9f6b61eff1a7f55a7baea997a2c`  
		Last Modified: Fri, 14 Nov 2025 01:23:11 GMT  
		Size: 18.5 MB (18503210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:966d49607e05a4ba526ccb96d42c38984d23fa9a7724b230ff1fdecbf3287da1`  
		Last Modified: Fri, 14 Nov 2025 01:23:10 GMT  
		Size: 10.7 KB (10669 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:0f97ff141bf6e2ba955f23abd3ca15a34cbaa55bd7ba845c36bd80b599ff46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 MB (840067867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98321fa9e4a72bd092ca7f77c2448478c39bb6f34d783bfe1487423b44888536`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:20 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:42:10 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:42:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:42:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:42:30 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:42:30 GMT
USER spark
# Fri, 14 Nov 2025 00:42:30 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:38:24 GMT
USER root
# Fri, 14 Nov 2025 01:38:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:38:24 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:38:24 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a970ce4b07b68726d7c7d9cf4c1e5c250d429307c71e724a001234cd82c44`  
		Last Modified: Tue, 13 Jan 2026 00:54:38 GMT  
		Size: 16.1 MB (16066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed77fd8d2627057e424752b07749af4fa46c9166dfa1dae49b863c328c34bdb`  
		Last Modified: Tue, 13 Jan 2026 01:54:22 GMT  
		Size: 141.7 MB (141737442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0ad7672facc935673ae17b0ba9af4eb1ff8de6b6f1c320abc46fed0abde8f`  
		Last Modified: Tue, 13 Jan 2026 00:54:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798f1e93315ead6c0269bdaf161c652aad5255cb384e63988571c2f70282579`  
		Last Modified: Tue, 13 Jan 2026 00:54:29 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209a7fd8d4b98af73c15edbfc79a5cc873a8542e09f2a057b32f4b064813e6af`  
		Last Modified: Tue, 13 Jan 2026 12:13:28 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e170feba31806d42f2d3a62ae70d7d795e1b2ac53d80738eff85625e64c41`  
		Last Modified: Tue, 13 Jan 2026 12:13:30 GMT  
		Size: 21.5 MB (21535516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa290ce8600b5f293443b39b35c28288864711e31c5d03feeee2bf3b8f0b5d`  
		Last Modified: Tue, 13 Jan 2026 12:13:45 GMT  
		Size: 324.9 MB (324927648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359710dc95aad6630f000289520cf6d48fb2fba73335ee78b5c2d6c2bc3c17f0`  
		Last Modified: Tue, 13 Jan 2026 12:13:29 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393ecd9bde121856eff58935f453c4655c3416a63db51df01c0a8d884aad73e7`  
		Last Modified: Fri, 14 Nov 2025 01:39:23 GMT  
		Size: 308.4 MB (308411166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-r` - unknown; unknown

```console
$ docker pull spark@sha256:09f3774b4552369eef675d51d0a415398698c389d639fd4b7e6dc3b8467abd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18479130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb0b69c6879a5ffd3a285ec7af9232bb5c2e39c2d1f02b588c1b49c0c23735a`

```dockerfile
```

-	Layers:
	-	`sha256:75c649b68801a5346737d5179f420b20f59617d60fc2d7915bb000d890c4d5c1`  
		Last Modified: Fri, 14 Nov 2025 01:39:18 GMT  
		Size: 18.5 MB (18468381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ba84cf9eeaa7d8e5e4df99ad179d0d327b02eff670f22581d2e3b5204ae2f7`  
		Last Modified: Fri, 14 Nov 2025 01:39:17 GMT  
		Size: 10.7 KB (10749 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala`

```console
$ docker pull spark@sha256:5d719873be72bde9955b8e9883c0a1481e7d99ce1b93febaff4a5e51d659998f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala` - linux; amd64

```console
$ docker pull spark@sha256:693ed54f5f55d1f0865335616ea0c01b13430fbed56e6322dadab243c4b7e8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.4 MB (537442954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f90fb45b27fd3db26e8fc99c25b711b7542c31cf6c6ff48af4f153b5f794bc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:18:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:18:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:18:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:18:54 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:02 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:09:33 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:09:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:09:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:09:45 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:09:53 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:09:54 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:09:54 GMT
USER spark
# Fri, 16 Jan 2026 01:09:54 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4cee3d5f1b89b96e8fff031dd86e71ff9da83c4946e0857d560048fa5fec74`  
		Last Modified: Thu, 15 Jan 2026 22:19:29 GMT  
		Size: 16.1 MB (16147489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cde85ba2de15bdf5f330c169d71fdd5b570420a47cd2c3cf826e2305abe0c1`  
		Last Modified: Thu, 15 Jan 2026 22:21:23 GMT  
		Size: 145.0 MB (144977521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d63977c411640a7d0a43e7a20297afa10ac2c6dc85ef0c2f65aa20f4ddb6171`  
		Last Modified: Thu, 15 Jan 2026 22:19:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a15ca2227fa162e039637f8ec5d82c039e2b4ca2bc43e3f77e36c74aa754b0d`  
		Last Modified: Thu, 15 Jan 2026 22:19:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea54fcc91296c26971334108f68dd41f0e5528d16c78b00791bde0fa045ee30`  
		Last Modified: Fri, 16 Jan 2026 01:13:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62c54dad5c577fb735117fb0b51601156a907a1430e694764158e9a4b3a5059`  
		Last Modified: Fri, 16 Jan 2026 02:22:56 GMT  
		Size: 21.8 MB (21847556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04dfe659543e31212072536f1fb210a5dcec2bbafd1adce5c4458ec0e7413d`  
		Last Modified: Fri, 16 Jan 2026 01:14:21 GMT  
		Size: 324.9 MB (324927691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5aff7a9f05ec1b3853a861bb61f770031fb032c7945502a9934d021f53fbb1`  
		Last Modified: Fri, 16 Jan 2026 01:13:40 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala` - unknown; unknown

```console
$ docker pull spark@sha256:5ccc9989835c63c7c3b7d5b267b5f787bfe8d3ca7de16ce152359f2907056f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e71ee24d00a947d5bb4eebb8b46d040b600efc3dacb7fa28c987819d579ae4`

```dockerfile
```

-	Layers:
	-	`sha256:7d0294a009426ca4981b8ea879ba50a00d5f62f8d5b4ff45995539ef5594bef0`  
		Last Modified: Fri, 16 Jan 2026 03:12:44 GMT  
		Size: 4.7 MB (4695589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5145caa35de5e174032e5ef39fed1cd2309e98a89103c4ea4760f45bc8c5d69e`  
		Last Modified: Fri, 16 Jan 2026 03:12:45 GMT  
		Size: 22.9 KB (22949 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:3f976c91fc5074f1cb0ede2ffa49d34b708af28bc8eb5ada17216daf5cafcd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.7 MB (531655805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6612f572189f88864eeb748bfa11e2954cb8b7ccdc19c539ed791b1e4a3dbb80`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:00 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:08 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:13:26 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:13:26 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:13:35 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:13:35 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:13:44 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:13:44 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:13:44 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:13:44 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:13:44 GMT
USER spark
# Fri, 16 Jan 2026 01:13:44 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed683be0c0112753a3cbd430d1090f3be2f81699aaa5e7f55374220c1102da06`  
		Last Modified: Thu, 15 Jan 2026 22:19:35 GMT  
		Size: 16.1 MB (16065812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e54d506f4b37b818f77d4774d549eae26b37db3ff20fd5dd15d9d55fd0b1a6`  
		Last Modified: Fri, 16 Jan 2026 00:04:57 GMT  
		Size: 141.7 MB (141737466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531f77d5ded81823943a5f77829b2138a6b8080324b21043144bf4cfd8ad7677`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a606e3fc494a2c56340614266a25ee62ecb705bdb4ca8c2aa387158e7e8ef1f4`  
		Last Modified: Thu, 15 Jan 2026 22:19:35 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d273b5bd89b4535389e49a308fac7ac5b12e0e6f853bb688fbe8c95cd7e6deb8`  
		Last Modified: Fri, 16 Jan 2026 01:14:20 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e9c66b58b4ea4c2f5c83d2f93b6c4c420a990e63d47e1cce8a32b8b6ba1de6`  
		Last Modified: Fri, 16 Jan 2026 01:14:22 GMT  
		Size: 21.5 MB (21535377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31495597488988392314cfced7d8a3ea414a0836d7568fd23ebd92e90564e5c3`  
		Last Modified: Fri, 16 Jan 2026 01:14:33 GMT  
		Size: 324.9 MB (324927623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ce896bb4787ad0b4d43b303d35ea73a334d0206214f596ba2facddbe39eb2`  
		Last Modified: Fri, 16 Jan 2026 01:14:20 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala` - unknown; unknown

```console
$ docker pull spark@sha256:b36cd7bdaa2f57e9a12f23df1c50fc89c227d762df945ca36da7c9e3a58451e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82cbcbbf88d117734db62458c01c034974dc0483d66d23b465283802013e8a8`

```dockerfile
```

-	Layers:
	-	`sha256:b64e55c8739e9db9b6561e1aafeed77378818252f86f2dfed57b5206ff4bd417`  
		Last Modified: Fri, 16 Jan 2026 03:12:50 GMT  
		Size: 4.7 MB (4695908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a55ee6d543611b41c4f1fccdd23419fc718156263c5f2eca0a5a0d4e48a69e`  
		Last Modified: Fri, 16 Jan 2026 03:12:51 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:c29af9e2e4173e883b139f6d81bc8b20c8a9792afc56b42fe9d01eddbc1ea81e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a65a78b3997ebe219f98e0602ca93b4b9f423b6f7dadfeaa5d66023de254b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.9 MB (875861568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a615e9bfb075dd549e67dcfb42de0cf083cabe3966441f644ec6f9f8c8f1b67`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:43 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:07 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:07 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:23 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:23 GMT
USER spark
# Fri, 14 Nov 2025 00:40:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:18:25 GMT
USER root
# Fri, 14 Nov 2025 01:18:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:25 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:18:25 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9997af0184af5a3eec8b9c31e521431f71ab4219764f54025bded4ac95f540`  
		Last Modified: Tue, 13 Jan 2026 00:58:35 GMT  
		Size: 16.2 MB (16150551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0b6ef10bde275888f1e4eabdf96bf1fb39810178fe9e45884c8d0ee37a6ed`  
		Last Modified: Tue, 13 Jan 2026 00:58:43 GMT  
		Size: 145.0 MB (144977425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc12bfa2e7919efde5fc34c1cf3018da75e1cf252fd1bfee26a392fe8a452b`  
		Last Modified: Tue, 13 Jan 2026 00:58:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d3b3f4cbc4ce873ec58088f789c93e489f329e1ae73f2c915a75412c3179`  
		Last Modified: Tue, 13 Jan 2026 00:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712adf158431f9946962fb99ccd9ef1c1684cbd51303ee663e707fe7565cdd3e`  
		Last Modified: Tue, 13 Jan 2026 01:55:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14953853692245e7b11cea4c9c3caadc89c72d6fa8110f8634ddb49021d861f3`  
		Last Modified: Tue, 13 Jan 2026 01:55:54 GMT  
		Size: 21.8 MB (21847512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb90fd3aceeed484813737477c0b17c4c45184571577f29932a10e8c0d6f534`  
		Last Modified: Tue, 13 Jan 2026 07:26:14 GMT  
		Size: 324.9 MB (324927696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe664390b099dce484c7ab57f87a10495026606ed3f8cfe5be8ceff1fa00658`  
		Last Modified: Tue, 13 Jan 2026 01:56:00 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b432835a25c81d5298e6ec11e38718721a163e79cd5cb67ae94d67ce37ce6a88`  
		Last Modified: Wed, 14 Jan 2026 08:39:46 GMT  
		Size: 338.4 MB (338415554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d4bddd272202a06e8e540d63d8e4055734915ee9f917992e8e8f1e9fe5f086c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19559916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869676bf60cecd295884c8556b96695cbfd4ac9a7ff2b344ee5226d5df15c4d3`

```dockerfile
```

-	Layers:
	-	`sha256:a7ba4d05edf224fdf3f93d94b92caa6b611efed75f82213f2665e73284a02c38`  
		Last Modified: Fri, 14 Nov 2025 01:19:19 GMT  
		Size: 19.5 MB (19549369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25b334ca13ea1ce5238345a8200d11653c3ef73675556ad87c3a5933658d9cc`  
		Last Modified: Fri, 14 Nov 2025 01:19:18 GMT  
		Size: 10.5 KB (10547 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2573c331d882ac4b90871a8e000cb2ae75c270dbfb5c0a503a5e750b0d610a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 MB (854628249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a296d5a4ff5a2158e0368f895c3fa2bd3a812f1558ff322835f5dfcb02fb644b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:20 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:42:10 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:42:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:42:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:42:30 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:42:30 GMT
USER spark
# Fri, 14 Nov 2025 00:42:30 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:34:35 GMT
USER root
# Fri, 14 Nov 2025 01:34:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:35 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:34:35 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a970ce4b07b68726d7c7d9cf4c1e5c250d429307c71e724a001234cd82c44`  
		Last Modified: Tue, 13 Jan 2026 00:54:38 GMT  
		Size: 16.1 MB (16066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed77fd8d2627057e424752b07749af4fa46c9166dfa1dae49b863c328c34bdb`  
		Last Modified: Tue, 13 Jan 2026 01:54:22 GMT  
		Size: 141.7 MB (141737442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0ad7672facc935673ae17b0ba9af4eb1ff8de6b6f1c320abc46fed0abde8f`  
		Last Modified: Tue, 13 Jan 2026 00:54:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798f1e93315ead6c0269bdaf161c652aad5255cb384e63988571c2f70282579`  
		Last Modified: Tue, 13 Jan 2026 00:54:29 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209a7fd8d4b98af73c15edbfc79a5cc873a8542e09f2a057b32f4b064813e6af`  
		Last Modified: Tue, 13 Jan 2026 12:13:28 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e170feba31806d42f2d3a62ae70d7d795e1b2ac53d80738eff85625e64c41`  
		Last Modified: Tue, 13 Jan 2026 12:13:30 GMT  
		Size: 21.5 MB (21535516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa290ce8600b5f293443b39b35c28288864711e31c5d03feeee2bf3b8f0b5d`  
		Last Modified: Tue, 13 Jan 2026 12:13:45 GMT  
		Size: 324.9 MB (324927648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359710dc95aad6630f000289520cf6d48fb2fba73335ee78b5c2d6c2bc3c17f0`  
		Last Modified: Tue, 13 Jan 2026 12:13:29 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf08ceb2942d60d73a058d2dc82586827df26eed6e677e0f82d60e8a2e10ded`  
		Last Modified: Tue, 25 Nov 2025 19:08:12 GMT  
		Size: 323.0 MB (322971548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:90512f8666064f33fe1ccbacb7aaa78025c02607dada5a7a852bdd4da41214b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19525167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eed72bc64046c93c403c8a760bc42ff1619528b1def52ecd583a73ed6abb7d3`

```dockerfile
```

-	Layers:
	-	`sha256:54dd87456ef60551439c0a724d5df69c119e3148a3e07677dc5e9915c49928d5`  
		Last Modified: Fri, 14 Nov 2025 01:35:34 GMT  
		Size: 19.5 MB (19514552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f32ed3f6844003bcdb3f3924d2f1b0c09dbc291903583fefe07acd0198bf3c`  
		Last Modified: Fri, 14 Nov 2025 01:35:33 GMT  
		Size: 10.6 KB (10615 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:bc10f25ccbac0e6e9f131a3f369da6e865a2765300ca0c171b81c7d4499ff727
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:c1148460dd3cb5e42475c6dba634a267074af65bea2c78736367bb5f5eff41da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 MB (655675169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd92d38b1d5d9ab51dbeffa29dbb1fea953f34f30147b60c6b93c68087706d4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:43 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:07 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:07 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:23 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:23 GMT
USER spark
# Fri, 14 Nov 2025 00:40:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:21:15 GMT
USER root
# Fri, 14 Nov 2025 01:21:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:21:15 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9997af0184af5a3eec8b9c31e521431f71ab4219764f54025bded4ac95f540`  
		Last Modified: Tue, 13 Jan 2026 00:58:35 GMT  
		Size: 16.2 MB (16150551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0b6ef10bde275888f1e4eabdf96bf1fb39810178fe9e45884c8d0ee37a6ed`  
		Last Modified: Tue, 13 Jan 2026 00:58:43 GMT  
		Size: 145.0 MB (144977425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc12bfa2e7919efde5fc34c1cf3018da75e1cf252fd1bfee26a392fe8a452b`  
		Last Modified: Tue, 13 Jan 2026 00:58:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d3b3f4cbc4ce873ec58088f789c93e489f329e1ae73f2c915a75412c3179`  
		Last Modified: Tue, 13 Jan 2026 00:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712adf158431f9946962fb99ccd9ef1c1684cbd51303ee663e707fe7565cdd3e`  
		Last Modified: Tue, 13 Jan 2026 01:55:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14953853692245e7b11cea4c9c3caadc89c72d6fa8110f8634ddb49021d861f3`  
		Last Modified: Tue, 13 Jan 2026 01:55:54 GMT  
		Size: 21.8 MB (21847512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb90fd3aceeed484813737477c0b17c4c45184571577f29932a10e8c0d6f534`  
		Last Modified: Tue, 13 Jan 2026 07:26:14 GMT  
		Size: 324.9 MB (324927696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe664390b099dce484c7ab57f87a10495026606ed3f8cfe5be8ceff1fa00658`  
		Last Modified: Tue, 13 Jan 2026 01:56:00 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ed2b86389774845b228ee3dbbaa75b2a9ad02b0d137b40e9f7e5645221c35`  
		Last Modified: Tue, 13 Jan 2026 07:32:46 GMT  
		Size: 118.2 MB (118229155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e2198b677a650ec51500f2ac5ec7815a8e2e3fb042cae368c50fc8f45d2f02b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694f5b39362d28c5c51169c890921318e71657ca2d059e5977d171aae23cfbc1`

```dockerfile
```

-	Layers:
	-	`sha256:d6fad832c733c1b30ffa034ae8dd6d65a626b8aa44df1e6b2235f48ef59df244`  
		Last Modified: Thu, 15 Jan 2026 12:09:32 GMT  
		Size: 10.3 MB (10314925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23935aa857de4c5bb5428ee4219f5e1611b2339db5274e77f41676035de4befc`  
		Last Modified: Thu, 15 Jan 2026 12:09:10 GMT  
		Size: 11.0 KB (10973 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:27ace266cd2f246ada7833718da5585188286f114bb10f9826d1e6735444a1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (645970486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9c45e5e577a47f98cbe67943f8c5a91b75360b19fc6757fc60ad6857cfd18`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:20 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:42:10 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:42:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:42:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:42:30 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:42:30 GMT
USER spark
# Fri, 14 Nov 2025 00:42:30 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:37 GMT
USER root
# Fri, 14 Nov 2025 01:37:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:37 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a970ce4b07b68726d7c7d9cf4c1e5c250d429307c71e724a001234cd82c44`  
		Last Modified: Tue, 13 Jan 2026 00:54:38 GMT  
		Size: 16.1 MB (16066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed77fd8d2627057e424752b07749af4fa46c9166dfa1dae49b863c328c34bdb`  
		Last Modified: Tue, 13 Jan 2026 01:54:22 GMT  
		Size: 141.7 MB (141737442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0ad7672facc935673ae17b0ba9af4eb1ff8de6b6f1c320abc46fed0abde8f`  
		Last Modified: Tue, 13 Jan 2026 00:54:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798f1e93315ead6c0269bdaf161c652aad5255cb384e63988571c2f70282579`  
		Last Modified: Tue, 13 Jan 2026 00:54:29 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209a7fd8d4b98af73c15edbfc79a5cc873a8542e09f2a057b32f4b064813e6af`  
		Last Modified: Tue, 13 Jan 2026 12:13:28 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e170feba31806d42f2d3a62ae70d7d795e1b2ac53d80738eff85625e64c41`  
		Last Modified: Tue, 13 Jan 2026 12:13:30 GMT  
		Size: 21.5 MB (21535516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa290ce8600b5f293443b39b35c28288864711e31c5d03feeee2bf3b8f0b5d`  
		Last Modified: Tue, 13 Jan 2026 12:13:45 GMT  
		Size: 324.9 MB (324927648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359710dc95aad6630f000289520cf6d48fb2fba73335ee78b5c2d6c2bc3c17f0`  
		Last Modified: Tue, 13 Jan 2026 12:13:29 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189236b7ecdb4dc58b9dc29a37baa7010a4995bdd34be08f3659e9f9dbd60477`  
		Last Modified: Tue, 13 Jan 2026 12:13:36 GMT  
		Size: 114.3 MB (114313785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c4f0897e460c6385d069a2c86b8deb6bc20a636f23ec1e33f191296a3dd6ae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88e64e7fc2da084a64711cbf7f72da0e5cff3e0406675a2c31fed239bb4b5f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec28110373922cd55696179774b8fc7ace61db34ab3b2d94ea990c55fc4f9439`  
		Last Modified: Fri, 14 Nov 2025 01:38:10 GMT  
		Size: 10.3 MB (10309991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edcd4a44dde40b09a1799152ba053058af588b7b2f439fc6c7882e3af5c616ee`  
		Last Modified: Thu, 15 Jan 2026 04:20:29 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:8527c1782ed6b13043424451e4d5f618a65c4fe81c0f18efaf823d2b6a402d54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:efd244a376602e4a4eac471afbeda3a5d1c651dd4ea98d5fdbd4d6c8d0cb1774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.1 MB (861121172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd94dce41fb06c09a0e238157e60f1f107d611b8090e2930a9362bd2fd629036`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:43 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:07 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:07 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:23 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:23 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:23 GMT
USER spark
# Fri, 14 Nov 2025 00:40:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:22:20 GMT
USER root
# Fri, 14 Nov 2025 01:22:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:22:20 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:22:20 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9997af0184af5a3eec8b9c31e521431f71ab4219764f54025bded4ac95f540`  
		Last Modified: Tue, 13 Jan 2026 00:58:35 GMT  
		Size: 16.2 MB (16150551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0b6ef10bde275888f1e4eabdf96bf1fb39810178fe9e45884c8d0ee37a6ed`  
		Last Modified: Tue, 13 Jan 2026 00:58:43 GMT  
		Size: 145.0 MB (144977425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc12bfa2e7919efde5fc34c1cf3018da75e1cf252fd1bfee26a392fe8a452b`  
		Last Modified: Tue, 13 Jan 2026 00:58:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d3b3f4cbc4ce873ec58088f789c93e489f329e1ae73f2c915a75412c3179`  
		Last Modified: Tue, 13 Jan 2026 00:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712adf158431f9946962fb99ccd9ef1c1684cbd51303ee663e707fe7565cdd3e`  
		Last Modified: Tue, 13 Jan 2026 01:55:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14953853692245e7b11cea4c9c3caadc89c72d6fa8110f8634ddb49021d861f3`  
		Last Modified: Tue, 13 Jan 2026 01:55:54 GMT  
		Size: 21.8 MB (21847512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb90fd3aceeed484813737477c0b17c4c45184571577f29932a10e8c0d6f534`  
		Last Modified: Tue, 13 Jan 2026 07:26:14 GMT  
		Size: 324.9 MB (324927696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe664390b099dce484c7ab57f87a10495026606ed3f8cfe5be8ceff1fa00658`  
		Last Modified: Tue, 13 Jan 2026 01:56:00 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cd7fe6629e29c03494e2c429f3de27ad8cc2ccb00788db11501c7f77663922`  
		Last Modified: Fri, 14 Nov 2025 01:23:18 GMT  
		Size: 323.7 MB (323675158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:17e6df8a8c31d7d4121ff1d4ec43587c447c3111c8bf8bf9e84d5e910230c4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18513879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c6f67b8c63a5af4949cda24d5e4632795d38d74fe2a0b5d099253251177dc1`

```dockerfile
```

-	Layers:
	-	`sha256:8ff5aafb5d9f18234b7ac1a6ea344ed10086b9f6b61eff1a7f55a7baea997a2c`  
		Last Modified: Fri, 14 Nov 2025 01:23:11 GMT  
		Size: 18.5 MB (18503210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:966d49607e05a4ba526ccb96d42c38984d23fa9a7724b230ff1fdecbf3287da1`  
		Last Modified: Fri, 14 Nov 2025 01:23:10 GMT  
		Size: 10.7 KB (10669 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:0f97ff141bf6e2ba955f23abd3ca15a34cbaa55bd7ba845c36bd80b599ff46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 MB (840067867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98321fa9e4a72bd092ca7f77c2448478c39bb6f34d783bfe1487423b44888536`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:20 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:42:10 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:42:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:42:20 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:42:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:42:30 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:42:30 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:42:30 GMT
USER spark
# Fri, 14 Nov 2025 00:42:30 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:38:24 GMT
USER root
# Fri, 14 Nov 2025 01:38:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:38:24 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:38:24 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a970ce4b07b68726d7c7d9cf4c1e5c250d429307c71e724a001234cd82c44`  
		Last Modified: Tue, 13 Jan 2026 00:54:38 GMT  
		Size: 16.1 MB (16066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed77fd8d2627057e424752b07749af4fa46c9166dfa1dae49b863c328c34bdb`  
		Last Modified: Tue, 13 Jan 2026 01:54:22 GMT  
		Size: 141.7 MB (141737442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0ad7672facc935673ae17b0ba9af4eb1ff8de6b6f1c320abc46fed0abde8f`  
		Last Modified: Tue, 13 Jan 2026 00:54:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798f1e93315ead6c0269bdaf161c652aad5255cb384e63988571c2f70282579`  
		Last Modified: Tue, 13 Jan 2026 00:54:29 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209a7fd8d4b98af73c15edbfc79a5cc873a8542e09f2a057b32f4b064813e6af`  
		Last Modified: Tue, 13 Jan 2026 12:13:28 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e170feba31806d42f2d3a62ae70d7d795e1b2ac53d80738eff85625e64c41`  
		Last Modified: Tue, 13 Jan 2026 12:13:30 GMT  
		Size: 21.5 MB (21535516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa290ce8600b5f293443b39b35c28288864711e31c5d03feeee2bf3b8f0b5d`  
		Last Modified: Tue, 13 Jan 2026 12:13:45 GMT  
		Size: 324.9 MB (324927648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359710dc95aad6630f000289520cf6d48fb2fba73335ee78b5c2d6c2bc3c17f0`  
		Last Modified: Tue, 13 Jan 2026 12:13:29 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393ecd9bde121856eff58935f453c4655c3416a63db51df01c0a8d884aad73e7`  
		Last Modified: Fri, 14 Nov 2025 01:39:23 GMT  
		Size: 308.4 MB (308411166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:09f3774b4552369eef675d51d0a415398698c389d639fd4b7e6dc3b8467abd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18479130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb0b69c6879a5ffd3a285ec7af9232bb5c2e39c2d1f02b588c1b49c0c23735a`

```dockerfile
```

-	Layers:
	-	`sha256:75c649b68801a5346737d5179f420b20f59617d60fc2d7915bb000d890c4d5c1`  
		Last Modified: Fri, 14 Nov 2025 01:39:18 GMT  
		Size: 18.5 MB (18468381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ba84cf9eeaa7d8e5e4df99ad179d0d327b02eff670f22581d2e3b5204ae2f7`  
		Last Modified: Fri, 14 Nov 2025 01:39:17 GMT  
		Size: 10.7 KB (10749 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:5d719873be72bde9955b8e9883c0a1481e7d99ce1b93febaff4a5e51d659998f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:693ed54f5f55d1f0865335616ea0c01b13430fbed56e6322dadab243c4b7e8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.4 MB (537442954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f90fb45b27fd3db26e8fc99c25b711b7542c31cf6c6ff48af4f153b5f794bc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:18:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:18:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:18:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:18:54 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:02 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:09:33 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:09:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:09:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:09:45 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:09:53 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:09:54 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:09:54 GMT
USER spark
# Fri, 16 Jan 2026 01:09:54 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4cee3d5f1b89b96e8fff031dd86e71ff9da83c4946e0857d560048fa5fec74`  
		Last Modified: Thu, 15 Jan 2026 22:19:29 GMT  
		Size: 16.1 MB (16147489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cde85ba2de15bdf5f330c169d71fdd5b570420a47cd2c3cf826e2305abe0c1`  
		Last Modified: Thu, 15 Jan 2026 22:21:23 GMT  
		Size: 145.0 MB (144977521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d63977c411640a7d0a43e7a20297afa10ac2c6dc85ef0c2f65aa20f4ddb6171`  
		Last Modified: Thu, 15 Jan 2026 22:19:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a15ca2227fa162e039637f8ec5d82c039e2b4ca2bc43e3f77e36c74aa754b0d`  
		Last Modified: Thu, 15 Jan 2026 22:19:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea54fcc91296c26971334108f68dd41f0e5528d16c78b00791bde0fa045ee30`  
		Last Modified: Fri, 16 Jan 2026 01:13:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62c54dad5c577fb735117fb0b51601156a907a1430e694764158e9a4b3a5059`  
		Last Modified: Fri, 16 Jan 2026 02:22:56 GMT  
		Size: 21.8 MB (21847556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04dfe659543e31212072536f1fb210a5dcec2bbafd1adce5c4458ec0e7413d`  
		Last Modified: Fri, 16 Jan 2026 01:14:21 GMT  
		Size: 324.9 MB (324927691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5aff7a9f05ec1b3853a861bb61f770031fb032c7945502a9934d021f53fbb1`  
		Last Modified: Fri, 16 Jan 2026 01:13:40 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5ccc9989835c63c7c3b7d5b267b5f787bfe8d3ca7de16ce152359f2907056f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e71ee24d00a947d5bb4eebb8b46d040b600efc3dacb7fa28c987819d579ae4`

```dockerfile
```

-	Layers:
	-	`sha256:7d0294a009426ca4981b8ea879ba50a00d5f62f8d5b4ff45995539ef5594bef0`  
		Last Modified: Fri, 16 Jan 2026 03:12:44 GMT  
		Size: 4.7 MB (4695589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5145caa35de5e174032e5ef39fed1cd2309e98a89103c4ea4760f45bc8c5d69e`  
		Last Modified: Fri, 16 Jan 2026 03:12:45 GMT  
		Size: 22.9 KB (22949 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:3f976c91fc5074f1cb0ede2ffa49d34b708af28bc8eb5ada17216daf5cafcd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.7 MB (531655805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6612f572189f88864eeb748bfa11e2954cb8b7ccdc19c539ed791b1e4a3dbb80`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:00 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:08 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:13:26 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:13:26 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:13:35 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:13:35 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:13:44 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:13:44 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:13:44 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:13:44 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:13:44 GMT
USER spark
# Fri, 16 Jan 2026 01:13:44 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed683be0c0112753a3cbd430d1090f3be2f81699aaa5e7f55374220c1102da06`  
		Last Modified: Thu, 15 Jan 2026 22:19:35 GMT  
		Size: 16.1 MB (16065812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e54d506f4b37b818f77d4774d549eae26b37db3ff20fd5dd15d9d55fd0b1a6`  
		Last Modified: Fri, 16 Jan 2026 00:04:57 GMT  
		Size: 141.7 MB (141737466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531f77d5ded81823943a5f77829b2138a6b8080324b21043144bf4cfd8ad7677`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a606e3fc494a2c56340614266a25ee62ecb705bdb4ca8c2aa387158e7e8ef1f4`  
		Last Modified: Thu, 15 Jan 2026 22:19:35 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d273b5bd89b4535389e49a308fac7ac5b12e0e6f853bb688fbe8c95cd7e6deb8`  
		Last Modified: Fri, 16 Jan 2026 01:14:20 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e9c66b58b4ea4c2f5c83d2f93b6c4c420a990e63d47e1cce8a32b8b6ba1de6`  
		Last Modified: Fri, 16 Jan 2026 01:14:22 GMT  
		Size: 21.5 MB (21535377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31495597488988392314cfced7d8a3ea414a0836d7568fd23ebd92e90564e5c3`  
		Last Modified: Fri, 16 Jan 2026 01:14:33 GMT  
		Size: 324.9 MB (324927623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ce896bb4787ad0b4d43b303d35ea73a334d0206214f596ba2facddbe39eb2`  
		Last Modified: Fri, 16 Jan 2026 01:14:20 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b36cd7bdaa2f57e9a12f23df1c50fc89c227d762df945ca36da7c9e3a58451e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82cbcbbf88d117734db62458c01c034974dc0483d66d23b465283802013e8a8`

```dockerfile
```

-	Layers:
	-	`sha256:b64e55c8739e9db9b6561e1aafeed77378818252f86f2dfed57b5206ff4bd417`  
		Last Modified: Fri, 16 Jan 2026 03:12:50 GMT  
		Size: 4.7 MB (4695908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a55ee6d543611b41c4f1fccdd23419fc718156263c5f2eca0a5a0d4e48a69e`  
		Last Modified: Fri, 16 Jan 2026 03:12:51 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:76b88f105b3239a1b96f2f92567c94bec9b3144436c052a04d63e91f895c4c96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:786e3fb4eaec19e375e3be908efe24ac0689c8f49a4977ec87310547c8a6ea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 MB (875737367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbaa918ff44fefaefb94904978c4004651a089cb974d94a1013e9fc1490b6b4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:03 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:03 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:03 GMT
USER spark
# Fri, 14 Nov 2025 00:40:03 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:17:52 GMT
USER root
# Fri, 14 Nov 2025 01:17:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:52 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:17:52 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ddc142dbd294d1861ba917801969cddd78edae3050e0abe0153b39ea3722e0`  
		Last Modified: Tue, 13 Jan 2026 02:27:44 GMT  
		Size: 21.9 MB (21850558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6f43adf3d8d5ac8048ad3d28d3140461ab08ff548611f3e549653bcf0f86e`  
		Last Modified: Tue, 13 Jan 2026 03:41:33 GMT  
		Size: 324.9 MB (324927670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21d6393c00ceffcb23b76c01584309a96fb6e976dd6aa974e27772112dde9d`  
		Last Modified: Tue, 13 Jan 2026 02:27:51 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e35a6424a1345f1bd1cd4ecf622830c50dd69880103aef149c69015e041c12`  
		Last Modified: Tue, 13 Jan 2026 18:07:48 GMT  
		Size: 333.9 MB (333863942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b27d8da5421b4722a4cc8510aba6c02537fa0bddf4ca5f4cd0962490702965f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59bc576b50d15d56c97036c309283334c39c575ee832bdde98540a0c5d459e4`

```dockerfile
```

-	Layers:
	-	`sha256:634c815bd0b7ae981a68d3abee2c5a19639ed9da8822af4a22b2c3e5e3ebc9b4`  
		Last Modified: Thu, 15 Jan 2026 19:42:52 GMT  
		Size: 19.5 MB (19529230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ed8d0109b0eaa4c188535197dcd4faaec8139097d25e2023cf2955c7544d3e`  
		Last Modified: Thu, 15 Jan 2026 19:42:51 GMT  
		Size: 10.5 KB (10547 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:33083767e0ea1fe9c26fe46ae8d30df05bc9c0f438aeed2ff2758ee302a42d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 MB (856583734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59f86b3ff983713103c52dfabdef4640513ca6e8d08f173395ddaf2f44d82d7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:41:52 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:52 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:52 GMT
USER spark
# Fri, 14 Nov 2025 00:41:52 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:34:54 GMT
USER root
# Fri, 14 Nov 2025 01:34:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:54 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:34:54 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a2d7b006aa25763b9e6edd46f17d2069567773314a5077991ec87d2b170a6`  
		Last Modified: Tue, 13 Jan 2026 11:29:15 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b3dbef2ce366da1ade8376fcad6bff5e0d39d87b4a7d9e6e635bbfeb30a173`  
		Last Modified: Tue, 13 Jan 2026 11:29:35 GMT  
		Size: 21.5 MB (21537971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035bcc6536920fedae222ca7c8add833bd67dc5739c25cdd7caaadd09249a18`  
		Last Modified: Tue, 13 Jan 2026 11:30:08 GMT  
		Size: 324.9 MB (324927659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134b18b042cae2e6c65253efcb1add53663a5cc729b915923070f36487e141b2`  
		Last Modified: Tue, 13 Jan 2026 11:29:16 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753c1f044ec09e07ffd97b2591aceb810d48941868a08064aab9ac20145c0547`  
		Last Modified: Fri, 14 Nov 2025 01:35:56 GMT  
		Size: 317.0 MB (316953998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c8d0690dd54210df5930ac1ba16f26fe7f8c7173b661df133af95f3398d3eb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19504411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685f8687aefd3411caaac193ce75f4c143c47be6f2baec2b99d3041ff97be733`

```dockerfile
```

-	Layers:
	-	`sha256:0862084db7e39074c3e41a6500f574f0019116d67a1c854616b8d5c981f5a66b`  
		Last Modified: Fri, 14 Nov 2025 01:35:50 GMT  
		Size: 19.5 MB (19493795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b275a524ba18a1e4e24a47f2e75d04d391b00de52254b725d05e89dbc9f287a6`  
		Last Modified: Fri, 14 Nov 2025 01:35:49 GMT  
		Size: 10.6 KB (10616 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:31a8c385283050d7a756634f23e0f3cddde0131a6c8ad6a6b20b05d94bc1d472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:def686569eaa28c79f23f92c6eb2a711248c113a028a3f20eafeb9474fe96104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 MB (655560130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a841694b4855726107822e6155eccff688aa2cef6a9a47ddaded82f5f22b6c2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:03 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:03 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:03 GMT
USER spark
# Fri, 14 Nov 2025 00:40:03 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:36 GMT
USER root
# Fri, 14 Nov 2025 01:20:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:36 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ddc142dbd294d1861ba917801969cddd78edae3050e0abe0153b39ea3722e0`  
		Last Modified: Tue, 13 Jan 2026 02:27:44 GMT  
		Size: 21.9 MB (21850558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6f43adf3d8d5ac8048ad3d28d3140461ab08ff548611f3e549653bcf0f86e`  
		Last Modified: Tue, 13 Jan 2026 03:41:33 GMT  
		Size: 324.9 MB (324927670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21d6393c00ceffcb23b76c01584309a96fb6e976dd6aa974e27772112dde9d`  
		Last Modified: Tue, 13 Jan 2026 02:27:51 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c70143cbc33471a2d273161de97a0e5ce788172c6f8b44262cfb154b91547`  
		Last Modified: Tue, 13 Jan 2026 10:34:50 GMT  
		Size: 113.7 MB (113686705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:dea25b3a982b7474158dfe3ae8278bb987bf074e6db6b9c5f20c7c0ac4f5d678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10305816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91c26477fd08846992db26a04f02c1b4cc5f3661c2e2041a622d26398495b97`

```dockerfile
```

-	Layers:
	-	`sha256:dba2eda3687c44598cb2a42f9d2da8a020028d197aa4ea4453de756d4c1fd6da`  
		Last Modified: Tue, 13 Jan 2026 09:44:51 GMT  
		Size: 10.3 MB (10294814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef959e21a2d3d01e2a605e0a2f463587b3c2a983b51971f0e8a122ab514f510`  
		Last Modified: Tue, 13 Jan 2026 09:44:40 GMT  
		Size: 11.0 KB (11002 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7d2eeaf6eae957e80e281db027921cb528c0a508d550cc9a01a644939f5b9d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647906249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12282df21256323007b4623b516ac4113f97dc91d029232ed96e2d1014cc0c9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:41:52 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:52 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:52 GMT
USER spark
# Fri, 14 Nov 2025 00:41:52 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:02 GMT
USER root
# Fri, 14 Nov 2025 01:37:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:02 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a2d7b006aa25763b9e6edd46f17d2069567773314a5077991ec87d2b170a6`  
		Last Modified: Tue, 13 Jan 2026 11:29:15 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b3dbef2ce366da1ade8376fcad6bff5e0d39d87b4a7d9e6e635bbfeb30a173`  
		Last Modified: Tue, 13 Jan 2026 11:29:35 GMT  
		Size: 21.5 MB (21537971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035bcc6536920fedae222ca7c8add833bd67dc5739c25cdd7caaadd09249a18`  
		Last Modified: Tue, 13 Jan 2026 11:30:08 GMT  
		Size: 324.9 MB (324927659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134b18b042cae2e6c65253efcb1add53663a5cc729b915923070f36487e141b2`  
		Last Modified: Tue, 13 Jan 2026 11:29:16 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f210fb2984de57ceb6b469a3dec2876da4300d19fe07f76ca013ca7637e661`  
		Last Modified: Tue, 13 Jan 2026 14:45:03 GMT  
		Size: 108.3 MB (108276513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:60445b1fee7882c31f552cce280beb025af5bc3758a715a66d6e18d1ff72b7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10300356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910d492fe9de2da09de3a6d0fa881d5f8739b295ee3e1e4bbdf6b11dc4617d42`

```dockerfile
```

-	Layers:
	-	`sha256:d586568f1813d1f8d5f52ad544a4dc15ccd1578faba729ddb1a546d2e47d2eed`  
		Last Modified: Fri, 14 Nov 2025 01:37:30 GMT  
		Size: 10.3 MB (10289262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f5a3acd0e7bc34e04e814f1f889c20aa45f10cdd173c444b1b39899dcdf270`  
		Last Modified: Fri, 14 Nov 2025 01:37:29 GMT  
		Size: 11.1 KB (11094 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:ac9ae5af06250e70d3bb8f2ad15d16704aed47d2a0c8f09d764ea0dea52cd198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:5be26a067968db84328419943a1b89764682b40980b53ce6d0004d1514f2de6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.0 MB (861020614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f243213f525acff42b9182c21d4a70d889e3bc4ce3e65c5bbf328fb614b875`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:54 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:40:03 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:03 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:03 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:03 GMT
USER spark
# Fri, 14 Nov 2025 00:40:03 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:21:34 GMT
USER root
# Fri, 14 Nov 2025 01:21:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:21:34 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:21:34 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ddc142dbd294d1861ba917801969cddd78edae3050e0abe0153b39ea3722e0`  
		Last Modified: Tue, 13 Jan 2026 02:27:44 GMT  
		Size: 21.9 MB (21850558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6f43adf3d8d5ac8048ad3d28d3140461ab08ff548611f3e549653bcf0f86e`  
		Last Modified: Tue, 13 Jan 2026 03:41:33 GMT  
		Size: 324.9 MB (324927670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21d6393c00ceffcb23b76c01584309a96fb6e976dd6aa974e27772112dde9d`  
		Last Modified: Tue, 13 Jan 2026 02:27:51 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b44b3a53a6157dd4f6f5cec0315fd41402e0756bfdcd9826537e873174f5702`  
		Last Modified: Fri, 14 Nov 2025 01:22:31 GMT  
		Size: 319.1 MB (319147189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:3bb23fa662fbbd29ec0b490d5621f5bc6bf7ab1f68b2ae3bcc7d9ce0f31ac595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18493769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c61df2ae57c77c34f331c43cef8489ae82dd9b850b4aa4a12a669cc3e72f67`

```dockerfile
```

-	Layers:
	-	`sha256:5c813313a5dc936472fbb2e5eceef2466df4ab720a54d856b5b8793c77b4b570`  
		Last Modified: Fri, 14 Nov 2025 01:22:25 GMT  
		Size: 18.5 MB (18483085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e02c8abe2bb91a2148190d700e9437489c9dcebd50b37db2db253196f7f8ce`  
		Last Modified: Fri, 14 Nov 2025 01:22:24 GMT  
		Size: 10.7 KB (10684 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:68f800e24abfc9710ed538d3c0c6a719208bca6932a742909be9bb32670b842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.0 MB (842007725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fcc0b353a058ffb31b2d06e15ee66080e2b41b044c7590ad4d0f27c14f57d1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 14 Nov 2025 00:41:52 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:52 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:52 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:52 GMT
USER spark
# Fri, 14 Nov 2025 00:41:52 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:59 GMT
USER root
# Fri, 14 Nov 2025 01:37:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:59 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:37:59 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a2d7b006aa25763b9e6edd46f17d2069567773314a5077991ec87d2b170a6`  
		Last Modified: Tue, 13 Jan 2026 11:29:15 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b3dbef2ce366da1ade8376fcad6bff5e0d39d87b4a7d9e6e635bbfeb30a173`  
		Last Modified: Tue, 13 Jan 2026 11:29:35 GMT  
		Size: 21.5 MB (21537971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035bcc6536920fedae222ca7c8add833bd67dc5739c25cdd7caaadd09249a18`  
		Last Modified: Tue, 13 Jan 2026 11:30:08 GMT  
		Size: 324.9 MB (324927659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134b18b042cae2e6c65253efcb1add53663a5cc729b915923070f36487e141b2`  
		Last Modified: Tue, 13 Jan 2026 11:29:16 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1807a6df26343c6fbd03b2cbc60d970d29aca3529ebe4a7d9a4be6eddbf3bc`  
		Last Modified: Fri, 14 Nov 2025 01:39:12 GMT  
		Size: 302.4 MB (302377989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2d20252b04eedd3bdfda10fff2954915e3e16f02f338ada54cc0e4a4462a28fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18458402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c51bfabb6f43ca700974558bcdd4fb6652ebd2173a0a41cd943a0f33c4d2f56`

```dockerfile
```

-	Layers:
	-	`sha256:b0f27d88476698da3b19025f43545ccb349c8e0eac7ef869e4fbf345789bdc99`  
		Last Modified: Fri, 14 Nov 2025 01:38:53 GMT  
		Size: 18.4 MB (18447638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dced6e36914f837a9c0168edd79aa52e651fc11e246fe1a89cfd1321ad14885e`  
		Last Modified: Fri, 14 Nov 2025 01:38:52 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.7-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:a98f634ebbfbc563a05eb915db55bb760cfb9a8670afa1ce4ecd2fbcf67ae1c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.7-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:0687f5aea29cd047c36649cdc979e27bc05a6b21efebce90ab8578a187fbba3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541860517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ab6f56713d867309191b865acf7d468e2c6c0ca812f5a0af94913e71824e9f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:52 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:09:19 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:09:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:09:30 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:09:30 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:09:53 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:09:53 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:09:53 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:09:53 GMT
USER spark
# Fri, 16 Jan 2026 01:09:53 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ede50ffae3ced1f5ffed35549b8bac68387426b88ec95cdbcc82baf2fd33f`  
		Last Modified: Thu, 15 Jan 2026 22:20:18 GMT  
		Size: 20.7 MB (20688694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227b76b41c25c5c0ce948a17f2d8308398b5dc827c545c7142ca20f30b1cb256`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 144.9 MB (144850896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589743ef81c842f54b86e7e96cf9a3ce388b1e8e676068f5d16a511dd91fccfb`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70ee470d498578f3f261d731c31f16ca9c9f5f583ac83347ec39bc91ed183dc`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4366d7e804bd53e52548a58e956a5efcb2cd46a2e4c55fd5f4c0ed1b53503f4`  
		Last Modified: Fri, 16 Jan 2026 01:10:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82576562d168916fca66911ab14611c93a942588e4826774dfd3b3f96ef40432`  
		Last Modified: Fri, 16 Jan 2026 01:10:29 GMT  
		Size: 21.9 MB (21850522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b9c14222bf58edb5bb5cfd6d119d581ed29ba6fc921384433f7425efb37d2a`  
		Last Modified: Fri, 16 Jan 2026 01:13:00 GMT  
		Size: 324.9 MB (324927712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bddc1e58d0f4cf586898891621c317f4d4d6eb0d1aa7003d559030c715da1e`  
		Last Modified: Fri, 16 Jan 2026 01:26:34 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:addf68a9151384e7913fc568cdee26c296a52a143e4c13b42b2e4094458c2c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4858150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b01cd2d7ce9ddf52dfc677deab096d47a42d7db1f88316562a0647c97a97d7`

```dockerfile
```

-	Layers:
	-	`sha256:ae3f545ac1f8d273de7577493ea71e9561eeba6360f4617aa1233569f9cdd317`  
		Last Modified: Fri, 16 Jan 2026 03:12:34 GMT  
		Size: 4.8 MB (4835184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79dcd826100976968c375f221ac5d20538176b24205b841aff2d1d4ab381781`  
		Last Modified: Fri, 16 Jan 2026 03:12:35 GMT  
		Size: 23.0 KB (22966 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.7-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:78ba004d6bde8ad5a03fb76b7d1abcf5bbe8f56d84c6fc4bc883342fa23c596b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539643827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be73312d8fb0e9f932d7bcd15b6ce8c0bc4ea7cb2c85d66c853a0dfeafab779c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:18 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:13:34 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:13:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:13:42 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:13:42 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz.asc?action=download GPG_KEY=564CA14951C29266889F9C5B90E2BA86F7A9B307
# Fri, 16 Jan 2026 01:13:51 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:13:51 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:13:51 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:13:51 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:13:51 GMT
USER spark
# Fri, 16 Jan 2026 01:13:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f84e430918f56b2a3b21400c38155cc3747e29ae43bf89ec7bd1a2d206b818`  
		Last Modified: Thu, 15 Jan 2026 22:19:47 GMT  
		Size: 22.1 MB (22107474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adfc04002164e831afd68d878fa3bbe3cc04f413d131d3222fbedebb7dda33`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 143.7 MB (143681283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b23fdceb460806f1b4d37e8e1d0a03126441b8a0d1efe1ad54d2d05fce4d1`  
		Last Modified: Thu, 15 Jan 2026 22:19:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7feaec1b5ae6c7e6e38638d964d4991ce35f3a13191880a163bdef3d12c7312`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6798439e682e845c9714243eb0cb4fca1a0ece43f8e3f3f27af8a0c870074a`  
		Last Modified: Fri, 16 Jan 2026 01:14:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dbbccc0cdb73db88c9d082dd42755d1d35fc974a0e17fc9e87479a416aa0b4`  
		Last Modified: Fri, 16 Jan 2026 01:14:32 GMT  
		Size: 21.5 MB (21537886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49017c17b48ad3771d968afcb5848cc73c1d3451839294635fe71c6bb10f0e13`  
		Last Modified: Fri, 16 Jan 2026 01:14:38 GMT  
		Size: 324.9 MB (324927655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232ccd192c997a9d999d7bebad3523792f2f7faf2bb7ed5185279ca4a8250d28`  
		Last Modified: Fri, 16 Jan 2026 01:14:28 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.7-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:20eb85aca3ae6886c8a8ddc4d35d1a0d2cec8c54073928ac1a800e69af5d8e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71e513f81ef9c6a3d7255347af1de780f4f78c9a345e31bbd04e7149f9c747`

```dockerfile
```

-	Layers:
	-	`sha256:8875f74694af27a94dacff08815f4c3a7fe8629cc45e30b668ea437890ebd3bf`  
		Last Modified: Fri, 16 Jan 2026 03:12:40 GMT  
		Size: 4.9 MB (4930687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8985a775bbdfa7a4004fa4b15b6b0d8fe3482af227e23db7184de17b0388b0c`  
		Last Modified: Fri, 16 Jan 2026 03:12:41 GMT  
		Size: 23.1 KB (23076 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1`

```console
$ docker pull spark@sha256:10d82ec4a2ddb2ab04e895b183ef3d8bfa81c1e15966afd70a02a47a653e18b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1` - linux; amd64

```console
$ docker pull spark@sha256:54c0faa057db288676532e00395f4994953e183eecfe6249800ea91f8b4023d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 MB (772276685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c440479d95c1f8bfe55c6bbc4fff92a0f1664b2c25693f96be7903b4221bcb5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:53 GMT
USER root
# Fri, 14 Nov 2025 01:19:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:53 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6c0b15beb1f7c2add40ff91df8173eb94b17d3b34dc560d9d82c266195f3d4`  
		Last Modified: Tue, 13 Jan 2026 03:14:31 GMT  
		Size: 113.7 MB (113686819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1` - unknown; unknown

```console
$ docker pull spark@sha256:7ec8febb51c60fa5983b45933aa939c481d56c81106d505a0d419b4385f6377b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dc4d76299acff30771c8f7565266ff42857b90c756bd62c30439e328ee44a3`

```dockerfile
```

-	Layers:
	-	`sha256:f4a5066b60365e0f34aaa959ac9b90ed7ad3aa3daa2a6f940ddaf5b7db296be4`  
		Last Modified: Tue, 13 Jan 2026 12:04:52 GMT  
		Size: 10.4 MB (10420637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de90fa4611af7c0ed1c1c9bd5a92b18dcdf42b58fc500855dcbbaac244d68459`  
		Last Modified: Tue, 13 Jan 2026 12:04:51 GMT  
		Size: 11.3 KB (11286 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4c7b62625fabdf7510fd9289d7287970adca7ef32cf4d73b26881e96531f858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.6 MB (764622390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff32243530b87b56022f2a2eb11b0ff1af7e53eb72432325a239c174a055c483`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:36:20 GMT
USER root
# Fri, 14 Nov 2025 01:36:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:36:20 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581918ddba692095c8771fa5610fa309618e3b6d07b379998cf2509c39c723ff`  
		Last Modified: Tue, 13 Jan 2026 10:11:40 GMT  
		Size: 108.3 MB (108276240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1` - unknown; unknown

```console
$ docker pull spark@sha256:c10f200c9b24e06e9de5327434ff9eff6b91f5552256f103c853ea07fecd68e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10426487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ac90a0d41df63778af9e4adeb3fba6ccc54738c357fd0e83c7239a60aff49`

```dockerfile
```

-	Layers:
	-	`sha256:2decabcd1a004a7777ce414910e1a222e5935ab648ab17346f8817f24dbf814c`  
		Last Modified: Tue, 13 Jan 2026 10:40:27 GMT  
		Size: 10.4 MB (10415097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35dd24331d7eb13ea99c56d120693a8db251a5df7be18783b5e48873e8058db`  
		Last Modified: Tue, 13 Jan 2026 10:40:26 GMT  
		Size: 11.4 KB (11390 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-java21`

```console
$ docker pull spark@sha256:84738ac8824a2da1d74c225f4371b4e6109295d39ed75eee085d07286505bd55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-java21` - linux; amd64

```console
$ docker pull spark@sha256:63e31a664dc310489593bbc8fa6940a1f6eb829d92995b8ed7a2c8ac17c5e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.3 MB (785264481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03086b8c65cc1e8b1c5c262c2e5fcca8c404962cf7c9fae6ec457aedfe50b957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:40 GMT
USER root
# Fri, 14 Nov 2025 01:19:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:40 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5744c2ff3ef2818580ff98e4c72b03431d4c10df688217345bf3235e344e4286`  
		Last Modified: Tue, 13 Jan 2026 03:00:57 GMT  
		Size: 113.7 MB (113686928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21` - unknown; unknown

```console
$ docker pull spark@sha256:59d70ef9a16a686e072ffb595f562a57bbc8668ce3509c3a6cff802dc0323927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10435643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaacaae6dfb6e269e647874f8338b045b7955a71010163e311107de8021e777`

```dockerfile
```

-	Layers:
	-	`sha256:765a7110bc892c472020b7f249e2508de146b3883a0afa8f988c140dec94d591`  
		Last Modified: Tue, 13 Jan 2026 07:03:47 GMT  
		Size: 10.4 MB (10424049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79c2976685765bc2ef92e52525d62d2c11c5b7d3420fd95d49ee07217d83cf6`  
		Last Modified: Tue, 13 Jan 2026 07:03:34 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-java21` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:68e13bc08f99764294fb2d0726db670b5518e2f3284c9689342a0ef1f62213ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 MB (777048485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691bbd4469ce1c3743f6d39d60793d3d28f2008fc8c85dc106b32b11e592a40d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:35:42 GMT
USER root
# Fri, 14 Nov 2025 01:35:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:42 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c5ece496843e6c9d1a0923897c89e59dd6742a3f4c4335a80f19f88e1b3975`  
		Last Modified: Tue, 13 Jan 2026 04:24:36 GMT  
		Size: 108.3 MB (108276034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21` - unknown; unknown

```console
$ docker pull spark@sha256:b89fc3febef2aa00f549de48d87b0eb2a7ada85e32facb83a24671e3c53e9ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10430232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cddf1b42888a9bbf6c140b7d480fa1f3bd9a834a39739fb7d132dbce2c7d847`

```dockerfile
```

-	Layers:
	-	`sha256:862e22b3e353edb9457e481b012eb3a1f50b2b9c28f7563913c26ff63cbc899d`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 10.4 MB (10418521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b54bca6722798708e9a3b41d59ceed81d33eaa423852b4eb21e7cfab25ecfe0`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-java21-python3`

```console
$ docker pull spark@sha256:84738ac8824a2da1d74c225f4371b4e6109295d39ed75eee085d07286505bd55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-java21-python3` - linux; amd64

```console
$ docker pull spark@sha256:63e31a664dc310489593bbc8fa6940a1f6eb829d92995b8ed7a2c8ac17c5e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.3 MB (785264481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03086b8c65cc1e8b1c5c262c2e5fcca8c404962cf7c9fae6ec457aedfe50b957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:40 GMT
USER root
# Fri, 14 Nov 2025 01:19:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:40 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5744c2ff3ef2818580ff98e4c72b03431d4c10df688217345bf3235e344e4286`  
		Last Modified: Tue, 13 Jan 2026 03:00:57 GMT  
		Size: 113.7 MB (113686928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:59d70ef9a16a686e072ffb595f562a57bbc8668ce3509c3a6cff802dc0323927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10435643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaacaae6dfb6e269e647874f8338b045b7955a71010163e311107de8021e777`

```dockerfile
```

-	Layers:
	-	`sha256:765a7110bc892c472020b7f249e2508de146b3883a0afa8f988c140dec94d591`  
		Last Modified: Tue, 13 Jan 2026 07:03:47 GMT  
		Size: 10.4 MB (10424049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79c2976685765bc2ef92e52525d62d2c11c5b7d3420fd95d49ee07217d83cf6`  
		Last Modified: Tue, 13 Jan 2026 07:03:34 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-java21-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:68e13bc08f99764294fb2d0726db670b5518e2f3284c9689342a0ef1f62213ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 MB (777048485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691bbd4469ce1c3743f6d39d60793d3d28f2008fc8c85dc106b32b11e592a40d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:35:42 GMT
USER root
# Fri, 14 Nov 2025 01:35:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:42 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c5ece496843e6c9d1a0923897c89e59dd6742a3f4c4335a80f19f88e1b3975`  
		Last Modified: Tue, 13 Jan 2026 04:24:36 GMT  
		Size: 108.3 MB (108276034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:b89fc3febef2aa00f549de48d87b0eb2a7ada85e32facb83a24671e3c53e9ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10430232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cddf1b42888a9bbf6c140b7d480fa1f3bd9a834a39739fb7d132dbce2c7d847`

```dockerfile
```

-	Layers:
	-	`sha256:862e22b3e353edb9457e481b012eb3a1f50b2b9c28f7563913c26ff63cbc899d`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 10.4 MB (10418521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b54bca6722798708e9a3b41d59ceed81d33eaa423852b4eb21e7cfab25ecfe0`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-java21-r`

```console
$ docker pull spark@sha256:716248beabd6db7560907828990a144f095c82e4f35f92cb382add8e15a8a192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-java21-r` - linux; amd64

```console
$ docker pull spark@sha256:0939b0bfa5fc378eeaca4ea17b53bcaba32327dd2d5294237a137e66a4a88b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.7 MB (990725127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f51f848d49589f824366a4a95076207e98d7b665dde7b91568fb675564392f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:29 GMT
USER root
# Fri, 14 Nov 2025 01:20:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:29 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:20:29 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28711b4abc2d93f458fd32c1d435808c53d64ee93073b47dd680ff39ea37aa72`  
		Last Modified: Fri, 14 Nov 2025 01:21:28 GMT  
		Size: 319.1 MB (319147574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:0590b982726e6611191b30d2cea907287b213b0c8dcded8d657f246bedaafa92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18622409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad05ba9bed4965f1921795b38d91df0629ac3188b01b6d7778052e973d326047`

```dockerfile
```

-	Layers:
	-	`sha256:fbac804417f3b00d1e7561c0821c957f9c0be4102cecb9ab79270e1741543bc6`  
		Last Modified: Fri, 14 Nov 2025 01:21:22 GMT  
		Size: 18.6 MB (18611726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c229a00a8f026bdfda197a7a2d7e0a49f4aeb2ce94b3e864cae0b7cbd238836a`  
		Last Modified: Fri, 14 Nov 2025 01:21:22 GMT  
		Size: 10.7 KB (10683 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-java21-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a1cc66648ce44a0e2e13ff18e0efa4d52b9840d5df3c760464a185d400bcd5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **971.2 MB (971150563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a00a5b185ed700bdcd1586dd792f258b850bf46a95b2461d66e587951410f3`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:00 GMT
USER root
# Fri, 14 Nov 2025 01:37:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:00 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:37:00 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f194f3b13852d6fd4535500dc0e647429bc42567ec113cae80277080b576741`  
		Last Modified: Fri, 14 Nov 2025 01:38:01 GMT  
		Size: 302.4 MB (302378112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:c4429ecb1ab853f074ea29ca983454da63fbe0ae8508b2f2279be8dd0d15c536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18587042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427d7302ef3bcba2582701a4f85e1b2aaff5aa646ab33c4b50269616ec061a3d`

```dockerfile
```

-	Layers:
	-	`sha256:c672e1995ca6d367e9ed7965c5551e9306d87a3c73ffa97be9357218dba3b4c5`  
		Last Modified: Fri, 14 Nov 2025 01:37:55 GMT  
		Size: 18.6 MB (18576279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e1e141a638c5ebad4fdd4507023f76998147c02c04e65bb27b4a64dbf57ee6`  
		Last Modified: Fri, 14 Nov 2025 01:37:54 GMT  
		Size: 10.8 KB (10763 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-java21-scala`

```console
$ docker pull spark@sha256:ba1366f3a75ddcc1a2f9fea6f03eaad3204c9431d48fb38363f0e73af02cf3f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-java21-scala` - linux; amd64

```console
$ docker pull spark@sha256:1a2635d7e998a96a507af3da90e74bb84de78e00980f3191ce597e1911ac0e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 MB (671565059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537861e32726c493f1c22b0839e0e6358fabb1a3a3fc228cfbfc976120388272`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:05 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:13 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:08:28 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:08:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:08:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:08:39 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:08:51 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:08:51 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:08:51 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:08:51 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:08:51 GMT
USER spark
# Fri, 16 Jan 2026 01:08:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77e7736fdec006b65bbe1bb0abdb2bf076a4fb1b67089cb602e6a1431964ed`  
		Last Modified: Thu, 15 Jan 2026 22:20:41 GMT  
		Size: 20.7 MB (20688486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab53b7b2400ba6f98bb37e2d40662fa86f1584df7e665bc9488dd47b2d37e9f`  
		Last Modified: Thu, 15 Jan 2026 22:20:54 GMT  
		Size: 157.8 MB (157839010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dfb2663e897777f9a9bf3970e6e2f996b97af462e87e478fb62536aebfd75f`  
		Last Modified: Thu, 15 Jan 2026 22:20:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b156b5a347025523a628f6f438e139290c2bac2a1cb5c0d113e5004a068d8e`  
		Last Modified: Thu, 15 Jan 2026 22:20:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d4e9c15cf9995dfd044a3334a4c1d83bb530051cb2bc5a3204260a080cce5d`  
		Last Modified: Fri, 16 Jan 2026 01:09:36 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bad664bdd84ce2afb55f393473dd9cc1641495c4624173702a3dfe81da06b51`  
		Last Modified: Fri, 16 Jan 2026 01:09:43 GMT  
		Size: 21.9 MB (21850694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e8f7bfcc142ed83d1a5061afcf5041c76bf9a0b321d391c5a06cc43c78b919`  
		Last Modified: Fri, 16 Jan 2026 01:11:22 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fdffd9a41182ab92c7e0a4a40969d8ce95faca43da58907bd2d8c36e0bc5b9`  
		Last Modified: Fri, 16 Jan 2026 01:09:36 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:b3174c914ce43a8d49728c055fdf4e191ea11074404a3ca3eafe575cb7cad6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b958a172b4bfb4b664822dda554f5d6400bb64224f7245e2cd3e068de773fe`

```dockerfile
```

-	Layers:
	-	`sha256:f63d70a920bf33cb4b34fd6b841706e9f26fceff78e3ee69a54d9ca47f7dd4ca`  
		Last Modified: Fri, 16 Jan 2026 03:13:14 GMT  
		Size: 5.0 MB (4963825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806743b9a7015dec75b602a0c71b40860ab8a131ff97778b879a12a5d0528d04`  
		Last Modified: Fri, 16 Jan 2026 03:13:15 GMT  
		Size: 23.0 KB (22963 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-java21-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9106c69c7364b1bf597fce9c14378da8a0cbfd90ae51d40f4d2b53c84142a08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.8 MB (668786582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9961edf7d8fbfa7b825ecb732de1b2e0ee3f85b1aaa6787d908d7fd0ce16ea`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:23 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:32 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:11:06 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:11:06 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:11:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:11:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:11:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:11:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:11:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:11:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:11:28 GMT
USER spark
# Fri, 16 Jan 2026 01:11:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493c2f62b1fb2eeb7f16caf75211c2742191586cc868924f24652124cf64a330`  
		Last Modified: Thu, 15 Jan 2026 22:21:03 GMT  
		Size: 22.1 MB (22107475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd81e4068932ff2943205b5e34a7c3ce496d549f89a22362e6255791b8bd9db7`  
		Last Modified: Thu, 15 Jan 2026 23:54:39 GMT  
		Size: 156.1 MB (156107615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0ca63e8dda6e564c2bec761ae086ce8bc75214a4ae61b90de83c0abae8c6a`  
		Last Modified: Thu, 15 Jan 2026 22:21:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ee81093faa209f1b1d40e0fdf45471a90f0497e7932ac88bc3b4b1d403118`  
		Last Modified: Thu, 15 Jan 2026 22:20:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfc82ff8d0cf716bf220922e4e5f841fc7d50afcce2e53079e1212285ab4af`  
		Last Modified: Fri, 16 Jan 2026 01:13:47 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9c6ebb16fc15249fd16f5340c8098a686c6415aaf8be4c66569f5c632eee`  
		Last Modified: Fri, 16 Jan 2026 01:13:49 GMT  
		Size: 21.5 MB (21537861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01ef94eec84118210899406c1c704889c87268544a1327aa52fbe14fab312f1`  
		Last Modified: Fri, 16 Jan 2026 01:16:44 GMT  
		Size: 441.6 MB (441644106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23edfb5ce0735bc5ab82168aaed5ab60ff3d4a014624e806083423e1c358ad4d`  
		Last Modified: Fri, 16 Jan 2026 01:13:47 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:412f2266e1dd38a384fdfafe3bc79762e3d891babdfc0ae9a0d6ddb38558bb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510fd02777069044bf62550e8942597e19e40b8608ec3db1ef443c91b2466163`

```dockerfile
```

-	Layers:
	-	`sha256:f9c2e45ec7059ef9a372619fe53ad2cdf7421d054b2c4fd86f698501d97265d9`  
		Last Modified: Fri, 16 Jan 2026 03:13:20 GMT  
		Size: 5.1 MB (5059328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60c41703358f1a83dd8c9eb85b6bfe75a262d8958d8ccf76f362eae8d31ceffb`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 23.1 KB (23072 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-python3`

```console
$ docker pull spark@sha256:10d82ec4a2ddb2ab04e895b183ef3d8bfa81c1e15966afd70a02a47a653e18b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-python3` - linux; amd64

```console
$ docker pull spark@sha256:54c0faa057db288676532e00395f4994953e183eecfe6249800ea91f8b4023d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 MB (772276685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c440479d95c1f8bfe55c6bbc4fff92a0f1664b2c25693f96be7903b4221bcb5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:53 GMT
USER root
# Fri, 14 Nov 2025 01:19:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:53 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6c0b15beb1f7c2add40ff91df8173eb94b17d3b34dc560d9d82c266195f3d4`  
		Last Modified: Tue, 13 Jan 2026 03:14:31 GMT  
		Size: 113.7 MB (113686819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:7ec8febb51c60fa5983b45933aa939c481d56c81106d505a0d419b4385f6377b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dc4d76299acff30771c8f7565266ff42857b90c756bd62c30439e328ee44a3`

```dockerfile
```

-	Layers:
	-	`sha256:f4a5066b60365e0f34aaa959ac9b90ed7ad3aa3daa2a6f940ddaf5b7db296be4`  
		Last Modified: Tue, 13 Jan 2026 12:04:52 GMT  
		Size: 10.4 MB (10420637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de90fa4611af7c0ed1c1c9bd5a92b18dcdf42b58fc500855dcbbaac244d68459`  
		Last Modified: Tue, 13 Jan 2026 12:04:51 GMT  
		Size: 11.3 KB (11286 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4c7b62625fabdf7510fd9289d7287970adca7ef32cf4d73b26881e96531f858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.6 MB (764622390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff32243530b87b56022f2a2eb11b0ff1af7e53eb72432325a239c174a055c483`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:36:20 GMT
USER root
# Fri, 14 Nov 2025 01:36:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:36:20 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581918ddba692095c8771fa5610fa309618e3b6d07b379998cf2509c39c723ff`  
		Last Modified: Tue, 13 Jan 2026 10:11:40 GMT  
		Size: 108.3 MB (108276240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:c10f200c9b24e06e9de5327434ff9eff6b91f5552256f103c853ea07fecd68e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10426487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ac90a0d41df63778af9e4adeb3fba6ccc54738c357fd0e83c7239a60aff49`

```dockerfile
```

-	Layers:
	-	`sha256:2decabcd1a004a7777ce414910e1a222e5935ab648ab17346f8817f24dbf814c`  
		Last Modified: Tue, 13 Jan 2026 10:40:27 GMT  
		Size: 10.4 MB (10415097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35dd24331d7eb13ea99c56d120693a8db251a5df7be18783b5e48873e8058db`  
		Last Modified: Tue, 13 Jan 2026 10:40:26 GMT  
		Size: 11.4 KB (11390 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-r`

```console
$ docker pull spark@sha256:11a21d0df03fe4e8e625ff25a781961f8e1ef0f98f41dc7844ef9f2d255fd8c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-r` - linux; amd64

```console
$ docker pull spark@sha256:c0cac1cf2ea853b3ddd96cd31f5af6cd736ee40514be0c78308eb309987e3517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.7 MB (977736656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b59da1863dcfdfdde0b52316727a9b0c733ea0661c2d3645dd190e02690d229`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:42 GMT
USER root
# Fri, 14 Nov 2025 01:20:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:42 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:20:42 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd980dead91451bfbc34750030cc61a1d59c15517362e71a04673af50e5ebccb`  
		Last Modified: Wed, 14 Jan 2026 21:24:54 GMT  
		Size: 319.1 MB (319146790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:11cb3e5896d6f98921ebaae45ba72593e0bfd05beee24934bbf35b369ef744d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18619852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f9ff84084064b0b359035da19233b4fa3dadc0f17dec0c81395b759e78978`

```dockerfile
```

-	Layers:
	-	`sha256:7b6ca02a6a477677b1dcf1f5c26bdcdebe70aef34ae9da060db8262d5c1c1754`  
		Last Modified: Fri, 14 Nov 2025 01:21:35 GMT  
		Size: 18.6 MB (18608896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29bea142bbd31c6363379711341a13bba22d4d06bfd39a9fe04df65ecb321ab2`  
		Last Modified: Fri, 14 Nov 2025 01:21:33 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:3b80e15381cf6b61a836c3f74e2a2630336d95c8a03b38a4c5c9efb7af44be66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.7 MB (958723807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e643c763d9ec411260be6d5b6a946d0243b446d8cc7278e1be3edcd5166aa5d8`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:08 GMT
USER root
# Fri, 14 Nov 2025 01:37:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:08 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:37:08 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdef43c0f11c86fb05c4b2bf024ed807e36ae26d8b4945b257f5e0a4d295ee2f`  
		Last Modified: Fri, 14 Nov 2025 01:38:08 GMT  
		Size: 302.4 MB (302377657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:e3025df6c37c8816746b88105f882e33ff72b90071e8a9a6935006e39a267210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18584509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93cc93127a5b9acb9996d40b2ccb17ddc89b5b4b355109bbd5eb8032be21e34`

```dockerfile
```

-	Layers:
	-	`sha256:40592b19336d8e196854b806088803070cdcf14256fe11c8c7995d1832978c1c`  
		Last Modified: Fri, 14 Nov 2025 01:38:01 GMT  
		Size: 18.6 MB (18573461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3883515069edb7d45d094ae20a8d729d479aa5421ecb679706bc8261bba2c7`  
		Last Modified: Fri, 14 Nov 2025 01:38:00 GMT  
		Size: 11.0 KB (11048 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala`

```console
$ docker pull spark@sha256:978661143403e30c831851a25b2c1e85eb04e5e27fccea9721184b8852159c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala` - linux; amd64

```console
$ docker pull spark@sha256:5479d4469a489290f6f5b73e6369b1e82d7a426da7a7f74a5cdc0503f1ac868c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.6 MB (658577133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7ffcc31b0856ca24a002f760e385d42d33d1165d43f4cb1f584b8e2d018194`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:52 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:09:21 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:09:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:09:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:09:32 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:09:44 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:09:44 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:09:44 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:09:44 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:09:44 GMT
USER spark
# Fri, 16 Jan 2026 01:09:44 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ede50ffae3ced1f5ffed35549b8bac68387426b88ec95cdbcc82baf2fd33f`  
		Last Modified: Thu, 15 Jan 2026 22:20:18 GMT  
		Size: 20.7 MB (20688694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227b76b41c25c5c0ce948a17f2d8308398b5dc827c545c7142ca20f30b1cb256`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 144.9 MB (144850896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589743ef81c842f54b86e7e96cf9a3ce388b1e8e676068f5d16a511dd91fccfb`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70ee470d498578f3f261d731c31f16ca9c9f5f583ac83347ec39bc91ed183dc`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac811d8620bc57d872722ac4910288a89e8581d9ed0551a130ad9c64767e04`  
		Last Modified: Fri, 16 Jan 2026 01:10:28 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aa7237a5f72f89ff3782080245fd12a0be926874d28bc85603eb7d31ee6d07`  
		Last Modified: Fri, 16 Jan 2026 01:10:30 GMT  
		Size: 21.9 MB (21850674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3636baf6ed3807b0750514e6bd544c1ea1c5aa2081d9429e02c771406ff019f3`  
		Last Modified: Fri, 16 Jan 2026 01:12:40 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a3a74c95017f38125de35d632f73dad1649f9d50c2e3c0cf9860c49c549d0f`  
		Last Modified: Fri, 16 Jan 2026 01:10:28 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:a1be5df6e184c99f740f40fa0319981a4440bbcce2d28c5037026434f79b3b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20843b82234c150e2905a4997342962a2aab1e2c79db62812f7377dc54afd91`

```dockerfile
```

-	Layers:
	-	`sha256:d3fa23949a3c498feed638209111733c3ddfb12f47164d4a8acacf131e7b93f3`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 5.0 MB (4961003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c325fb71069d0fd1fee1c7ef1b3fdcbe4aae4da48991a95a3dc6c9ae1dd096`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 23.2 KB (23246 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:486dab03bc3059acf0617ab83ca06f992411bdd964ec0089c3e9ed6b51e475bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.4 MB (656360295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756e7ab3e7f9bf11227501cd89b02b2b3bddde0d594bfc198499b588236faf64`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:18 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:12:17 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:12:17 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:12:25 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:12:25 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:12:37 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:12:37 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:12:37 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:12:37 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:12:37 GMT
USER spark
# Fri, 16 Jan 2026 01:12:37 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f84e430918f56b2a3b21400c38155cc3747e29ae43bf89ec7bd1a2d206b818`  
		Last Modified: Thu, 15 Jan 2026 22:19:47 GMT  
		Size: 22.1 MB (22107474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adfc04002164e831afd68d878fa3bbe3cc04f413d131d3222fbedebb7dda33`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 143.7 MB (143681283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b23fdceb460806f1b4d37e8e1d0a03126441b8a0d1efe1ad54d2d05fce4d1`  
		Last Modified: Thu, 15 Jan 2026 22:19:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7feaec1b5ae6c7e6e38638d964d4991ce35f3a13191880a163bdef3d12c7312`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d93a4122d19034a36085227ce22f88e160cba24899cefba8a716ee8cb6c532`  
		Last Modified: Fri, 16 Jan 2026 01:13:20 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9c4b7a4c814851146b036c758c57eaf037ccd0379f814dd4f532033a325099`  
		Last Modified: Fri, 16 Jan 2026 01:13:22 GMT  
		Size: 21.5 MB (21537840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1f217834cbb15d4dcddf79d4bfd1f94e6db6d4066803685d051b15938795fe`  
		Last Modified: Fri, 16 Jan 2026 01:13:47 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafd9920332da7a567896960fe8d43ca03d5d622e21a92a39709b70f48cd8ac9`  
		Last Modified: Fri, 16 Jan 2026 01:13:20 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:4c8ed362a6ab8a11795acef324f175480a6529fba08e3090bf0a493e87ac3b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd871afea0d83865878ea5559202edb8a47f708c5ea9ce6ffda8bb35e4576fa`

```dockerfile
```

-	Layers:
	-	`sha256:a8fd8bb7f44216601d1a328cc0a898bcdb07e3431fcf7db336742c426d0d956a`  
		Last Modified: Fri, 16 Jan 2026 03:13:27 GMT  
		Size: 5.1 MB (5056518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075a3508c9e74bbc6ca9c51623c0b485546a97d97184f5d7be3be4c02d590b18`  
		Last Modified: Fri, 16 Jan 2026 03:13:27 GMT  
		Size: 23.4 KB (23368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:a11e1041ede37e47aaa5eae5dc5fecb9c055b78d8ee11aecdb377cec46eb1a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:e6ca75a464e7b730f1b0187611c97d37cafd79ad4c3bf3d8072cd9d77b22f321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 MB (992453452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f61424a1fb3c8cf9211a3938ab420b3c568156bfdf2db502a4fe5b8e7c0586e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:17:56 GMT
USER root
# Fri, 14 Nov 2025 01:17:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:56 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:17:56 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1fc3d0296856f29bbc1063fa77ad1c878ae381a661f60ab2a9c8db44785aa`  
		Last Modified: Tue, 13 Jan 2026 05:02:27 GMT  
		Size: 333.9 MB (333863586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6ac3eef5af136095da45dadb77edffd198cf021f32f20e0de5cd63e1f768eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19665316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220b9db8d5c7c43570e8e018bdbafa85860494496b9ad756d76fecff15a02d8c`

```dockerfile
```

-	Layers:
	-	`sha256:fa6686da1257da99b68722630ae0520e51b81e521930061ba9f04072d8d6ad60`  
		Last Modified: Thu, 15 Jan 2026 18:07:10 GMT  
		Size: 19.7 MB (19654769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:761e8978d49938ff5c2670eb5d496b9accea2e8023c70aaf3f55c1172fd6d552`  
		Last Modified: Thu, 15 Jan 2026 18:07:09 GMT  
		Size: 10.5 KB (10547 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:0153608658d7abffe422d77f23adc2b38d70385932194ba17f577d0d7452f953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.3 MB (973300592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374836f3b4baf689867f7affd0bb6e8edca2b570c9a841260905ba0cbdc4d388`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:34:38 GMT
USER root
# Fri, 14 Nov 2025 01:34:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:38 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:34:38 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc60a1bbec0491ebbb1df1f1dc4dcc6b0dbf30699bb4c540f6451f1a43a42ac`  
		Last Modified: Thu, 15 Jan 2026 03:24:56 GMT  
		Size: 317.0 MB (316954442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6cdfdce75b9633541f4f477a1968bd8671cf6b291f948f83c440a098ca44badf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19629950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb3e25b45182925f1767172cb6d66a823f4b470aa636c5f5f17dff147bd3a75`

```dockerfile
```

-	Layers:
	-	`sha256:569aae89e3770841c0077374de580b6c7e87043ea2de40aba03fb4c63c6b1426`  
		Last Modified: Fri, 14 Nov 2025 01:35:37 GMT  
		Size: 19.6 MB (19619334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:275de82794edad46a47a5460905e1cadf0e032f22858d8917912a58750217e8f`  
		Last Modified: Fri, 14 Nov 2025 01:35:37 GMT  
		Size: 10.6 KB (10616 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:10d82ec4a2ddb2ab04e895b183ef3d8bfa81c1e15966afd70a02a47a653e18b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:54c0faa057db288676532e00395f4994953e183eecfe6249800ea91f8b4023d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 MB (772276685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c440479d95c1f8bfe55c6bbc4fff92a0f1664b2c25693f96be7903b4221bcb5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:53 GMT
USER root
# Fri, 14 Nov 2025 01:19:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:53 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6c0b15beb1f7c2add40ff91df8173eb94b17d3b34dc560d9d82c266195f3d4`  
		Last Modified: Tue, 13 Jan 2026 03:14:31 GMT  
		Size: 113.7 MB (113686819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:7ec8febb51c60fa5983b45933aa939c481d56c81106d505a0d419b4385f6377b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dc4d76299acff30771c8f7565266ff42857b90c756bd62c30439e328ee44a3`

```dockerfile
```

-	Layers:
	-	`sha256:f4a5066b60365e0f34aaa959ac9b90ed7ad3aa3daa2a6f940ddaf5b7db296be4`  
		Last Modified: Tue, 13 Jan 2026 12:04:52 GMT  
		Size: 10.4 MB (10420637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de90fa4611af7c0ed1c1c9bd5a92b18dcdf42b58fc500855dcbbaac244d68459`  
		Last Modified: Tue, 13 Jan 2026 12:04:51 GMT  
		Size: 11.3 KB (11286 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4c7b62625fabdf7510fd9289d7287970adca7ef32cf4d73b26881e96531f858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.6 MB (764622390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff32243530b87b56022f2a2eb11b0ff1af7e53eb72432325a239c174a055c483`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:36:20 GMT
USER root
# Fri, 14 Nov 2025 01:36:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:36:20 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581918ddba692095c8771fa5610fa309618e3b6d07b379998cf2509c39c723ff`  
		Last Modified: Tue, 13 Jan 2026 10:11:40 GMT  
		Size: 108.3 MB (108276240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c10f200c9b24e06e9de5327434ff9eff6b91f5552256f103c853ea07fecd68e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10426487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ac90a0d41df63778af9e4adeb3fba6ccc54738c357fd0e83c7239a60aff49`

```dockerfile
```

-	Layers:
	-	`sha256:2decabcd1a004a7777ce414910e1a222e5935ab648ab17346f8817f24dbf814c`  
		Last Modified: Tue, 13 Jan 2026 10:40:27 GMT  
		Size: 10.4 MB (10415097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35dd24331d7eb13ea99c56d120693a8db251a5df7be18783b5e48873e8058db`  
		Last Modified: Tue, 13 Jan 2026 10:40:26 GMT  
		Size: 11.4 KB (11390 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java17-r-ubuntu`

```console
$ docker pull spark@sha256:11a21d0df03fe4e8e625ff25a781961f8e1ef0f98f41dc7844ef9f2d255fd8c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:c0cac1cf2ea853b3ddd96cd31f5af6cd736ee40514be0c78308eb309987e3517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.7 MB (977736656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b59da1863dcfdfdde0b52316727a9b0c733ea0661c2d3645dd190e02690d229`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:42 GMT
USER root
# Fri, 14 Nov 2025 01:20:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:42 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:20:42 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd980dead91451bfbc34750030cc61a1d59c15517362e71a04673af50e5ebccb`  
		Last Modified: Wed, 14 Jan 2026 21:24:54 GMT  
		Size: 319.1 MB (319146790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:11cb3e5896d6f98921ebaae45ba72593e0bfd05beee24934bbf35b369ef744d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18619852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f9ff84084064b0b359035da19233b4fa3dadc0f17dec0c81395b759e78978`

```dockerfile
```

-	Layers:
	-	`sha256:7b6ca02a6a477677b1dcf1f5c26bdcdebe70aef34ae9da060db8262d5c1c1754`  
		Last Modified: Fri, 14 Nov 2025 01:21:35 GMT  
		Size: 18.6 MB (18608896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29bea142bbd31c6363379711341a13bba22d4d06bfd39a9fe04df65ecb321ab2`  
		Last Modified: Fri, 14 Nov 2025 01:21:33 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:3b80e15381cf6b61a836c3f74e2a2630336d95c8a03b38a4c5c9efb7af44be66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.7 MB (958723807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e643c763d9ec411260be6d5b6a946d0243b446d8cc7278e1be3edcd5166aa5d8`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:08 GMT
USER root
# Fri, 14 Nov 2025 01:37:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:08 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:37:08 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdef43c0f11c86fb05c4b2bf024ed807e36ae26d8b4945b257f5e0a4d295ee2f`  
		Last Modified: Fri, 14 Nov 2025 01:38:08 GMT  
		Size: 302.4 MB (302377657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e3025df6c37c8816746b88105f882e33ff72b90071e8a9a6935006e39a267210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18584509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93cc93127a5b9acb9996d40b2ccb17ddc89b5b4b355109bbd5eb8032be21e34`

```dockerfile
```

-	Layers:
	-	`sha256:40592b19336d8e196854b806088803070cdcf14256fe11c8c7995d1832978c1c`  
		Last Modified: Fri, 14 Nov 2025 01:38:01 GMT  
		Size: 18.6 MB (18573461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3883515069edb7d45d094ae20a8d729d479aa5421ecb679706bc8261bba2c7`  
		Last Modified: Fri, 14 Nov 2025 01:38:00 GMT  
		Size: 11.0 KB (11048 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java17-ubuntu`

```console
$ docker pull spark@sha256:978661143403e30c831851a25b2c1e85eb04e5e27fccea9721184b8852159c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:5479d4469a489290f6f5b73e6369b1e82d7a426da7a7f74a5cdc0503f1ac868c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.6 MB (658577133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7ffcc31b0856ca24a002f760e385d42d33d1165d43f4cb1f584b8e2d018194`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:52 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:09:21 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:09:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:09:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:09:32 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:09:44 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:09:44 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:09:44 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:09:44 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:09:44 GMT
USER spark
# Fri, 16 Jan 2026 01:09:44 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ede50ffae3ced1f5ffed35549b8bac68387426b88ec95cdbcc82baf2fd33f`  
		Last Modified: Thu, 15 Jan 2026 22:20:18 GMT  
		Size: 20.7 MB (20688694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227b76b41c25c5c0ce948a17f2d8308398b5dc827c545c7142ca20f30b1cb256`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 144.9 MB (144850896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589743ef81c842f54b86e7e96cf9a3ce388b1e8e676068f5d16a511dd91fccfb`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70ee470d498578f3f261d731c31f16ca9c9f5f583ac83347ec39bc91ed183dc`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac811d8620bc57d872722ac4910288a89e8581d9ed0551a130ad9c64767e04`  
		Last Modified: Fri, 16 Jan 2026 01:10:28 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aa7237a5f72f89ff3782080245fd12a0be926874d28bc85603eb7d31ee6d07`  
		Last Modified: Fri, 16 Jan 2026 01:10:30 GMT  
		Size: 21.9 MB (21850674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3636baf6ed3807b0750514e6bd544c1ea1c5aa2081d9429e02c771406ff019f3`  
		Last Modified: Fri, 16 Jan 2026 01:12:40 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a3a74c95017f38125de35d632f73dad1649f9d50c2e3c0cf9860c49c549d0f`  
		Last Modified: Fri, 16 Jan 2026 01:10:28 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a1be5df6e184c99f740f40fa0319981a4440bbcce2d28c5037026434f79b3b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20843b82234c150e2905a4997342962a2aab1e2c79db62812f7377dc54afd91`

```dockerfile
```

-	Layers:
	-	`sha256:d3fa23949a3c498feed638209111733c3ddfb12f47164d4a8acacf131e7b93f3`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 5.0 MB (4961003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c325fb71069d0fd1fee1c7ef1b3fdcbe4aae4da48991a95a3dc6c9ae1dd096`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 23.2 KB (23246 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:486dab03bc3059acf0617ab83ca06f992411bdd964ec0089c3e9ed6b51e475bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.4 MB (656360295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756e7ab3e7f9bf11227501cd89b02b2b3bddde0d594bfc198499b588236faf64`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:18 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:12:17 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:12:17 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:12:25 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:12:25 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:12:37 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:12:37 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:12:37 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:12:37 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:12:37 GMT
USER spark
# Fri, 16 Jan 2026 01:12:37 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f84e430918f56b2a3b21400c38155cc3747e29ae43bf89ec7bd1a2d206b818`  
		Last Modified: Thu, 15 Jan 2026 22:19:47 GMT  
		Size: 22.1 MB (22107474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adfc04002164e831afd68d878fa3bbe3cc04f413d131d3222fbedebb7dda33`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 143.7 MB (143681283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b23fdceb460806f1b4d37e8e1d0a03126441b8a0d1efe1ad54d2d05fce4d1`  
		Last Modified: Thu, 15 Jan 2026 22:19:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7feaec1b5ae6c7e6e38638d964d4991ce35f3a13191880a163bdef3d12c7312`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d93a4122d19034a36085227ce22f88e160cba24899cefba8a716ee8cb6c532`  
		Last Modified: Fri, 16 Jan 2026 01:13:20 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9c4b7a4c814851146b036c758c57eaf037ccd0379f814dd4f532033a325099`  
		Last Modified: Fri, 16 Jan 2026 01:13:22 GMT  
		Size: 21.5 MB (21537840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1f217834cbb15d4dcddf79d4bfd1f94e6db6d4066803685d051b15938795fe`  
		Last Modified: Fri, 16 Jan 2026 01:13:47 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafd9920332da7a567896960fe8d43ca03d5d622e21a92a39709b70f48cd8ac9`  
		Last Modified: Fri, 16 Jan 2026 01:13:20 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4c8ed362a6ab8a11795acef324f175480a6529fba08e3090bf0a493e87ac3b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd871afea0d83865878ea5559202edb8a47f708c5ea9ce6ffda8bb35e4576fa`

```dockerfile
```

-	Layers:
	-	`sha256:a8fd8bb7f44216601d1a328cc0a898bcdb07e3431fcf7db336742c426d0d956a`  
		Last Modified: Fri, 16 Jan 2026 03:13:27 GMT  
		Size: 5.1 MB (5056518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075a3508c9e74bbc6ca9c51623c0b485546a97d97184f5d7be3be4c02d590b18`  
		Last Modified: Fri, 16 Jan 2026 03:13:27 GMT  
		Size: 23.4 KB (23368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java21-python3-r-ubuntu`

```console
$ docker pull spark@sha256:2fd82437afe7470abbfbce7cb91c0deefbdff864fa44a4cb01bca2d4505bb648
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java21-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:373fc7202c0601581251561846b634f6f4847b58bef92ce39c670af488a2beb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1005441638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4049de64b1fbe52bed6f02bae688e8fc2ea9c4f30bec76b25b5c9f1824f58bee`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:17:57 GMT
USER root
# Fri, 14 Nov 2025 01:17:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:57 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:17:57 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4673255510291cac0fbd1731aade3ac04b8667d2b408ff0af2eb20af935fde42`  
		Last Modified: Wed, 14 Jan 2026 13:49:58 GMT  
		Size: 333.9 MB (333864085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8233191bcbef0a6272417666afef9df8866bb0c2fddb5efe84184b256872a98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19668418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18e426464d88845ee09894f3224fc659dfee4cf7f67588d4123bc7cbe8ba97c`

```dockerfile
```

-	Layers:
	-	`sha256:1ca36f76143f5ce5b90fdaeb5e38ca1db23c255e1f0366107cbf7c359c0c5a98`  
		Last Modified: Wed, 14 Jan 2026 13:49:37 GMT  
		Size: 19.7 MB (19657871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d9f82e2c8362a7f8df97e3ae9edee76b0023779c847c7bae837016d053a885`  
		Last Modified: Wed, 14 Jan 2026 13:49:35 GMT  
		Size: 10.5 KB (10547 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java21-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d1403e437ca47cafe57d3725561d3cb2733f9fa50479ea7fe8a79a4e24a3e43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.7 MB (985726144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cfbdeaa5b2a2faac9efa08ae3871443dccdb0b1ba6c87b7854c0ec22e6c488`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:34:08 GMT
USER root
# Fri, 14 Nov 2025 01:34:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:08 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:34:08 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f70879517691ad5da4457eeea55e68aaf28045c701b94fdd676213a0019749b`  
		Last Modified: Fri, 14 Nov 2025 01:35:11 GMT  
		Size: 317.0 MB (316953693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4c878b7c8f72a823037fb57412c8c468d5e020ee7d8ea3bdb3190b9e839ef949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19633051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b268d812005b8db34c3c7a0889618b55cac7986d5285daef9408fc796bbd3e3`

```dockerfile
```

-	Layers:
	-	`sha256:72e07f0f7daefba8a8c1fdb369152a7c4cdccc56fcc69bac11d4efa9e4a91c96`  
		Last Modified: Fri, 14 Nov 2025 01:35:06 GMT  
		Size: 19.6 MB (19622436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc594e916cc971d37ba27e7e7484d6a52c87d01013eb786b56064c32c879ee2`  
		Last Modified: Fri, 14 Nov 2025 01:35:05 GMT  
		Size: 10.6 KB (10615 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java21-python3-ubuntu`

```console
$ docker pull spark@sha256:84738ac8824a2da1d74c225f4371b4e6109295d39ed75eee085d07286505bd55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java21-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:63e31a664dc310489593bbc8fa6940a1f6eb829d92995b8ed7a2c8ac17c5e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.3 MB (785264481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03086b8c65cc1e8b1c5c262c2e5fcca8c404962cf7c9fae6ec457aedfe50b957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:40 GMT
USER root
# Fri, 14 Nov 2025 01:19:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:40 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5744c2ff3ef2818580ff98e4c72b03431d4c10df688217345bf3235e344e4286`  
		Last Modified: Tue, 13 Jan 2026 03:00:57 GMT  
		Size: 113.7 MB (113686928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:59d70ef9a16a686e072ffb595f562a57bbc8668ce3509c3a6cff802dc0323927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10435643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaacaae6dfb6e269e647874f8338b045b7955a71010163e311107de8021e777`

```dockerfile
```

-	Layers:
	-	`sha256:765a7110bc892c472020b7f249e2508de146b3883a0afa8f988c140dec94d591`  
		Last Modified: Tue, 13 Jan 2026 07:03:47 GMT  
		Size: 10.4 MB (10424049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79c2976685765bc2ef92e52525d62d2c11c5b7d3420fd95d49ee07217d83cf6`  
		Last Modified: Tue, 13 Jan 2026 07:03:34 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java21-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:68e13bc08f99764294fb2d0726db670b5518e2f3284c9689342a0ef1f62213ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 MB (777048485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691bbd4469ce1c3743f6d39d60793d3d28f2008fc8c85dc106b32b11e592a40d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:35:42 GMT
USER root
# Fri, 14 Nov 2025 01:35:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:42 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c5ece496843e6c9d1a0923897c89e59dd6742a3f4c4335a80f19f88e1b3975`  
		Last Modified: Tue, 13 Jan 2026 04:24:36 GMT  
		Size: 108.3 MB (108276034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b89fc3febef2aa00f549de48d87b0eb2a7ada85e32facb83a24671e3c53e9ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10430232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cddf1b42888a9bbf6c140b7d480fa1f3bd9a834a39739fb7d132dbce2c7d847`

```dockerfile
```

-	Layers:
	-	`sha256:862e22b3e353edb9457e481b012eb3a1f50b2b9c28f7563913c26ff63cbc899d`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 10.4 MB (10418521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b54bca6722798708e9a3b41d59ceed81d33eaa423852b4eb21e7cfab25ecfe0`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java21-r-ubuntu`

```console
$ docker pull spark@sha256:716248beabd6db7560907828990a144f095c82e4f35f92cb382add8e15a8a192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java21-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:0939b0bfa5fc378eeaca4ea17b53bcaba32327dd2d5294237a137e66a4a88b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.7 MB (990725127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f51f848d49589f824366a4a95076207e98d7b665dde7b91568fb675564392f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:29 GMT
USER root
# Fri, 14 Nov 2025 01:20:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:29 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:20:29 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28711b4abc2d93f458fd32c1d435808c53d64ee93073b47dd680ff39ea37aa72`  
		Last Modified: Fri, 14 Nov 2025 01:21:28 GMT  
		Size: 319.1 MB (319147574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0590b982726e6611191b30d2cea907287b213b0c8dcded8d657f246bedaafa92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18622409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad05ba9bed4965f1921795b38d91df0629ac3188b01b6d7778052e973d326047`

```dockerfile
```

-	Layers:
	-	`sha256:fbac804417f3b00d1e7561c0821c957f9c0be4102cecb9ab79270e1741543bc6`  
		Last Modified: Fri, 14 Nov 2025 01:21:22 GMT  
		Size: 18.6 MB (18611726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c229a00a8f026bdfda197a7a2d7e0a49f4aeb2ce94b3e864cae0b7cbd238836a`  
		Last Modified: Fri, 14 Nov 2025 01:21:22 GMT  
		Size: 10.7 KB (10683 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java21-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a1cc66648ce44a0e2e13ff18e0efa4d52b9840d5df3c760464a185d400bcd5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **971.2 MB (971150563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a00a5b185ed700bdcd1586dd792f258b850bf46a95b2461d66e587951410f3`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:00 GMT
USER root
# Fri, 14 Nov 2025 01:37:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:00 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:37:00 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f194f3b13852d6fd4535500dc0e647429bc42567ec113cae80277080b576741`  
		Last Modified: Fri, 14 Nov 2025 01:38:01 GMT  
		Size: 302.4 MB (302378112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c4429ecb1ab853f074ea29ca983454da63fbe0ae8508b2f2279be8dd0d15c536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18587042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427d7302ef3bcba2582701a4f85e1b2aaff5aa646ab33c4b50269616ec061a3d`

```dockerfile
```

-	Layers:
	-	`sha256:c672e1995ca6d367e9ed7965c5551e9306d87a3c73ffa97be9357218dba3b4c5`  
		Last Modified: Fri, 14 Nov 2025 01:37:55 GMT  
		Size: 18.6 MB (18576279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e1e141a638c5ebad4fdd4507023f76998147c02c04e65bb27b4a64dbf57ee6`  
		Last Modified: Fri, 14 Nov 2025 01:37:54 GMT  
		Size: 10.8 KB (10763 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.1-scala2.13-java21-ubuntu`

```console
$ docker pull spark@sha256:ba1366f3a75ddcc1a2f9fea6f03eaad3204c9431d48fb38363f0e73af02cf3f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.1-scala2.13-java21-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:1a2635d7e998a96a507af3da90e74bb84de78e00980f3191ce597e1911ac0e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 MB (671565059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537861e32726c493f1c22b0839e0e6358fabb1a3a3fc228cfbfc976120388272`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:05 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:13 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:08:28 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:08:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:08:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:08:39 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:08:51 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:08:51 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:08:51 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:08:51 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:08:51 GMT
USER spark
# Fri, 16 Jan 2026 01:08:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77e7736fdec006b65bbe1bb0abdb2bf076a4fb1b67089cb602e6a1431964ed`  
		Last Modified: Thu, 15 Jan 2026 22:20:41 GMT  
		Size: 20.7 MB (20688486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab53b7b2400ba6f98bb37e2d40662fa86f1584df7e665bc9488dd47b2d37e9f`  
		Last Modified: Thu, 15 Jan 2026 22:20:54 GMT  
		Size: 157.8 MB (157839010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dfb2663e897777f9a9bf3970e6e2f996b97af462e87e478fb62536aebfd75f`  
		Last Modified: Thu, 15 Jan 2026 22:20:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b156b5a347025523a628f6f438e139290c2bac2a1cb5c0d113e5004a068d8e`  
		Last Modified: Thu, 15 Jan 2026 22:20:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d4e9c15cf9995dfd044a3334a4c1d83bb530051cb2bc5a3204260a080cce5d`  
		Last Modified: Fri, 16 Jan 2026 01:09:36 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bad664bdd84ce2afb55f393473dd9cc1641495c4624173702a3dfe81da06b51`  
		Last Modified: Fri, 16 Jan 2026 01:09:43 GMT  
		Size: 21.9 MB (21850694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e8f7bfcc142ed83d1a5061afcf5041c76bf9a0b321d391c5a06cc43c78b919`  
		Last Modified: Fri, 16 Jan 2026 01:11:22 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fdffd9a41182ab92c7e0a4a40969d8ce95faca43da58907bd2d8c36e0bc5b9`  
		Last Modified: Fri, 16 Jan 2026 01:09:36 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b3174c914ce43a8d49728c055fdf4e191ea11074404a3ca3eafe575cb7cad6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b958a172b4bfb4b664822dda554f5d6400bb64224f7245e2cd3e068de773fe`

```dockerfile
```

-	Layers:
	-	`sha256:f63d70a920bf33cb4b34fd6b841706e9f26fceff78e3ee69a54d9ca47f7dd4ca`  
		Last Modified: Fri, 16 Jan 2026 03:13:14 GMT  
		Size: 5.0 MB (4963825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806743b9a7015dec75b602a0c71b40860ab8a131ff97778b879a12a5d0528d04`  
		Last Modified: Fri, 16 Jan 2026 03:13:15 GMT  
		Size: 23.0 KB (22963 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.1-scala2.13-java21-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9106c69c7364b1bf597fce9c14378da8a0cbfd90ae51d40f4d2b53c84142a08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.8 MB (668786582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9961edf7d8fbfa7b825ecb732de1b2e0ee3f85b1aaa6787d908d7fd0ce16ea`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:23 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:32 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:11:06 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:11:06 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:11:15 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:11:15 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:11:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:11:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:11:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:11:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:11:28 GMT
USER spark
# Fri, 16 Jan 2026 01:11:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493c2f62b1fb2eeb7f16caf75211c2742191586cc868924f24652124cf64a330`  
		Last Modified: Thu, 15 Jan 2026 22:21:03 GMT  
		Size: 22.1 MB (22107475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd81e4068932ff2943205b5e34a7c3ce496d549f89a22362e6255791b8bd9db7`  
		Last Modified: Thu, 15 Jan 2026 23:54:39 GMT  
		Size: 156.1 MB (156107615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0ca63e8dda6e564c2bec761ae086ce8bc75214a4ae61b90de83c0abae8c6a`  
		Last Modified: Thu, 15 Jan 2026 22:21:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ee81093faa209f1b1d40e0fdf45471a90f0497e7932ac88bc3b4b1d403118`  
		Last Modified: Thu, 15 Jan 2026 22:20:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfc82ff8d0cf716bf220922e4e5f841fc7d50afcce2e53079e1212285ab4af`  
		Last Modified: Fri, 16 Jan 2026 01:13:47 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9c6ebb16fc15249fd16f5340c8098a686c6415aaf8be4c66569f5c632eee`  
		Last Modified: Fri, 16 Jan 2026 01:13:49 GMT  
		Size: 21.5 MB (21537861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01ef94eec84118210899406c1c704889c87268544a1327aa52fbe14fab312f1`  
		Last Modified: Fri, 16 Jan 2026 01:16:44 GMT  
		Size: 441.6 MB (441644106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23edfb5ce0735bc5ab82168aaed5ab60ff3d4a014624e806083423e1c358ad4d`  
		Last Modified: Fri, 16 Jan 2026 01:13:47 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.1-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:412f2266e1dd38a384fdfafe3bc79762e3d891babdfc0ae9a0d6ddb38558bb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510fd02777069044bf62550e8942597e19e40b8608ec3db1ef443c91b2466163`

```dockerfile
```

-	Layers:
	-	`sha256:f9c2e45ec7059ef9a372619fe53ad2cdf7421d054b2c4fd86f698501d97265d9`  
		Last Modified: Fri, 16 Jan 2026 03:13:20 GMT  
		Size: 5.1 MB (5059328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60c41703358f1a83dd8c9eb85b6bfe75a262d8958d8ccf76f362eae8d31ceffb`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 23.1 KB (23072 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:latest`

```console
$ docker pull spark@sha256:84738ac8824a2da1d74c225f4371b4e6109295d39ed75eee085d07286505bd55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:63e31a664dc310489593bbc8fa6940a1f6eb829d92995b8ed7a2c8ac17c5e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.3 MB (785264481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03086b8c65cc1e8b1c5c262c2e5fcca8c404962cf7c9fae6ec457aedfe50b957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:40 GMT
USER root
# Fri, 14 Nov 2025 01:19:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:40 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5744c2ff3ef2818580ff98e4c72b03431d4c10df688217345bf3235e344e4286`  
		Last Modified: Tue, 13 Jan 2026 03:00:57 GMT  
		Size: 113.7 MB (113686928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:59d70ef9a16a686e072ffb595f562a57bbc8668ce3509c3a6cff802dc0323927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10435643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaacaae6dfb6e269e647874f8338b045b7955a71010163e311107de8021e777`

```dockerfile
```

-	Layers:
	-	`sha256:765a7110bc892c472020b7f249e2508de146b3883a0afa8f988c140dec94d591`  
		Last Modified: Tue, 13 Jan 2026 07:03:47 GMT  
		Size: 10.4 MB (10424049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79c2976685765bc2ef92e52525d62d2c11c5b7d3420fd95d49ee07217d83cf6`  
		Last Modified: Tue, 13 Jan 2026 07:03:34 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:68e13bc08f99764294fb2d0726db670b5518e2f3284c9689342a0ef1f62213ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 MB (777048485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691bbd4469ce1c3743f6d39d60793d3d28f2008fc8c85dc106b32b11e592a40d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:35:42 GMT
USER root
# Fri, 14 Nov 2025 01:35:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:42 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c5ece496843e6c9d1a0923897c89e59dd6742a3f4c4335a80f19f88e1b3975`  
		Last Modified: Tue, 13 Jan 2026 04:24:36 GMT  
		Size: 108.3 MB (108276034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:b89fc3febef2aa00f549de48d87b0eb2a7ada85e32facb83a24671e3c53e9ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10430232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cddf1b42888a9bbf6c140b7d480fa1f3bd9a834a39739fb7d132dbce2c7d847`

```dockerfile
```

-	Layers:
	-	`sha256:862e22b3e353edb9457e481b012eb3a1f50b2b9c28f7563913c26ff63cbc899d`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 10.4 MB (10418521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b54bca6722798708e9a3b41d59ceed81d33eaa423852b4eb21e7cfab25ecfe0`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:84738ac8824a2da1d74c225f4371b4e6109295d39ed75eee085d07286505bd55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:63e31a664dc310489593bbc8fa6940a1f6eb829d92995b8ed7a2c8ac17c5e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.3 MB (785264481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03086b8c65cc1e8b1c5c262c2e5fcca8c404962cf7c9fae6ec457aedfe50b957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:46 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:46 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:57 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:29 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:29 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:29 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:29 GMT
USER spark
# Fri, 14 Nov 2025 00:40:29 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:40 GMT
USER root
# Fri, 14 Nov 2025 01:19:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:40 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01facf544478e1a2955676ca1741ac59c36b2e80ddaa739f43812a4585b704e7`  
		Last Modified: Tue, 13 Jan 2026 00:56:35 GMT  
		Size: 20.7 MB (20700743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974368270e4f573ff1edaae07b59b84ccaff6997873cccde92a19c7ec978851`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 157.8 MB (157838972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f51c3d063559e2c0d0a8f88d051dff78b56bec8c4f6769d9947a96f87f917`  
		Last Modified: Tue, 13 Jan 2026 00:56:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d80376fd82870628b01ae6f01bd27552bc9aa3a4cd5be88515f79fe298a87a`  
		Last Modified: Tue, 13 Jan 2026 00:54:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89435976ade4bf9ffdab347cc2127ece8ed171d95b0637e367a5c619758f0b7`  
		Last Modified: Tue, 13 Jan 2026 01:35:34 GMT  
		Size: 21.9 MB (21850857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063390a3e34276a9a0c4eb5112ce7cb4f3f3ea6e364bf6a50ce8df86cde9a42`  
		Last Modified: Tue, 13 Jan 2026 03:01:05 GMT  
		Size: 441.6 MB (441644158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd2dd572a13075d6aa464c831107623ada0a6713598bd0ede7b5e8153d3c9a`  
		Last Modified: Tue, 13 Jan 2026 01:35:05 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5744c2ff3ef2818580ff98e4c72b03431d4c10df688217345bf3235e344e4286`  
		Last Modified: Tue, 13 Jan 2026 03:00:57 GMT  
		Size: 113.7 MB (113686928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:59d70ef9a16a686e072ffb595f562a57bbc8668ce3509c3a6cff802dc0323927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10435643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaacaae6dfb6e269e647874f8338b045b7955a71010163e311107de8021e777`

```dockerfile
```

-	Layers:
	-	`sha256:765a7110bc892c472020b7f249e2508de146b3883a0afa8f988c140dec94d591`  
		Last Modified: Tue, 13 Jan 2026 07:03:47 GMT  
		Size: 10.4 MB (10424049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79c2976685765bc2ef92e52525d62d2c11c5b7d3420fd95d49ee07217d83cf6`  
		Last Modified: Tue, 13 Jan 2026 07:03:34 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:68e13bc08f99764294fb2d0726db670b5518e2f3284c9689342a0ef1f62213ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 MB (777048485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691bbd4469ce1c3743f6d39d60793d3d28f2008fc8c85dc106b32b11e592a40d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:40:33 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:40:33 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:40:43 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:56 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:56 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:56 GMT
USER spark
# Fri, 14 Nov 2025 00:40:56 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:35:42 GMT
USER root
# Fri, 14 Nov 2025 01:35:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:42 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecb6e88fc36fb41b415f06176f9b74e274e739250977c09acebf8816ecf286`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 22.1 MB (22092833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd987826e3dd6fd09ed91b426f49a8d6a16bc6bf3b7fc9aafe7c6a1826610d09`  
		Last Modified: Tue, 13 Jan 2026 00:59:00 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2466544f7fad579bcd489c810f646e3bdb9906072a8f5cb406091b1e34db27`  
		Last Modified: Tue, 13 Jan 2026 00:55:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Tue, 13 Jan 2026 00:55:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64451e4b5a9a3a3a2883a2de890bb8c85ddf1bd9debf2182e4486f8f4fd54c`  
		Last Modified: Tue, 13 Jan 2026 04:24:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c19695da78e32ba6ac8294bae4f0a44b0e0451c11867e699320de865ad3bfd`  
		Last Modified: Tue, 13 Jan 2026 04:24:14 GMT  
		Size: 21.5 MB (21538003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52716093a1b821d39385d58928b1457eec4e04c3de80feec5a7b3c5725eee`  
		Last Modified: Tue, 13 Jan 2026 04:24:34 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e186bec97414ada2872e728ad6d4167971c992a17fa632788a3934aa85563f6a`  
		Last Modified: Tue, 13 Jan 2026 04:24:11 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c5ece496843e6c9d1a0923897c89e59dd6742a3f4c4335a80f19f88e1b3975`  
		Last Modified: Tue, 13 Jan 2026 04:24:36 GMT  
		Size: 108.3 MB (108276034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:b89fc3febef2aa00f549de48d87b0eb2a7ada85e32facb83a24671e3c53e9ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10430232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cddf1b42888a9bbf6c140b7d480fa1f3bd9a834a39739fb7d132dbce2c7d847`

```dockerfile
```

-	Layers:
	-	`sha256:862e22b3e353edb9457e481b012eb3a1f50b2b9c28f7563913c26ff63cbc899d`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 10.4 MB (10418521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b54bca6722798708e9a3b41d59ceed81d33eaa423852b4eb21e7cfab25ecfe0`  
		Last Modified: Tue, 13 Jan 2026 05:55:38 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:10d82ec4a2ddb2ab04e895b183ef3d8bfa81c1e15966afd70a02a47a653e18b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:54c0faa057db288676532e00395f4994953e183eecfe6249800ea91f8b4023d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 MB (772276685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c440479d95c1f8bfe55c6bbc4fff92a0f1664b2c25693f96be7903b4221bcb5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:19:53 GMT
USER root
# Fri, 14 Nov 2025 01:19:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:19:53 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6c0b15beb1f7c2add40ff91df8173eb94b17d3b34dc560d9d82c266195f3d4`  
		Last Modified: Tue, 13 Jan 2026 03:14:31 GMT  
		Size: 113.7 MB (113686819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:7ec8febb51c60fa5983b45933aa939c481d56c81106d505a0d419b4385f6377b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dc4d76299acff30771c8f7565266ff42857b90c756bd62c30439e328ee44a3`

```dockerfile
```

-	Layers:
	-	`sha256:f4a5066b60365e0f34aaa959ac9b90ed7ad3aa3daa2a6f940ddaf5b7db296be4`  
		Last Modified: Tue, 13 Jan 2026 12:04:52 GMT  
		Size: 10.4 MB (10420637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de90fa4611af7c0ed1c1c9bd5a92b18dcdf42b58fc500855dcbbaac244d68459`  
		Last Modified: Tue, 13 Jan 2026 12:04:51 GMT  
		Size: 11.3 KB (11286 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4c7b62625fabdf7510fd9289d7287970adca7ef32cf4d73b26881e96531f858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.6 MB (764622390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff32243530b87b56022f2a2eb11b0ff1af7e53eb72432325a239c174a055c483`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:36:20 GMT
USER root
# Fri, 14 Nov 2025 01:36:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:36:20 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581918ddba692095c8771fa5610fa309618e3b6d07b379998cf2509c39c723ff`  
		Last Modified: Tue, 13 Jan 2026 10:11:40 GMT  
		Size: 108.3 MB (108276240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:c10f200c9b24e06e9de5327434ff9eff6b91f5552256f103c853ea07fecd68e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10426487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ac90a0d41df63778af9e4adeb3fba6ccc54738c357fd0e83c7239a60aff49`

```dockerfile
```

-	Layers:
	-	`sha256:2decabcd1a004a7777ce414910e1a222e5935ab648ab17346f8817f24dbf814c`  
		Last Modified: Tue, 13 Jan 2026 10:40:27 GMT  
		Size: 10.4 MB (10415097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35dd24331d7eb13ea99c56d120693a8db251a5df7be18783b5e48873e8058db`  
		Last Modified: Tue, 13 Jan 2026 10:40:26 GMT  
		Size: 11.4 KB (11390 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:r`

```console
$ docker pull spark@sha256:11a21d0df03fe4e8e625ff25a781961f8e1ef0f98f41dc7844ef9f2d255fd8c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:c0cac1cf2ea853b3ddd96cd31f5af6cd736ee40514be0c78308eb309987e3517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.7 MB (977736656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b59da1863dcfdfdde0b52316727a9b0c733ea0661c2d3645dd190e02690d229`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:21:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:39:45 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:39:45 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:39:55 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:40:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:40:28 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:40:28 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:40:28 GMT
USER spark
# Fri, 14 Nov 2025 00:40:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:20:42 GMT
USER root
# Fri, 14 Nov 2025 01:20:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:42 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:20:42 GMT
USER spark
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e106dd8ed6ad2e6cce7b8a0e8ec5a228fd591f46f34a5c649b68ec66090c4e67`  
		Last Modified: Tue, 13 Jan 2026 01:01:27 GMT  
		Size: 20.7 MB (20700812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a3134bb3a9ba57065c495a66645b15abc9c0d5239598e0efa785944e1d877`  
		Last Modified: Tue, 13 Jan 2026 01:02:22 GMT  
		Size: 144.9 MB (144851556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837687f10a1f82571090fcd9ad0528fcc7b5f43242cc1c6b76f6afefdff0a2d6`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Tue, 13 Jan 2026 00:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892f13c311d1d1a818636efd4a177b56dd17fc664225df506aa7060fea257e3c`  
		Last Modified: Tue, 13 Jan 2026 01:02:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac64952b7233b658c040139bf49d1ed0f48d0d96f102df9dfe4a63b108675b`  
		Last Modified: Tue, 13 Jan 2026 01:02:18 GMT  
		Size: 21.9 MB (21850569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca49e9b1fdac5fe5b1afc5675e6951bf6bddeb62c6350a98b8c877d08bc874a`  
		Last Modified: Tue, 13 Jan 2026 03:02:29 GMT  
		Size: 441.6 MB (441644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58772a9f9b581314a98c4bcddc341f9e84af7c6d4d11bb0becef4154628ac4d4`  
		Last Modified: Tue, 13 Jan 2026 01:02:19 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd980dead91451bfbc34750030cc61a1d59c15517362e71a04673af50e5ebccb`  
		Last Modified: Wed, 14 Jan 2026 21:24:54 GMT  
		Size: 319.1 MB (319146790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:11cb3e5896d6f98921ebaae45ba72593e0bfd05beee24934bbf35b369ef744d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18619852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f9ff84084064b0b359035da19233b4fa3dadc0f17dec0c81395b759e78978`

```dockerfile
```

-	Layers:
	-	`sha256:7b6ca02a6a477677b1dcf1f5c26bdcdebe70aef34ae9da060db8262d5c1c1754`  
		Last Modified: Fri, 14 Nov 2025 01:21:35 GMT  
		Size: 18.6 MB (18608896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29bea142bbd31c6363379711341a13bba22d4d06bfd39a9fe04df65ecb321ab2`  
		Last Modified: Fri, 14 Nov 2025 01:21:33 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:3b80e15381cf6b61a836c3f74e2a2630336d95c8a03b38a4c5c9efb7af44be66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.7 MB (958723807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e643c763d9ec411260be6d5b6a946d0243b446d8cc7278e1be3edcd5166aa5d8`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 00:41:03 GMT
ARG spark_uid=185
# Fri, 14 Nov 2025 00:41:03 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:41:17 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 14 Nov 2025 00:41:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 14 Nov 2025 00:41:31 GMT
WORKDIR /opt/spark/work-dir
# Fri, 14 Nov 2025 00:41:31 GMT
USER spark
# Fri, 14 Nov 2025 00:41:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 14 Nov 2025 01:37:08 GMT
USER root
# Fri, 14 Nov 2025 01:37:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:37:08 GMT
ENV R_HOME=/usr/lib/R
# Fri, 14 Nov 2025 01:37:08 GMT
USER spark
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2849897877d222c1e47f4429bc201f8dac9e3928b5f62477e65322fd20e6cf6`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 22.1 MB (22092876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c06c2c11bfa511856423cf486ac48acb38c2f29e20be0ac73a2d2668e399c`  
		Last Modified: Tue, 13 Jan 2026 00:57:38 GMT  
		Size: 143.7 MB (143681319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a2e4244e8b79db4007b78580a88314aee875e6c48a36da752cac522391607`  
		Last Modified: Tue, 13 Jan 2026 00:57:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8af0f08fed4c71fd62423d57cad381de9b8d23034d0f441b1723bb9537782`  
		Last Modified: Tue, 13 Jan 2026 00:57:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108f82234d377fa94241db6825035d912d3928634399e1769691ca5112aeaef`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098b44a23922a9871d86fda4a3f7c59ad214ce9885162232a2b23eaeb2767bf`  
		Last Modified: Tue, 13 Jan 2026 01:37:47 GMT  
		Size: 21.5 MB (21537994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ae10611d88bce9d0514566672932f4b3ed4908ee37aaec28fdee1969962c`  
		Last Modified: Tue, 13 Jan 2026 10:11:51 GMT  
		Size: 441.6 MB (441644050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658a12fbc8aeb8fd457eeeaf788117883542594de4a838374d8ad7c72744c5a`  
		Last Modified: Tue, 13 Jan 2026 01:37:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdef43c0f11c86fb05c4b2bf024ed807e36ae26d8b4945b257f5e0a4d295ee2f`  
		Last Modified: Fri, 14 Nov 2025 01:38:08 GMT  
		Size: 302.4 MB (302377657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:e3025df6c37c8816746b88105f882e33ff72b90071e8a9a6935006e39a267210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18584509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93cc93127a5b9acb9996d40b2ccb17ddc89b5b4b355109bbd5eb8032be21e34`

```dockerfile
```

-	Layers:
	-	`sha256:40592b19336d8e196854b806088803070cdcf14256fe11c8c7995d1832978c1c`  
		Last Modified: Fri, 14 Nov 2025 01:38:01 GMT  
		Size: 18.6 MB (18573461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3883515069edb7d45d094ae20a8d729d479aa5421ecb679706bc8261bba2c7`  
		Last Modified: Fri, 14 Nov 2025 01:38:00 GMT  
		Size: 11.0 KB (11048 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:scala`

```console
$ docker pull spark@sha256:978661143403e30c831851a25b2c1e85eb04e5e27fccea9721184b8852159c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:5479d4469a489290f6f5b73e6369b1e82d7a426da7a7f74a5cdc0503f1ac868c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.6 MB (658577133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7ffcc31b0856ca24a002f760e385d42d33d1165d43f4cb1f584b8e2d018194`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:52 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:09:21 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:09:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:09:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:09:32 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:09:44 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:09:44 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:09:44 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:09:44 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:09:44 GMT
USER spark
# Fri, 16 Jan 2026 01:09:44 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ede50ffae3ced1f5ffed35549b8bac68387426b88ec95cdbcc82baf2fd33f`  
		Last Modified: Thu, 15 Jan 2026 22:20:18 GMT  
		Size: 20.7 MB (20688694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227b76b41c25c5c0ce948a17f2d8308398b5dc827c545c7142ca20f30b1cb256`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 144.9 MB (144850896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589743ef81c842f54b86e7e96cf9a3ce388b1e8e676068f5d16a511dd91fccfb`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70ee470d498578f3f261d731c31f16ca9c9f5f583ac83347ec39bc91ed183dc`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac811d8620bc57d872722ac4910288a89e8581d9ed0551a130ad9c64767e04`  
		Last Modified: Fri, 16 Jan 2026 01:10:28 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aa7237a5f72f89ff3782080245fd12a0be926874d28bc85603eb7d31ee6d07`  
		Last Modified: Fri, 16 Jan 2026 01:10:30 GMT  
		Size: 21.9 MB (21850674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3636baf6ed3807b0750514e6bd544c1ea1c5aa2081d9429e02c771406ff019f3`  
		Last Modified: Fri, 16 Jan 2026 01:12:40 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a3a74c95017f38125de35d632f73dad1649f9d50c2e3c0cf9860c49c549d0f`  
		Last Modified: Fri, 16 Jan 2026 01:10:28 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:a1be5df6e184c99f740f40fa0319981a4440bbcce2d28c5037026434f79b3b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20843b82234c150e2905a4997342962a2aab1e2c79db62812f7377dc54afd91`

```dockerfile
```

-	Layers:
	-	`sha256:d3fa23949a3c498feed638209111733c3ddfb12f47164d4a8acacf131e7b93f3`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 5.0 MB (4961003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c325fb71069d0fd1fee1c7ef1b3fdcbe4aae4da48991a95a3dc6c9ae1dd096`  
		Last Modified: Fri, 16 Jan 2026 03:13:21 GMT  
		Size: 23.2 KB (23246 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:486dab03bc3059acf0617ab83ca06f992411bdd964ec0089c3e9ed6b51e475bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.4 MB (656360295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756e7ab3e7f9bf11227501cd89b02b2b3bddde0d594bfc198499b588236faf64`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:18 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:12:17 GMT
ARG spark_uid=185
# Fri, 16 Jan 2026 01:12:17 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark -d /nonexistent spark # buildkit
# Fri, 16 Jan 2026 01:12:25 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:12:25 GMT
ENV SPARK_TGZ_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz?action=download SPARK_TGZ_ASC_URL=https://www.apache.org/dyn/closer.lua/spark/spark-4.0.1/spark-4.0.1-bin-hadoop3.tgz.asc?action=download GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 16 Jan 2026 01:12:37 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 16 Jan 2026 01:12:37 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 16 Jan 2026 01:12:37 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 16 Jan 2026 01:12:37 GMT
WORKDIR /opt/spark/work-dir
# Fri, 16 Jan 2026 01:12:37 GMT
USER spark
# Fri, 16 Jan 2026 01:12:37 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f84e430918f56b2a3b21400c38155cc3747e29ae43bf89ec7bd1a2d206b818`  
		Last Modified: Thu, 15 Jan 2026 22:19:47 GMT  
		Size: 22.1 MB (22107474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adfc04002164e831afd68d878fa3bbe3cc04f413d131d3222fbedebb7dda33`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 143.7 MB (143681283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b23fdceb460806f1b4d37e8e1d0a03126441b8a0d1efe1ad54d2d05fce4d1`  
		Last Modified: Thu, 15 Jan 2026 22:19:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7feaec1b5ae6c7e6e38638d964d4991ce35f3a13191880a163bdef3d12c7312`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d93a4122d19034a36085227ce22f88e160cba24899cefba8a716ee8cb6c532`  
		Last Modified: Fri, 16 Jan 2026 01:13:20 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9c4b7a4c814851146b036c758c57eaf037ccd0379f814dd4f532033a325099`  
		Last Modified: Fri, 16 Jan 2026 01:13:22 GMT  
		Size: 21.5 MB (21537840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1f217834cbb15d4dcddf79d4bfd1f94e6db6d4066803685d051b15938795fe`  
		Last Modified: Fri, 16 Jan 2026 01:13:47 GMT  
		Size: 441.6 MB (441644170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafd9920332da7a567896960fe8d43ca03d5d622e21a92a39709b70f48cd8ac9`  
		Last Modified: Fri, 16 Jan 2026 01:13:20 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:4c8ed362a6ab8a11795acef324f175480a6529fba08e3090bf0a493e87ac3b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd871afea0d83865878ea5559202edb8a47f708c5ea9ce6ffda8bb35e4576fa`

```dockerfile
```

-	Layers:
	-	`sha256:a8fd8bb7f44216601d1a328cc0a898bcdb07e3431fcf7db336742c426d0d956a`  
		Last Modified: Fri, 16 Jan 2026 03:13:27 GMT  
		Size: 5.1 MB (5056518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075a3508c9e74bbc6ca9c51623c0b485546a97d97184f5d7be3be4c02d590b18`  
		Last Modified: Fri, 16 Jan 2026 03:13:27 GMT  
		Size: 23.4 KB (23368 bytes)  
		MIME: application/vnd.in-toto+json
