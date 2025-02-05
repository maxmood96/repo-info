## `spark:python3-java17`

```console
$ docker pull spark@sha256:fc4737f79bb92df7509e17aede94c30c3d0c198087c207d6b32ba0c96ce984a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:3f506214f16aed31c8eb1dfd6ec29a4cb44d97047ca57a3f253ecca8efbd22b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.1 MB (655118022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df68300abeea765b42026743fc85c2b9a3b75bd05b272930001882c89ef717b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Dec 2024 05:28:31 GMT
ARG RELEASE
# Sun, 22 Dec 2024 05:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Dec 2024 05:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 22 Dec 2024 05:28:31 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Dec 2024 05:28:31 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89754ea33f26ef5f0e374c5b58928fc9f32ae72511a65a448c530a08a6ae9cb`  
		Last Modified: Tue, 04 Feb 2025 04:39:38 GMT  
		Size: 20.7 MB (20684652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e061bf326705adbdbd41ea0f52cd50dcf0b9c49e3d56d37560a8e1d0283e302`  
		Last Modified: Tue, 04 Feb 2025 04:39:39 GMT  
		Size: 144.6 MB (144576171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb685c542356d2b58335a3d0bd731d14276ffa9c85ee8a97cfc73cd71fa0981`  
		Last Modified: Tue, 04 Feb 2025 04:39:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962e188c6768410618da1fedec40bdc9c48f06c0d5e22cbd29875abe2d97865`  
		Last Modified: Tue, 04 Feb 2025 04:39:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee40b8f1abe5ed12966821907aa6e85ae5e80f297b841e874a9c314f74fc40a4`  
		Last Modified: Tue, 04 Feb 2025 05:27:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13edcea7313a31858eaadcea9632e0dba568ddd6a096d8f296d15f86eb8da5da`  
		Last Modified: Tue, 04 Feb 2025 05:27:07 GMT  
		Size: 21.7 MB (21687520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda1edff2e17af9beab5925e5e3214ad2556d2bff738a20eba766549bfbc900`  
		Last Modified: Tue, 04 Feb 2025 05:27:12 GMT  
		Size: 324.9 MB (324901717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b39fbffd95f6266cd7e0680fff8ca838189f20a83d19162a0fde4e1d93c673`  
		Last Modified: Tue, 04 Feb 2025 05:27:07 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ee8d4839803ce37e404c48302e7d20f2be2e0b580c49c34173b91878a9d5ca`  
		Last Modified: Tue, 04 Feb 2025 06:16:34 GMT  
		Size: 113.7 MB (113725987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:3e1387f040185ae45a362d7b1e141ca69940f85821f7955f61500e051ac5bab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9959493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05590e907772d863ea69724e61299a3a64e374f99fed25bf3bce3612230cfd12`

```dockerfile
```

-	Layers:
	-	`sha256:b886a60dc8b1285c327b525ba08c83585704b199cd229578d036abb00f6fa82e`  
		Last Modified: Tue, 04 Feb 2025 06:16:32 GMT  
		Size: 9.9 MB (9948181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48903d161ef5c520d9004a2cfba7c7231eb423005bc1f4aa5db20b971ef9bb3f`  
		Last Modified: Tue, 04 Feb 2025 06:16:32 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f2a7fa8251726c91ab958511e7d9580cb319dae1dd4c76861d17408f0cfe6a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.4 MB (647431859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21c732b387336add86b1434a705378c9b3c4f49d05188cd5567c418acf2b485`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Dec 2024 05:28:31 GMT
ARG RELEASE
# Sun, 22 Dec 2024 05:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Dec 2024 05:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 22 Dec 2024 05:28:31 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Dec 2024 05:28:31 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917805cfb6502c189ce3cf996ddbc16ac349000799293570d30f8455b5182667`  
		Last Modified: Tue, 04 Feb 2025 09:21:30 GMT  
		Size: 22.1 MB (22066656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aebdf20ee58fb630cab5ed629f4cdd7232ca7253a7d47dbd5e92a4f972f3b8f`  
		Last Modified: Tue, 04 Feb 2025 09:21:33 GMT  
		Size: 143.5 MB (143461717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b79ad980c16a20e57fcb258fcfb5ce3127a0d73d82b6f282092e9a717f3653`  
		Last Modified: Tue, 04 Feb 2025 09:21:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8c76f02186a08c7df18954b0f74e1a6511d8a72656f3984fb0b1d298c3ae0f`  
		Last Modified: Tue, 04 Feb 2025 09:21:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695061303239004605b6b0c8d1271dd9b5c280cc8c3a315be08c8f4757f676c1`  
		Last Modified: Tue, 04 Feb 2025 22:35:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64599368deb3a9ee5dbcd40e3feebe61bb7ad6eced67cd7d884adeb80d584630`  
		Last Modified: Tue, 04 Feb 2025 22:35:39 GMT  
		Size: 21.4 MB (21354981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ce0f3b4430335aa354595bf63dd9b5397f1afab9d6aed7f7b3f133c4959820`  
		Last Modified: Tue, 04 Feb 2025 22:37:13 GMT  
		Size: 324.9 MB (324901759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8f0bccc0053c7f75f56b6fa7a3a5d2918374cac9a1527436f9bf1bae72697c`  
		Last Modified: Tue, 04 Feb 2025 22:37:05 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c351d6f78b2324119bb1aba30567b68a12cfc511fca6e2a900094e2b5fec3e`  
		Last Modified: Wed, 05 Feb 2025 04:26:10 GMT  
		Size: 108.3 MB (108282528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:cc6384e31274f7a48d05263a11800a8a3728f998fbc0c2b3ba866e7a06c8520b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9954055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b445bdc4198bac0b0e0c7f97718b2a85962b09a68400e39e523038fe4223ee`

```dockerfile
```

-	Layers:
	-	`sha256:87b8ea8b40442d3e23abaed5153bde1cd3bd48e98a269cc35a9026934a1b65eb`  
		Last Modified: Wed, 05 Feb 2025 04:26:07 GMT  
		Size: 9.9 MB (9942639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c889d8fa7f3c1de5f37dbc0135a4e03e22257ab4d5ff4bf877fe869a2963dbe4`  
		Last Modified: Wed, 05 Feb 2025 04:26:06 GMT  
		Size: 11.4 KB (11416 bytes)  
		MIME: application/vnd.in-toto+json
