<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `flink`

-	[`flink:1.15`](#flink115)
-	[`flink:1.15-java11`](#flink115-java11)
-	[`flink:1.15-java8`](#flink115-java8)
-	[`flink:1.15-scala_2.12`](#flink115-scala_212)
-	[`flink:1.15-scala_2.12-java11`](#flink115-scala_212-java11)
-	[`flink:1.15-scala_2.12-java8`](#flink115-scala_212-java8)
-	[`flink:1.15.3`](#flink1153)
-	[`flink:1.15.3-java11`](#flink1153-java11)
-	[`flink:1.15.3-java8`](#flink1153-java8)
-	[`flink:1.15.3-scala_2.12`](#flink1153-scala_212)
-	[`flink:1.15.3-scala_2.12-java11`](#flink1153-scala_212-java11)
-	[`flink:1.15.3-scala_2.12-java8`](#flink1153-scala_212-java8)
-	[`flink:1.16`](#flink116)
-	[`flink:1.16-java11`](#flink116-java11)
-	[`flink:1.16-java8`](#flink116-java8)
-	[`flink:1.16-scala_2.12`](#flink116-scala_212)
-	[`flink:1.16-scala_2.12-java11`](#flink116-scala_212-java11)
-	[`flink:1.16-scala_2.12-java8`](#flink116-scala_212-java8)
-	[`flink:1.16.0`](#flink1160)
-	[`flink:1.16.0-java11`](#flink1160-java11)
-	[`flink:1.16.0-java8`](#flink1160-java8)
-	[`flink:1.16.0-scala_2.12`](#flink1160-scala_212)
-	[`flink:1.16.0-scala_2.12-java11`](#flink1160-scala_212-java11)
-	[`flink:1.16.0-scala_2.12-java8`](#flink1160-scala_212-java8)
-	[`flink:java11`](#flinkjava11)
-	[`flink:java8`](#flinkjava8)
-	[`flink:latest`](#flinklatest)
-	[`flink:scala_2.12`](#flinkscala_212)
-	[`flink:scala_2.12-java11`](#flinkscala_212-java11)
-	[`flink:scala_2.12-java8`](#flinkscala_212-java8)

## `flink:1.15`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-java11`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-java11` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-java8`

```console
$ docker pull flink@sha256:46f5562036217a4b5ee5147d6a4e138b3c79f7bff5c9af3dc692a08114ff8659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-java8` - linux; amd64

```console
$ docker pull flink@sha256:7976dc54ce3e619f2577af0db8e86e3395a86c217f8eaa4fc457c8381e4b9fd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526518740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad6a9786c1328d020bee638b364259b5db1e37f0565a9248375c6bab1ad5f67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:10 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:11 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:11 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:24:30 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:24:31 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:24:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:24:31 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:24:31 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4754904bbde826f6978e1ed2d88531a3f5146953c11dababfae32a60cd47f42`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f717668d8bfea5f9730b1a62602429f7f910f47b0faefbe180a3699f37187be7`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa73b7ab9dfad37276418dd6c14fd3b7428ed77e26d4a460b2d702dd881b3b4`  
		Last Modified: Mon, 05 Dec 2022 21:26:03 GMT  
		Size: 436.3 MB (436275246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5f6419e4d2c1132028fb13c5003de60a34add8cd849d0260449d0552996d9b`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:c8c24a8057a7df4973831937fc0aaf5d95c9484b33ef0ae0e00a45dd34f54419
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.2 MB (523205351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dfe98333e4a57138175aa3d6c856494ff3ce3fff17bbc79d2bdb6c81924b84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:01 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:21 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:21 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:21 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9738be50e89e64805937642c2ade4bea80487f4f5e2d5093ab4071bc1958396b`  
		Last Modified: Mon, 05 Dec 2022 20:45:29 GMT  
		Size: 4.6 KB (4647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313fd383768c3b7b315dc6a4bd3ae518fde984928cc9919d1f1b60fb0f952156`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979808c2884d0a63b49f0a33ef00f78b1d46f1834d32ecfa755e42d78331ca6c`  
		Last Modified: Mon, 05 Dec 2022 20:45:44 GMT  
		Size: 436.3 MB (436275294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edda9cc942e34b78ec1cfbdd85b84cb86d3954b84b95b1cf75d45c2f8bb39633`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-scala_2.12`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-scala_2.12-java11`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-scala_2.12-java8`

```console
$ docker pull flink@sha256:46f5562036217a4b5ee5147d6a4e138b3c79f7bff5c9af3dc692a08114ff8659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:7976dc54ce3e619f2577af0db8e86e3395a86c217f8eaa4fc457c8381e4b9fd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526518740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad6a9786c1328d020bee638b364259b5db1e37f0565a9248375c6bab1ad5f67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:10 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:11 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:11 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:24:30 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:24:31 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:24:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:24:31 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:24:31 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4754904bbde826f6978e1ed2d88531a3f5146953c11dababfae32a60cd47f42`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f717668d8bfea5f9730b1a62602429f7f910f47b0faefbe180a3699f37187be7`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa73b7ab9dfad37276418dd6c14fd3b7428ed77e26d4a460b2d702dd881b3b4`  
		Last Modified: Mon, 05 Dec 2022 21:26:03 GMT  
		Size: 436.3 MB (436275246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5f6419e4d2c1132028fb13c5003de60a34add8cd849d0260449d0552996d9b`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:c8c24a8057a7df4973831937fc0aaf5d95c9484b33ef0ae0e00a45dd34f54419
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.2 MB (523205351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dfe98333e4a57138175aa3d6c856494ff3ce3fff17bbc79d2bdb6c81924b84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:01 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:21 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:21 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:21 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9738be50e89e64805937642c2ade4bea80487f4f5e2d5093ab4071bc1958396b`  
		Last Modified: Mon, 05 Dec 2022 20:45:29 GMT  
		Size: 4.6 KB (4647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313fd383768c3b7b315dc6a4bd3ae518fde984928cc9919d1f1b60fb0f952156`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979808c2884d0a63b49f0a33ef00f78b1d46f1834d32ecfa755e42d78331ca6c`  
		Last Modified: Mon, 05 Dec 2022 20:45:44 GMT  
		Size: 436.3 MB (436275294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edda9cc942e34b78ec1cfbdd85b84cb86d3954b84b95b1cf75d45c2f8bb39633`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.3`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.3` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.3` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.3-java11`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.3-java11` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.3-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.3-java8`

```console
$ docker pull flink@sha256:46f5562036217a4b5ee5147d6a4e138b3c79f7bff5c9af3dc692a08114ff8659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.3-java8` - linux; amd64

```console
$ docker pull flink@sha256:7976dc54ce3e619f2577af0db8e86e3395a86c217f8eaa4fc457c8381e4b9fd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526518740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad6a9786c1328d020bee638b364259b5db1e37f0565a9248375c6bab1ad5f67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:10 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:11 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:11 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:24:30 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:24:31 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:24:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:24:31 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:24:31 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4754904bbde826f6978e1ed2d88531a3f5146953c11dababfae32a60cd47f42`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f717668d8bfea5f9730b1a62602429f7f910f47b0faefbe180a3699f37187be7`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa73b7ab9dfad37276418dd6c14fd3b7428ed77e26d4a460b2d702dd881b3b4`  
		Last Modified: Mon, 05 Dec 2022 21:26:03 GMT  
		Size: 436.3 MB (436275246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5f6419e4d2c1132028fb13c5003de60a34add8cd849d0260449d0552996d9b`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.3-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:c8c24a8057a7df4973831937fc0aaf5d95c9484b33ef0ae0e00a45dd34f54419
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.2 MB (523205351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dfe98333e4a57138175aa3d6c856494ff3ce3fff17bbc79d2bdb6c81924b84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:01 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:21 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:21 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:21 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9738be50e89e64805937642c2ade4bea80487f4f5e2d5093ab4071bc1958396b`  
		Last Modified: Mon, 05 Dec 2022 20:45:29 GMT  
		Size: 4.6 KB (4647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313fd383768c3b7b315dc6a4bd3ae518fde984928cc9919d1f1b60fb0f952156`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979808c2884d0a63b49f0a33ef00f78b1d46f1834d32ecfa755e42d78331ca6c`  
		Last Modified: Mon, 05 Dec 2022 20:45:44 GMT  
		Size: 436.3 MB (436275294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edda9cc942e34b78ec1cfbdd85b84cb86d3954b84b95b1cf75d45c2f8bb39633`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.3-scala_2.12`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.3-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.3-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.3-scala_2.12-java11`

```console
$ docker pull flink@sha256:d09c48071603b10d5626211fd9ced41df9d69eb21286763bf6a649288b19d662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.3-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:36af4bc996db086003869ab17d92961003202e2ec233fbabb4bb01fd1ece56e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531330084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45941d61b8921f8f620f1bfdf5efccaa27a4a896c3615b773b818f961fbb535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:34 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:34 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:35 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:25:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:25:02 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:25:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:25:02 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:25:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6a2071b8d0f279394741a750908aacc6693829ce021c80de3889403fea950`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a738e981251ed6a18a73d05b496bae486058f3614647538b73cb56f757053e7`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cbf225b322ad8af02146bf3a0d8ffae3b52f690a69f886d2baa28881f8bbf`  
		Last Modified: Mon, 05 Dec 2022 21:26:36 GMT  
		Size: 436.3 MB (436275295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe7781e4d61172e1b8b6ab6499fbb64485d1f4fa3c8a07b1c661c42b5deeb65`  
		Last Modified: Mon, 05 Dec 2022 21:26:17 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.3-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:21b618f60252206657fbfc634291ffea5351e75ebe302ff1fa038deb960ee136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 MB (527356496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51133c44f647ab0e4146befba145829c9b95f6ac908026b6d954d5549dbab43c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:24 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:24 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:25 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:42 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:45 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:45 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:45 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423c6f69db90079d52351839ebaa8c6c976ee25be919cdc471bfd88d5014015`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cd8989c3eaf5e26d1e026b3e0497682d2fbe955d3771a31c801af0d61da619`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0ea359a48885bd88c124e59ec77548b51ff17b31619d0941854aeaaf58114`  
		Last Modified: Mon, 05 Dec 2022 20:46:15 GMT  
		Size: 436.3 MB (436275254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6babb98e9356d12cfafa1b2d21c330da6914ac8a8c1b9d33e6885e7a75e360a`  
		Last Modified: Mon, 05 Dec 2022 20:45:59 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.3-scala_2.12-java8`

```console
$ docker pull flink@sha256:46f5562036217a4b5ee5147d6a4e138b3c79f7bff5c9af3dc692a08114ff8659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.3-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:7976dc54ce3e619f2577af0db8e86e3395a86c217f8eaa4fc457c8381e4b9fd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526518740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad6a9786c1328d020bee638b364259b5db1e37f0565a9248375c6bab1ad5f67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 21:24:10 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 21:24:10 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 21:24:11 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 21:24:11 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 21:24:30 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 21:24:31 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 21:24:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:24:31 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 21:24:31 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4754904bbde826f6978e1ed2d88531a3f5146953c11dababfae32a60cd47f42`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 4.6 KB (4613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f717668d8bfea5f9730b1a62602429f7f910f47b0faefbe180a3699f37187be7`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa73b7ab9dfad37276418dd6c14fd3b7428ed77e26d4a460b2d702dd881b3b4`  
		Last Modified: Mon, 05 Dec 2022 21:26:03 GMT  
		Size: 436.3 MB (436275246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5f6419e4d2c1132028fb13c5003de60a34add8cd849d0260449d0552996d9b`  
		Last Modified: Mon, 05 Dec 2022 21:25:44 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.3-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:c8c24a8057a7df4973831937fc0aaf5d95c9484b33ef0ae0e00a45dd34f54419
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.2 MB (523205351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dfe98333e4a57138175aa3d6c856494ff3ce3fff17bbc79d2bdb6c81924b84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.3/flink-1.15.3-bin-scala_2.12.tgz.asc GPG_KEY=90755B0A184BD9FFD22B6BE19D4F76C84EC11E37 CHECK_GPG=true
# Mon, 05 Dec 2022 20:44:01 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 05 Dec 2022 20:44:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Dec 2022 20:44:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Mon, 05 Dec 2022 20:44:01 GMT
WORKDIR /opt/flink
# Mon, 05 Dec 2022 20:44:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Mon, 05 Dec 2022 20:44:21 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Mon, 05 Dec 2022 20:44:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:44:21 GMT
EXPOSE 6123 8081
# Mon, 05 Dec 2022 20:44:21 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9738be50e89e64805937642c2ade4bea80487f4f5e2d5093ab4071bc1958396b`  
		Last Modified: Mon, 05 Dec 2022 20:45:29 GMT  
		Size: 4.6 KB (4647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313fd383768c3b7b315dc6a4bd3ae518fde984928cc9919d1f1b60fb0f952156`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979808c2884d0a63b49f0a33ef00f78b1d46f1834d32ecfa755e42d78331ca6c`  
		Last Modified: Mon, 05 Dec 2022 20:45:44 GMT  
		Size: 436.3 MB (436275294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edda9cc942e34b78ec1cfbdd85b84cb86d3954b84b95b1cf75d45c2f8bb39633`  
		Last Modified: Mon, 05 Dec 2022 20:45:28 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-java11`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-java11` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-java8`

```console
$ docker pull flink@sha256:e245fadd7f2adc39e0fec173f3fec9c6f4445d64dde963c752b5e683edeeca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-java8` - linux; amd64

```console
$ docker pull flink@sha256:cb494f82aa946fafbbb09c83ed3dd5ada8876a0a987a309eeb538d0f55d33428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.4 MB (566440282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584a51fe68accab093c89814154aeaf81497ff46d48c4734515ee9282d89c7f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:38:50 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:38:50 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:38:50 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:40:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:40:50 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:40:50 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:40:50 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41a152ba4f15d7f92679875f2553b39089c1a1fadc60cd5cc7645efa9c4d449`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56798772b043b412bbd783ea9ff8670a5d47fe9b4dd668c15fb39152f86176cd`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d00ae1c48679988ea59ee9fc770fbf4e6d1e7fc77205eb312f6ddc9bf8f4a`  
		Last Modified: Sat, 05 Nov 2022 00:49:59 GMT  
		Size: 476.2 MB (476196789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b0ff0f2bc59d9e9d9ed5ed896e3b8d9e04030fa2f8af4c778b2d40f821942`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:af967ec261d229633419e8a378fcb8992c9075020234e68c8d8b2725308189c3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563126840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cef1e0b390a25cf9ef42234665c4b077fa7760b70fb0be8525d46f687ccd37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:15:40 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:15:41 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:15:41 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:17 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:18 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d446e78a891000c185e35bc41587da78732dad21ebaa11a905939c4e607f5`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad795874d3e2e000e7cbf1cf9f7fd088c42a01a72ab6352db6068ab879ddfb`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff45cb461b18fbe0be97c3f15c0f392677ffbdfd7ad96dc5b39da2965f5fc26`  
		Last Modified: Sat, 05 Nov 2022 00:19:03 GMT  
		Size: 476.2 MB (476196786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4bfc02e67d2b67482ed7fa9111e860f653cc66791e50756738b729adcab56`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-scala_2.12`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-scala_2.12-java11`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-scala_2.12-java8`

```console
$ docker pull flink@sha256:e245fadd7f2adc39e0fec173f3fec9c6f4445d64dde963c752b5e683edeeca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:cb494f82aa946fafbbb09c83ed3dd5ada8876a0a987a309eeb538d0f55d33428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.4 MB (566440282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584a51fe68accab093c89814154aeaf81497ff46d48c4734515ee9282d89c7f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:38:50 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:38:50 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:38:50 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:40:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:40:50 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:40:50 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:40:50 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41a152ba4f15d7f92679875f2553b39089c1a1fadc60cd5cc7645efa9c4d449`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56798772b043b412bbd783ea9ff8670a5d47fe9b4dd668c15fb39152f86176cd`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d00ae1c48679988ea59ee9fc770fbf4e6d1e7fc77205eb312f6ddc9bf8f4a`  
		Last Modified: Sat, 05 Nov 2022 00:49:59 GMT  
		Size: 476.2 MB (476196789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b0ff0f2bc59d9e9d9ed5ed896e3b8d9e04030fa2f8af4c778b2d40f821942`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:af967ec261d229633419e8a378fcb8992c9075020234e68c8d8b2725308189c3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563126840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cef1e0b390a25cf9ef42234665c4b077fa7760b70fb0be8525d46f687ccd37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:15:40 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:15:41 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:15:41 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:17 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:18 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d446e78a891000c185e35bc41587da78732dad21ebaa11a905939c4e607f5`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad795874d3e2e000e7cbf1cf9f7fd088c42a01a72ab6352db6068ab879ddfb`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff45cb461b18fbe0be97c3f15c0f392677ffbdfd7ad96dc5b39da2965f5fc26`  
		Last Modified: Sat, 05 Nov 2022 00:19:03 GMT  
		Size: 476.2 MB (476196786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4bfc02e67d2b67482ed7fa9111e860f653cc66791e50756738b729adcab56`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.0`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.0` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.0` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.0-java11`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.0-java11` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.0-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.0-java8`

```console
$ docker pull flink@sha256:e245fadd7f2adc39e0fec173f3fec9c6f4445d64dde963c752b5e683edeeca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.0-java8` - linux; amd64

```console
$ docker pull flink@sha256:cb494f82aa946fafbbb09c83ed3dd5ada8876a0a987a309eeb538d0f55d33428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.4 MB (566440282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584a51fe68accab093c89814154aeaf81497ff46d48c4734515ee9282d89c7f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:38:50 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:38:50 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:38:50 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:40:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:40:50 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:40:50 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:40:50 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41a152ba4f15d7f92679875f2553b39089c1a1fadc60cd5cc7645efa9c4d449`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56798772b043b412bbd783ea9ff8670a5d47fe9b4dd668c15fb39152f86176cd`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d00ae1c48679988ea59ee9fc770fbf4e6d1e7fc77205eb312f6ddc9bf8f4a`  
		Last Modified: Sat, 05 Nov 2022 00:49:59 GMT  
		Size: 476.2 MB (476196789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b0ff0f2bc59d9e9d9ed5ed896e3b8d9e04030fa2f8af4c778b2d40f821942`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.0-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:af967ec261d229633419e8a378fcb8992c9075020234e68c8d8b2725308189c3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563126840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cef1e0b390a25cf9ef42234665c4b077fa7760b70fb0be8525d46f687ccd37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:15:40 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:15:41 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:15:41 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:17 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:18 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d446e78a891000c185e35bc41587da78732dad21ebaa11a905939c4e607f5`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad795874d3e2e000e7cbf1cf9f7fd088c42a01a72ab6352db6068ab879ddfb`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff45cb461b18fbe0be97c3f15c0f392677ffbdfd7ad96dc5b39da2965f5fc26`  
		Last Modified: Sat, 05 Nov 2022 00:19:03 GMT  
		Size: 476.2 MB (476196786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4bfc02e67d2b67482ed7fa9111e860f653cc66791e50756738b729adcab56`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.0-scala_2.12`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.0-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.0-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.0-scala_2.12-java11`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.0-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.0-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.0-scala_2.12-java8`

```console
$ docker pull flink@sha256:e245fadd7f2adc39e0fec173f3fec9c6f4445d64dde963c752b5e683edeeca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.0-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:cb494f82aa946fafbbb09c83ed3dd5ada8876a0a987a309eeb538d0f55d33428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.4 MB (566440282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584a51fe68accab093c89814154aeaf81497ff46d48c4734515ee9282d89c7f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:38:50 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:38:50 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:38:50 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:40:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:40:50 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:40:50 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:40:50 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41a152ba4f15d7f92679875f2553b39089c1a1fadc60cd5cc7645efa9c4d449`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56798772b043b412bbd783ea9ff8670a5d47fe9b4dd668c15fb39152f86176cd`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d00ae1c48679988ea59ee9fc770fbf4e6d1e7fc77205eb312f6ddc9bf8f4a`  
		Last Modified: Sat, 05 Nov 2022 00:49:59 GMT  
		Size: 476.2 MB (476196789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b0ff0f2bc59d9e9d9ed5ed896e3b8d9e04030fa2f8af4c778b2d40f821942`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.0-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:af967ec261d229633419e8a378fcb8992c9075020234e68c8d8b2725308189c3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563126840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cef1e0b390a25cf9ef42234665c4b077fa7760b70fb0be8525d46f687ccd37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:15:40 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:15:41 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:15:41 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:17 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:18 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d446e78a891000c185e35bc41587da78732dad21ebaa11a905939c4e607f5`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad795874d3e2e000e7cbf1cf9f7fd088c42a01a72ab6352db6068ab879ddfb`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff45cb461b18fbe0be97c3f15c0f392677ffbdfd7ad96dc5b39da2965f5fc26`  
		Last Modified: Sat, 05 Nov 2022 00:19:03 GMT  
		Size: 476.2 MB (476196786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4bfc02e67d2b67482ed7fa9111e860f653cc66791e50756738b729adcab56`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:java11`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:java11` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:java8`

```console
$ docker pull flink@sha256:e245fadd7f2adc39e0fec173f3fec9c6f4445d64dde963c752b5e683edeeca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:java8` - linux; amd64

```console
$ docker pull flink@sha256:cb494f82aa946fafbbb09c83ed3dd5ada8876a0a987a309eeb538d0f55d33428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.4 MB (566440282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584a51fe68accab093c89814154aeaf81497ff46d48c4734515ee9282d89c7f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:38:50 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:38:50 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:38:50 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:40:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:40:50 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:40:50 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:40:50 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41a152ba4f15d7f92679875f2553b39089c1a1fadc60cd5cc7645efa9c4d449`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56798772b043b412bbd783ea9ff8670a5d47fe9b4dd668c15fb39152f86176cd`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d00ae1c48679988ea59ee9fc770fbf4e6d1e7fc77205eb312f6ddc9bf8f4a`  
		Last Modified: Sat, 05 Nov 2022 00:49:59 GMT  
		Size: 476.2 MB (476196789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b0ff0f2bc59d9e9d9ed5ed896e3b8d9e04030fa2f8af4c778b2d40f821942`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:af967ec261d229633419e8a378fcb8992c9075020234e68c8d8b2725308189c3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563126840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cef1e0b390a25cf9ef42234665c4b077fa7760b70fb0be8525d46f687ccd37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:15:40 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:15:41 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:15:41 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:17 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:18 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d446e78a891000c185e35bc41587da78732dad21ebaa11a905939c4e607f5`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad795874d3e2e000e7cbf1cf9f7fd088c42a01a72ab6352db6068ab879ddfb`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff45cb461b18fbe0be97c3f15c0f392677ffbdfd7ad96dc5b39da2965f5fc26`  
		Last Modified: Sat, 05 Nov 2022 00:19:03 GMT  
		Size: 476.2 MB (476196786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4bfc02e67d2b67482ed7fa9111e860f653cc66791e50756738b729adcab56`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:latest`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:latest` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:latest` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:scala_2.12`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:scala_2.12-java11`

```console
$ docker pull flink@sha256:c7f02977b3313e1206ae944abe7c4f9b7634983937171912db26ec4ac1d54aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:e3611f667f7afe455ca08185b7749cad9b827ac7a5afe0652534510fa9bbff30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.3 MB (571251618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1b38a1f0ddc57073c0122f702bc67bc91356cafe3a2fe5e9eb8eae0073c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:41:05 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:41:05 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:41:11 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:41:12 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:41:12 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:41:12 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:41:13 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:43:32 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:43:33 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:43:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:43:34 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:43:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8a3af4e53d083f22ab9ead030a66bed328c381dffcc4da6c607f0b496a821`  
		Last Modified: Sat, 05 Nov 2022 00:50:23 GMT  
		Size: 4.7 MB (4652705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258618cb5889d16f438856db8ac365ebb64a863114d17985aa0ff3b3fc545bf`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 900.5 KB (900504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1708179f730002e533accc28eb9c777de30cd998654561080e16bb24cf86fb71`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a971c9ef0d3421eaafff70b62a742ff2d1ef934ad1a80cdb6035a07f8d26da`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a0ddb1ce66152fa6af563c2712ca5c67319a3260b19867edabc63ec818861d`  
		Last Modified: Sat, 05 Nov 2022 00:50:54 GMT  
		Size: 476.2 MB (476196827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9469cce13fae7d9baeac0c57d6ad242d2483feb3c611bc7a95f3d70959596`  
		Last Modified: Sat, 05 Nov 2022 00:50:20 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:42c0e376518bf61082874d3b21587ac0490e295721a87957a2d839f9a58471e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401ce2717809ba264046f0e2adebe5e660bc23e165e38da641a549bc9cdb592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 00:16:27 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:16:27 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:16:33 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:16:33 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:16:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:16:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:16:34 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:59 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:59 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71797e9a724454613155446475d454934b62d1d4327b3bd3bf1247310b155dbc`  
		Last Modified: Sat, 05 Nov 2022 00:19:27 GMT  
		Size: 4.5 MB (4501832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e80ad0c31c2d87b7faa08f0f405e965c48cb3b08d1a6e30a70ea8983001da3`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 835.4 KB (835389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c26d30e25748d1d0fa95f7adf4739227726beaff0b7737b98c0e5f50a4f8ef`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865cd91d484658ab861896a63a0caa87f009f2dc5f23ce50ce6e271db664c8cf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7695b1da38174d8dd873facee571f14e155dd0f2832250c6264b7c7a67e4077d`  
		Last Modified: Sat, 05 Nov 2022 00:19:41 GMT  
		Size: 476.2 MB (476196754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b09606948af754c6804ace6e2948dbe25bfa9df7b14e153ea37aaf1813faf`  
		Last Modified: Sat, 05 Nov 2022 00:19:24 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:scala_2.12-java8`

```console
$ docker pull flink@sha256:e245fadd7f2adc39e0fec173f3fec9c6f4445d64dde963c752b5e683edeeca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:cb494f82aa946fafbbb09c83ed3dd5ada8876a0a987a309eeb538d0f55d33428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.4 MB (566440282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584a51fe68accab093c89814154aeaf81497ff46d48c4734515ee9282d89c7f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:37:42 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:37:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:38:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:38:50 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:38:50 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:38:50 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:38:50 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:40:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:40:50 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:40:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:40:50 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:40:50 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d5c75dce404bfaa3b13c70eb006ae3699324e4a86e400d6974348b9a9083c`  
		Last Modified: Sat, 05 Nov 2022 00:49:41 GMT  
		Size: 4.7 MB (4652680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a6e3261144b846c3f3de360c1993e3244df3503770f6303645d7c3e713534`  
		Last Modified: Sat, 05 Nov 2022 00:49:39 GMT  
		Size: 900.5 KB (900507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41a152ba4f15d7f92679875f2553b39089c1a1fadc60cd5cc7645efa9c4d449`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 4.6 KB (4614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56798772b043b412bbd783ea9ff8670a5d47fe9b4dd668c15fb39152f86176cd`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d00ae1c48679988ea59ee9fc770fbf4e6d1e7fc77205eb312f6ddc9bf8f4a`  
		Last Modified: Sat, 05 Nov 2022 00:49:59 GMT  
		Size: 476.2 MB (476196789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b0ff0f2bc59d9e9d9ed5ed896e3b8d9e04030fa2f8af4c778b2d40f821942`  
		Last Modified: Sat, 05 Nov 2022 00:49:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:af967ec261d229633419e8a378fcb8992c9075020234e68c8d8b2725308189c3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563126840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cef1e0b390a25cf9ef42234665c4b077fa7760b70fb0be8525d46f687ccd37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:15:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:15:30 GMT
ENV GOSU_VERSION=1.11
# Sat, 05 Nov 2022 00:15:40 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.0/flink-1.16.0-bin-scala_2.12.tgz.asc GPG_KEY=EB3FE0FA3282FAF822E434AE3C2C9FFB59DF9F3E CHECK_GPG=true
# Sat, 05 Nov 2022 00:15:40 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 Nov 2022 00:15:40 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:15:41 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 Nov 2022 00:15:41 GMT
WORKDIR /opt/flink
# Sat, 05 Nov 2022 00:16:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Sat, 05 Nov 2022 00:16:17 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Sat, 05 Nov 2022 00:16:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:16:18 GMT
EXPOSE 6123 8081
# Sat, 05 Nov 2022 00:16:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181826e630654af8f0b5740900b059e2cc5b069c04718e168b07701d5e91dfc1`  
		Last Modified: Sat, 05 Nov 2022 00:18:49 GMT  
		Size: 4.5 MB (4501774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f934893b1e21eb3946ba0e5006230d5d37b69b4697058f7528a0ababd45bf2`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 835.4 KB (835387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d446e78a891000c185e35bc41587da78732dad21ebaa11a905939c4e607f5`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad795874d3e2e000e7cbf1cf9f7fd088c42a01a72ab6352db6068ab879ddfb`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff45cb461b18fbe0be97c3f15c0f392677ffbdfd7ad96dc5b39da2965f5fc26`  
		Last Modified: Sat, 05 Nov 2022 00:19:03 GMT  
		Size: 476.2 MB (476196786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4bfc02e67d2b67482ed7fa9111e860f653cc66791e50756738b729adcab56`  
		Last Modified: Sat, 05 Nov 2022 00:18:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
