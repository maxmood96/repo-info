## `tomcat:9-jre11-temurin-noble`

```console
$ docker pull tomcat@sha256:43c1ebb14d43d67c270fd7ad25e5c05ede65a89972bbef03e0264edecef22953
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

### `tomcat:9-jre11-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:62cdccc2daba5195b593bfae1eb6164378d23bf3d34dfd74ef85488d23eca578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109449088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1131f8d8024ea82460168ff85a0a6a3851eb6cab7cb9e2d43266bf92d8fa7447`
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
# Fri, 03 Apr 2026 18:11:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:32 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:40 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:40 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:40 GMT
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
	-	`sha256:96f5fab9b3212b23e51de0e4995886fabb953387d6e0b02d23a7b5795b3c509f`  
		Last Modified: Fri, 03 Apr 2026 18:11:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17e0ef83899308998bd5a4cc52a3a2e76538436c6a61087dba779f20434329`  
		Last Modified: Fri, 03 Apr 2026 18:11:50 GMT  
		Size: 13.8 MB (13786337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212b8471ee4eecba9802bef9ae4d4bcbbcb0c1cb3acef553c5582e0240aa8450`  
		Last Modified: Fri, 03 Apr 2026 18:11:49 GMT  
		Size: 1.6 MB (1639723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:9950ad63bf0bac6499580c11f1210383a5ecc3d750a1efe92c49c46c4184a1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3381995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838bae13ec2ac92e765243e2c621050899661717a5343b6b247885953a1035a7`

```dockerfile
```

-	Layers:
	-	`sha256:b28dca420fae5f6732e7a3e31038b7573104264e44591188ebcdc79714b2df15`  
		Last Modified: Fri, 03 Apr 2026 18:11:49 GMT  
		Size: 3.4 MB (3358900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b07dd8f098062acf32e0e34c9b0fe45be886bf6a697af66593a0a8f36f7094e`  
		Last Modified: Fri, 03 Apr 2026 18:11:49 GMT  
		Size: 23.1 KB (23095 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:4cabfb4acf1d53e1ae4d40d7860e38bff23ee3e1cf06d59a6e5d592e102b9b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104732891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0443deb6019f58d0108977c1df9142eb49ccdbfd8ee9ec2022238db3ae3f37`
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
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:10:08 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:10:08 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:12:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:12:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:12:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:12:31 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:12:31 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:12:31 GMT
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
	-	`sha256:56ce7082ff34da459d6d5beb6756f6a2d5bbc37db62abb43ba47cff391d25598`  
		Last Modified: Fri, 03 Apr 2026 18:12:39 GMT  
		Size: 13.7 MB (13722083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc067c86a9b32d81ed519538574613132004bbdbda8b652613703e2b349043d1`  
		Last Modified: Fri, 03 Apr 2026 18:12:39 GMT  
		Size: 2.4 MB (2422461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:4224b80260c9547cea07798dde9b244f1697f31510f0823b04d9cf40a32e0b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3385806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdbf51bc070949b9be4d8adafd85611cc25d83d608046d86c846e42d3a9a38d`

```dockerfile
```

-	Layers:
	-	`sha256:a3fa8a95ffa0de6fed001758a0218a2c976ed81964710f48f2d25d2d889d7ca2`  
		Last Modified: Fri, 03 Apr 2026 18:12:38 GMT  
		Size: 3.4 MB (3362543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2fc26054f5f373961df30b142341fbd3ff1cf350bbeaec87e7688f22ffbb38`  
		Last Modified: Fri, 03 Apr 2026 18:12:38 GMT  
		Size: 23.3 KB (23263 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:cf24cc7660aa8cd85706c7e794722fa6e2549b8825759b94bd81fa7e8333cecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (107007827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf25472a0a608ba8274bea359156bb4b7e354636a38f05c65f753510ef764c`
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
# Fri, 03 Apr 2026 18:11:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:11 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:11 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:22 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:22 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:22 GMT
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
	-	`sha256:7792ac1033352129c65dd1b73f5c492874ffd90deddf2cf40e60ba8963ae310a`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71706aeec248f1cd03b0343df3753a790479d95ba22b764dada9d86bb276b3d4`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 13.8 MB (13796569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3591af5eba16e8d11292be80d8832b81a48033f7bc1a2e59a30db9862b72c77`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 1.7 MB (1719412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:f3e0e9e6999b16ccae4352cec8d31b0c47026cf2ffa9fac9b3e6caf4940dd317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3383365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a436600186ddafee966a28de45d139f413b2d3a3406da2ec21d8dedcc19f39bb`

```dockerfile
```

-	Layers:
	-	`sha256:f5d4135267985e71752b812881ec200aad052fe690a228bd885dac5c5b18ce15`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 3.4 MB (3360050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8e902d0a09b4b3672d3f190d64381f7e189965ab0be6d131e392b789e0610a`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 23.3 KB (23315 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:02a1e48f732c6d062068031576167276045c94c864bb38b90649da2774db2eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111679958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c797f64908a8307f769ad7d653532c2138652f4142df41e3fcaf78a70494fe8`
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
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:12:32 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:12:32 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:16:30 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:16:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:16:43 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:16:43 GMT
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
	-	`sha256:3e1603c5d78c14ea7ee06e15b85ec4fb821241263ae75b12005baf1235916706`  
		Last Modified: Fri, 03 Apr 2026 18:17:03 GMT  
		Size: 13.8 MB (13823784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8abab31930cf5eacaffa6a2339a62460ae0c32f2184a82def6ff6ca7b7367a0`  
		Last Modified: Fri, 03 Apr 2026 18:17:03 GMT  
		Size: 2.0 MB (1978356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:4b9de0dd4acaa60474b9d16152a6979637451ae50d19a9db8b9b13176d8d9901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3386196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba546526154a5c08c29d0d48c771252ba0e8767af22b705ac81adbb5fea147a`

```dockerfile
```

-	Layers:
	-	`sha256:1aac0c431811c30c0a07913593598d9b0291929e49faccdaac90cc33ee64d1bc`  
		Last Modified: Fri, 03 Apr 2026 18:17:03 GMT  
		Size: 3.4 MB (3363013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79408d096149e9890f748db276a4f5f3b5ffde19dd371d18bacdc52f241ad713`  
		Last Modified: Fri, 03 Apr 2026 18:17:02 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:9734b8138a95f5922d3c3f5c0733e2324fe0dad6597f00449475769a5f9f9e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104251845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992044b9d202bbfef1e7ea20c7f219447f191c179952df0ec478a5a51f352e17`
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
# Fri, 03 Apr 2026 18:11:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:04 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:04 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:04 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:04 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:04 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:09 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:09 GMT
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
	-	`sha256:bdb46840f15412914e8b61ee94286561666205261c8fa7d53d576ef72499864f`  
		Last Modified: Fri, 03 Apr 2026 18:11:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce49122b3ae7e68389a61f113c802d97b8e9ea3e61b1dbdc96d84b086e4781c0`  
		Last Modified: Fri, 03 Apr 2026 18:11:22 GMT  
		Size: 13.8 MB (13796424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5a0ef7705bc167f29ec1290d7f2e453cd8551745f6c2a06164bdd56de923a2`  
		Last Modified: Fri, 03 Apr 2026 18:11:22 GMT  
		Size: 1.7 MB (1653279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:e0ce89c21583366e7c95f579990f81b3b15c907f4dd64aca6f551fc69b4a369a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3384200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0932d99aa4203221f6e9318ea7fb1b2c9422ed4f694652dd08ed571733f811`

```dockerfile
```

-	Layers:
	-	`sha256:62d8463141dc49d15cde769435fcdeb1406f19824c534dc1b0202502abe5e885`  
		Last Modified: Fri, 03 Apr 2026 18:11:21 GMT  
		Size: 3.4 MB (3361105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376aa58ea28f20d65fcd3a45a80b619dbc476d0b8ecb28c556fed7b468137b2c`  
		Last Modified: Fri, 03 Apr 2026 18:11:22 GMT  
		Size: 23.1 KB (23095 bytes)  
		MIME: application/vnd.in-toto+json
