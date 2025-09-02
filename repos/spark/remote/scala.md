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
		Last Modified: Tue, 02 Sep 2025 08:54:45 GMT  
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
