## `clojure:temurin-22-lein-jammy`

```console
$ docker pull clojure@sha256:d293cf2270fdc142b875819c791fb6f28b18bea34cdf9678504803c5803129b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:e5e3fd73b33aebb4066f3868d866b38cf3ed82d414c6845f9aa729a98c9feea1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222354000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b1e265480e00561b98728b148b3fb4c262cb8152e8a687b816599ead9d9ec2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Wed, 24 Apr 2024 21:35:14 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:35:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:35:14 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:35:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:35:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:35:31 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:35:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:35:34 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:35:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:35:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31e36bca11a3dc3a0c7d2e5d4656928537deb0d7cec7e4e4eb08d9d17b75dab`  
		Last Modified: Tue, 16 Apr 2024 04:07:50 GMT  
		Size: 16.3 MB (16337609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b9f1fa8bcf0d68f947e97661090e95c2c415ad20d3a9e2e79f042a754de0a4`  
		Last Modified: Wed, 24 Apr 2024 19:18:37 GMT  
		Size: 156.7 MB (156718125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5affb9e2ba3f1d576c3e8c285a4164f3603dbacd4b8df539da41602f360e68b`  
		Last Modified: Wed, 24 Apr 2024 19:18:24 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea31b3da51f302b7667893ae645797f78c4d70e1e8cc56b83eae6cce61178fc`  
		Last Modified: Wed, 24 Apr 2024 19:18:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a46be642dde7678b065faefe5d819a664a2fd53df39d7e64a5ee8901ce0ac0`  
		Last Modified: Wed, 24 Apr 2024 21:57:07 GMT  
		Size: 14.5 MB (14458065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4eafb01e0c52d36dd94fb15e61eff113ea556614560afab085b7af918b098`  
		Last Modified: Wed, 24 Apr 2024 21:57:07 GMT  
		Size: 4.4 MB (4399140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25493a97a48fa8197a28777dcf7ed7afb1f314224220ca995888bb45e0addfc1`  
		Last Modified: Wed, 24 Apr 2024 21:57:06 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-lein-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23fec8bdb851d745e70d0d83d0be95c655eb93993b2dafeb1f1484b68772c4b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219751347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44627b093cb619e4ffda4fd5d01f759c12b182022e2e8b1ba67ffb3454458411`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Wed, 24 Apr 2024 19:17:39 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:17:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:17:39 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:17:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:17:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:17:53 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:17:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:17:55 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:17:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:17:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ed6356befcb3f3e3f2dbe4ed0457e6f2e017191ad3f4f999da71660803fb42`  
		Last Modified: Tue, 16 Apr 2024 02:59:21 GMT  
		Size: 17.8 MB (17753415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c7c00a6bbbd321cd9413d399416da05e45fa855c65dda044f0318e737051`  
		Last Modified: Wed, 24 Apr 2024 18:02:41 GMT  
		Size: 154.7 MB (154738542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56297c614df7362f973f0fbdef0f15e85cfe0657d2464b2542d763ed698fae1`  
		Last Modified: Wed, 24 Apr 2024 18:02:32 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1830e08259efadc1579b8211eb357982609b98bfea278a366e25b7e4b1dacf7`  
		Last Modified: Wed, 24 Apr 2024 18:02:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c7a8ceec0f50499ae3b24f053527fa92ef95cd4b64e373c946e36e94629a9`  
		Last Modified: Wed, 24 Apr 2024 19:36:18 GMT  
		Size: 14.5 MB (14458630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bd411632e23914b857065e786126536b90b045a5f20bd332ed5ecf7cc5d665`  
		Last Modified: Wed, 24 Apr 2024 19:36:17 GMT  
		Size: 4.4 MB (4399183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e931f768b219067591d266b4d450b8e4acb6342e920487f623a621e6c36812a9`  
		Last Modified: Wed, 24 Apr 2024 19:36:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
