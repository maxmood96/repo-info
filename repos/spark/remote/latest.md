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
