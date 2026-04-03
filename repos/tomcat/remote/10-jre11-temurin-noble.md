## `tomcat:10-jre11-temurin-noble`

```console
$ docker pull tomcat@sha256:a31432a5f982b14ddfa48f044d74c3ec4f49ae7fb83e99391c14cf356b485b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre11-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:78150fda265709bbcbd3059ab4efb5bdb89e05a045ffc6105874e611f014a639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109963859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c056c416959c6ceb3b39e0803147d78272cf3570702683defc6a908f04559ce`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:22:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:22:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:22:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:22:45 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Mar 2026 01:22:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:22:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:22:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:22:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:12 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:12 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:12 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:11:12 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:11:12 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:11:12 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:20 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6502333748a9e5b5a7e8aaabb484e42b3cc861ca1dcf4d70331259c318eb596d`  
		Last Modified: Tue, 17 Mar 2026 01:23:01 GMT  
		Size: 17.0 MB (16983392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79913738bc1520d769b9074230062a524af97dea8452b5ad1428392983fc5058`  
		Last Modified: Tue, 17 Mar 2026 01:23:00 GMT  
		Size: 47.3 MB (47304998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b140e96e33be479679fcfcffc9574d66c782da4adc0b784a42c251e4068d65c7`  
		Last Modified: Tue, 17 Mar 2026 01:22:59 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5603f533e6e4d1c6ae92835c68651094cc820f111d15e9ffa1df76ca951ad44`  
		Last Modified: Tue, 17 Mar 2026 01:22:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a4aec6683866c58768f644b5322f5dc0d63364754a24b67982aed70678d5d`  
		Last Modified: Fri, 03 Apr 2026 18:11:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6be06cbc7c2e70c91c7ff9d7d2cc012ffb45cddaa8dd5749e4745a6d91641`  
		Last Modified: Fri, 03 Apr 2026 18:11:29 GMT  
		Size: 14.3 MB (14301109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bbfeb6459bb114aa77b93d979c72d3182fbece44e0334d133d795aaffd7f8a`  
		Last Modified: Fri, 03 Apr 2026 18:11:28 GMT  
		Size: 1.6 MB (1639722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:1d940cf2266cfa7bf6b151ae41519231aa1dbfa011fd7581411fecbfb28b91dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3384689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3072e39fb7b23cd0620faddc403232b8186fce799e54e0bc295cafacf6fe163e`

```dockerfile
```

-	Layers:
	-	`sha256:18afa81e59bf6cf151108a70863943fa8488a681925621d63aa4f65526921e3d`  
		Last Modified: Fri, 03 Apr 2026 18:11:28 GMT  
		Size: 3.4 MB (3361578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c0ced3a8f8e4b136c80687fcbbe3177b0e2778e7eac2f9aa435919e8643cb`  
		Last Modified: Fri, 03 Apr 2026 18:11:28 GMT  
		Size: 23.1 KB (23111 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:05e02b054783cec7ecb9e820debacfa6b87d4bb341c643bbd6085755cae8494e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105285441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05734a61523e1286293beab858f4a496896c4a8d67f3a54d7b4683d93e94b8c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:10 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:14 GMT
ADD file:834191023ea63b612bd409fecc858bd572114f2ce02aca5944385eae5eaf48f8 in / 
# Mon, 23 Feb 2026 17:19:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:15:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:15:22 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Mar 2026 01:15:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:10:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:08 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:08 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:08 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:08 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:08 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:08 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:21 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:21 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:51c4cbb22341ed2a12c82974973354e1be3db5c9041bb5fbe2640ced2f41020b`  
		Last Modified: Mon, 23 Feb 2026 17:51:31 GMT  
		Size: 26.9 MB (26859311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865412737d52f4fc93635ce3f2388c5d07a43962d7f65adfa7eeb77e9efb5e6`  
		Last Modified: Tue, 17 Mar 2026 01:15:47 GMT  
		Size: 16.3 MB (16309634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cb28309308ddbafd958ef056069355f97945d7d60d220df574d1bceea1ac69`  
		Last Modified: Tue, 17 Mar 2026 01:16:10 GMT  
		Size: 45.4 MB (45416758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e72a43edbce53332c5fa2835a06234537f0a6703b9c6e2423688a259099d7c`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750c96026dab6a056583410b850783bc99771b87c5b00e6df6318d6bb508bed6`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aa5fb3364b83bd431cd5b4339129bc9da4c89f506cd79ab9db824a32b2ebdb`  
		Last Modified: Fri, 03 Apr 2026 18:10:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c08ebc336e6af9a01d2906fce8885c68b190c6575065a91f9bf518e719baab`  
		Last Modified: Fri, 03 Apr 2026 18:10:30 GMT  
		Size: 14.3 MB (14274654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98a2c58224a3c13e817e3f189735e4cfeefb218be496816adf429645d8b4258`  
		Last Modified: Fri, 03 Apr 2026 18:10:29 GMT  
		Size: 2.4 MB (2422440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:359045e106c27082cb316055a27c04f5b8a09fef553782f7a7eaae4b2ed9f9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511d056ced2f0fa154ea211d9ed1a39d0bb92539b11fb7d31346671eebe3edde`

```dockerfile
```

-	Layers:
	-	`sha256:e092eb3f0ba6341de7d0997d895ea3014b7f0d0b8f7b09a81f8451faff2466c3`  
		Last Modified: Fri, 03 Apr 2026 18:10:29 GMT  
		Size: 3.4 MB (3365221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:562eedffda497e2fdd22f5b75f39f218d629fe622c367515e8097b25121cf4af`  
		Last Modified: Fri, 03 Apr 2026 18:10:29 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3141a3721c2c7411b383467b90442e02a5d3cd8536c4d659b5bffbb5b04d928f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107514556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7898f789c3b606b0b46f16f4acb7b32c9c1fc48279630c8c13dd0322ee2b45`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:24:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:24:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:24:07 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Mar 2026 01:24:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:10:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:54 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:54 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:54 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:54 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:06 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:06 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbde62ca35706489bb512ab9d010ce76c027c00fd8666abb8d76211dbf9a26c`  
		Last Modified: Tue, 17 Mar 2026 01:24:22 GMT  
		Size: 17.0 MB (16996043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f27d8602ee3dfb2cd3e6cc668d2b949a0c2f64528cff0829d3ba757e0ace6e`  
		Last Modified: Tue, 17 Mar 2026 01:24:23 GMT  
		Size: 45.6 MB (45623448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21eb890e1d9b6e38772d8cd2c74401fd9cde1dcb923f44ebe47ea88fa023ae2`  
		Last Modified: Tue, 17 Mar 2026 01:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615e1ab2a4feed9e17a64b3f2352e4d5f5616b4d0648df13d8e0429de39c8b6`  
		Last Modified: Tue, 17 Mar 2026 01:24:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc0cf243be000a5ca375206731f7674bc647d05257c2a01776290f5680f5f0`  
		Last Modified: Fri, 03 Apr 2026 18:11:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25844bd5d0ce405c1b690c0f27751dcbc46553e760e57ad900b48317ee09361b`  
		Last Modified: Fri, 03 Apr 2026 18:11:15 GMT  
		Size: 14.3 MB (14303298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ca8a0bbee0093498046e87a37a88083aac1430cd535b783f9e7d07ebc3104`  
		Last Modified: Fri, 03 Apr 2026 18:11:15 GMT  
		Size: 1.7 MB (1719412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:d098231210e1155fcc6dff598253887ff7709f33356653f1a742d2d36df6a90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3386059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90786290296782401488bce859a9a350de46384cb5514331a3c60a5efacaebd`

```dockerfile
```

-	Layers:
	-	`sha256:169ea5481c78e9a35f1100d287d05cb713426033a87d67e468eb3563fb33ef36`  
		Last Modified: Fri, 03 Apr 2026 18:11:15 GMT  
		Size: 3.4 MB (3362728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bccbce8a7dbf1801c5b0a44736fa34e082560642e04a2aa870e6aa19e1fbd7ea`  
		Last Modified: Fri, 03 Apr 2026 18:11:14 GMT  
		Size: 23.3 KB (23331 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:e1328d9735bbaa7220812361169524c9cb86aab8a66638f5ca660a99881c7be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112175192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c5229073b48db820e0886a3fc4b08e5f8825e68b9b59d9fae853d413586f1f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:29:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:29:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:29:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:29:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:29:49 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Mar 2026 08:32:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:32:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:32:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:32:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:12:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:12:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:12:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:12:32 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:12:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:12:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:12:32 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:12:32 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:12:32 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:12:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:13:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:13:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:13:05 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:13:05 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:13:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c602d6d5b3bff268e7b1f1815099c69255c8fca8953f0d22e169ed8acd2c409c`  
		Last Modified: Tue, 17 Mar 2026 08:30:26 GMT  
		Size: 18.8 MB (18813047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195420f32a2592e3183fca54ef45734254f09b9ac557fd646a841cd6d4d27b32`  
		Last Modified: Tue, 17 Mar 2026 08:32:30 GMT  
		Size: 42.8 MB (42752076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac96aed420c9e7035e5eff3af0bbfc43ce0de8cd302b2d507ee9cb8f940da51`  
		Last Modified: Tue, 17 Mar 2026 08:32:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5550ef78d1dd19036f23a6e1363938873459097b3039dca405af60b069a9f24`  
		Last Modified: Tue, 17 Mar 2026 08:32:28 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb995c5065924e29de4b348a335b1f5e6201c84f89b951fad28aaeb69e31f32`  
		Last Modified: Fri, 03 Apr 2026 18:13:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc9a44665a59c2fbc9596acabb963625cc403eab814c9510faa73d84b388d5c`  
		Last Modified: Fri, 03 Apr 2026 18:13:23 GMT  
		Size: 14.3 MB (14318996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68e662b55e3cba4b26d737b36db7f60a09c23dee6bb06640dc056d321bee4b0`  
		Last Modified: Fri, 03 Apr 2026 18:13:23 GMT  
		Size: 2.0 MB (1978378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:74c8f024b16ec68d2bc12fc36baaf09a39b4e9e4fa2de3d995057328c240f593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46450e7785bfce1fabd8ef3e8823711ac7f5fa6abbb759be83300791ecb2bbdf`

```dockerfile
```

-	Layers:
	-	`sha256:8504f20f2a475458d60a98920de666293fb121da6806b897953706ca8fbdc905`  
		Last Modified: Fri, 03 Apr 2026 18:13:23 GMT  
		Size: 3.4 MB (3365691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785f69bf7b68b5ffbb2cffd0bbe5e9e7b34f97c82488562ba0c3742dfcdfa011`  
		Last Modified: Fri, 03 Apr 2026 18:13:22 GMT  
		Size: 23.2 KB (23199 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:beb9d9ecb8ccb08b67165ff574594e8c46e621ec0ed81d633eb16e5aa4f4c11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104766445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b486de5a66bb0d496287372141cb9d7141f4e771000e8ea2950c70d27b7974c0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:20:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:20:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:56 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Mar 2026 02:20:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 02:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 02:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:09:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:09:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:09:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:09:58 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:09:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:09:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:09:58 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:09:58 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:09:58 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:09:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:03 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:03 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d5075c859e95f7ceeb1369ad2e7b18404db28432307eda800913f597c88e6`  
		Last Modified: Tue, 17 Mar 2026 02:21:18 GMT  
		Size: 17.6 MB (17578847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6359843cda4ba03245f1fcca4c8752bd39814575d5ba5840e3a3c659f95b9f`  
		Last Modified: Tue, 17 Mar 2026 02:21:19 GMT  
		Size: 41.3 MB (41310271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecec1b36b8fb78405a2616258c5289003e256f3fce2dd5d082e31c6423a5094`  
		Last Modified: Tue, 17 Mar 2026 02:21:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebda4fc7bdd2e7e943c6d7562f961161cbf5c1899f62feb15325916d2168a61d`  
		Last Modified: Tue, 17 Mar 2026 02:21:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405589a66a2ae419e1455eed5ad949961473f02afaac65aea5c6597225e0ad1a`  
		Last Modified: Fri, 03 Apr 2026 18:10:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb3266e07e42bcb549d045fa17c312d5e6cb1360c53324964f81d0529cfd896`  
		Last Modified: Fri, 03 Apr 2026 18:10:17 GMT  
		Size: 14.3 MB (14311188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837252740bddabb2a900e1fc44f10df07cc1a3114e8462de5b622f2001677a55`  
		Last Modified: Fri, 03 Apr 2026 18:10:17 GMT  
		Size: 1.7 MB (1653115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:48fb504c629b67502741652c8ebe579a65fd29ee068cb860f47fda0edd6142b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3386894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997649f5d59c9f98aa31c3135ed28dbbf64f9349b139c76ad3436447fb22f53`

```dockerfile
```

-	Layers:
	-	`sha256:90be78ef3eadb4c76abd46243d43bd99857d78dbe2a9fcc5aab2aa9c43163fe0`  
		Last Modified: Fri, 03 Apr 2026 18:10:17 GMT  
		Size: 3.4 MB (3363783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3318f3d2dcb79d22b384f0bba71469e05b02b99ab8c636f614a581dc63c424d`  
		Last Modified: Fri, 03 Apr 2026 18:10:16 GMT  
		Size: 23.1 KB (23111 bytes)  
		MIME: application/vnd.in-toto+json
