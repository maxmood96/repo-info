## `clojure:temurin-17-focal`

```console
$ docker pull clojure@sha256:73491de4856eef386142ca73052b0a95aa7f4d527c68f3ba7eace5d2f4322c18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-focal` - linux; amd64

```console
$ docker pull clojure@sha256:bb570a9db4edde8a55159a1537c6b69c8f4213c4ed9f0278feb03d003baa15fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254421097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4949c310d06dbc88f1c08017d13fbd40c9ab87ad6c2e0e724938ba1183704bec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a561288a64ce04c955cc2a899047873e9859e9750d9b10ca9fef14fd39c7333`  
		Last Modified: Thu, 02 May 2024 01:17:47 GMT  
		Size: 20.7 MB (20672110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bef26252a16bb42ac04415cbc6e61961698aefb6ff84300b0f59e4a0cb1969f`  
		Last Modified: Thu, 02 May 2024 01:17:56 GMT  
		Size: 145.1 MB (145102851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d4271e3e0ec1020bbb6707004968ed42f985445aabe248cd1e9144881ee37e`  
		Last Modified: Thu, 02 May 2024 01:17:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54303d91da2f1dce9bea715a3782e60576a9e02e5151cf7451e22de0324dd7a2`  
		Last Modified: Thu, 02 May 2024 01:17:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a52bbcfabb2116451f5bb99ca04f812d66ab7e21fd913fa8202805b9060ad0`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 60.1 MB (60059861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c9cc2b653e62bc866dce74afe4f5472323d8197886dd783a6120d139281278`  
		Last Modified: Wed, 29 May 2024 19:57:11 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f29271f2a9d97fac39196b91cbc02ae313778924fd10d90ee106e60a202763f`  
		Last Modified: Wed, 29 May 2024 19:57:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-focal` - unknown; unknown

```console
$ docker pull clojure@sha256:c250df439b0ff5ccfa6e6550c3fda6e8ecac5959f6ad29dd4963048d07c95412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8178f0d4fa180ab8e0811dd07ee378169063621cd02c2167395ed667b6a391`

```dockerfile
```

-	Layers:
	-	`sha256:e9633c70c52dbf89f913ddf59b3c5aa5f37a465e6384bc0000f026c174c3204e`  
		Last Modified: Wed, 29 May 2024 19:57:11 GMT  
		Size: 5.8 MB (5842497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249eab1f3edd825f23133b1f817155767e176baf34eb25a1c8f6c4c4ab6d6879`  
		Last Modified: Wed, 29 May 2024 19:57:11 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9a7843c3e7cf7c127bd336860e1122527173f7095b9d662c4b1a2de60a43c3f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252944174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea89fc254db24ce14b1880db83c989559291081e3003f740bfc445b4481e1eea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 19:58:02 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:58:02 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:58:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 28 May 2024 19:58:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:58:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:58:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:58:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea79202db79da3bd9ee6809f42ca3ba5eee228dfcbe1a0b240b898b3a991a63`  
		Last Modified: Thu, 02 May 2024 04:19:26 GMT  
		Size: 21.4 MB (21375620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f17299686fe3d852e8e484fabdfbd4565233be6f8e2a876e00afae3eda5f06`  
		Last Modified: Thu, 02 May 2024 04:19:32 GMT  
		Size: 143.9 MB (143897010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5272442066df5d8cbbf4ff6e100f3871fd7eba368467d4a38215ab1ca39ed4d8`  
		Last Modified: Thu, 02 May 2024 04:19:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d769917d6209b484682591b021afab8ef9f901252031daf0e696ab86534a0c`  
		Last Modified: Thu, 02 May 2024 04:19:23 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bea6289e0de9c73ce551c4727c7136962b78755371a9ba1f69cce2182173ef`  
		Last Modified: Tue, 28 May 2024 20:17:27 GMT  
		Size: 60.5 MB (60463463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cdd8e6dfee930516a09896e5d29d49509bd9a7dee3c92f3e2c6076b80d472`  
		Last Modified: Tue, 28 May 2024 20:17:20 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1ecae4cdcd747ffc6d63da51eceea92b42d37f59e6552f8071c8dc8a493f6e`  
		Last Modified: Tue, 28 May 2024 20:17:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
