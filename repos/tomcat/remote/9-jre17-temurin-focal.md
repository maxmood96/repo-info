## `tomcat:9-jre17-temurin-focal`

```console
$ docker pull tomcat@sha256:1f8b84588f1e9e49685061a16f222187530ece149d3094d5614bbe49b1243f13
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

### `tomcat:9-jre17-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:aab20290d7781421e6299e4ba664e69712b31c536914a92e56544ac7192d8b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105489737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf8cef242af7d2d80aa74d97daf62a2ac4cb9a1fafa82fcbbdeea3331061169`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3630fc0cbd45fa0f80b9d434d6267894dff370a431e607d5d88715f6f34b248`  
		Last Modified: Wed, 05 Jun 2024 05:01:07 GMT  
		Size: 47.3 MB (47257501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50b3e479a06b6f065e082c6bae5655399f91386e5e182da500cfd4465a69cc4`  
		Last Modified: Wed, 05 Jun 2024 05:00:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c991c061285997b311c858ccf96137389597ab2f80353f60bc9a8bcc7210f`  
		Last Modified: Wed, 05 Jun 2024 05:00:58 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e712c6877a61a1ccf0046981a913833da7b01dcedb79357a21f94d45ab2e7c37`  
		Last Modified: Fri, 28 Jun 2024 21:59:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c674913298378336017f25b88fd6d5f7fe41d443ada162e11437dca112d1fce`  
		Last Modified: Fri, 28 Jun 2024 21:59:50 GMT  
		Size: 12.5 MB (12514163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0618bd336922647249cf83271229f1ac1694b214bda53a2ff1964a904278e7b5`  
		Last Modified: Fri, 28 Jun 2024 21:59:49 GMT  
		Size: 212.0 KB (211978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-focal` - unknown; unknown

```console
$ docker pull tomcat@sha256:cb6773575422b3b58aca3fa5b879d02064d1e47514b4b15e6d5c35b68505c31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93b7fda99bb04faca195811226e947764f6d3ddba007840706bc8073206be71`

```dockerfile
```

-	Layers:
	-	`sha256:1cdd816aa5eb5614017a98cb7b921f7e25d3cdc4a25820591496cb8ac10f654e`  
		Last Modified: Fri, 28 Jun 2024 21:59:49 GMT  
		Size: 3.5 MB (3499972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199ba85d43af9e8696c08c74507120c038a5434967df6cf25783624ef7663696`  
		Last Modified: Fri, 28 Jun 2024 21:59:49 GMT  
		Size: 21.9 KB (21868 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:7e8585f71cb3eb84fd317ada56424aadd3e15fbbc2755d74ca8a054ac85e0c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97843931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb715efe54b0d51c00ac184ac0114723f9de39437ccd3147330b6d2e9b2c3fe`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd806615dd9e79fe2050b42062de2990cd11200b6ffc1fa232a301bdbba22f2`  
		Last Modified: Wed, 05 Jun 2024 03:59:31 GMT  
		Size: 15.7 MB (15665820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d5442271d15b0f27e867039d815365b9d3f6159f04e466fbf34133fe722f83`  
		Last Modified: Wed, 05 Jun 2024 04:02:40 GMT  
		Size: 44.9 MB (44917829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa996cf00762d2e72db39e862124d9ea71f6527607751cf12bf077ed7fb4e79`  
		Last Modified: Wed, 05 Jun 2024 04:02:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeee1dc3fc629d3a67d99ac1ae73e8a752335b340653d60524105d4fc59dc566`  
		Last Modified: Wed, 05 Jun 2024 04:02:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c8ac5c80e28d524fd2c388a1062929b5b3cebb6cb30953f88452ae7023a32b`  
		Last Modified: Fri, 28 Jun 2024 22:03:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b402401475cbf71184dd07ed34d096dbe6b914b77a185f1ce4a33d14ab95749f`  
		Last Modified: Fri, 28 Jun 2024 22:03:42 GMT  
		Size: 12.5 MB (12466707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc38b0dd24aed34be732329b8d246c27918be8d816df5ec522916dc4e4eb41`  
		Last Modified: Fri, 28 Jun 2024 22:03:42 GMT  
		Size: 188.7 KB (188659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-focal` - unknown; unknown

```console
$ docker pull tomcat@sha256:162e33ec5c08824575d0946bb4a676a004d4e0d1db02e84bf382d89213fca651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3523293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f789246cc442151750b68148ef3f8c448a0dce8ccd9ed47315fb9e2b9ab1534b`

```dockerfile
```

-	Layers:
	-	`sha256:f0bb215a79817af51de200c9a41fd06974b0408d8b9efe6bde7fb093eab1ca67`  
		Last Modified: Fri, 28 Jun 2024 22:03:41 GMT  
		Size: 3.5 MB (3501291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ee40fd5f08e3ea1ccb40d543a18fb39621f437194d0d88ea985ab5b0be52f6`  
		Last Modified: Fri, 28 Jun 2024 22:03:40 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:878e7ac7945ce20ec6184698af9242dab1377943eae96e378c6d345823280390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103444358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a64c806bbf7fff6502cdfc75c8cef3e1ea620f4838548f33695fdb2a063a0e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9da89d621d5589a1bf916269effba35507f61db2bdf22036c2310a6753d80c`  
		Last Modified: Wed, 05 Jun 2024 04:57:30 GMT  
		Size: 46.7 MB (46715355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62da6711f3da89b998c50fdb5d517a581ec33123d634981be5ae117e0f6aaa4`  
		Last Modified: Wed, 05 Jun 2024 04:57:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f030b548337d3dc0699cc1f263412b41324dc0b536fe7b05c3132a45bcb7a61`  
		Last Modified: Wed, 05 Jun 2024 04:57:25 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e530c8814fbc70dd62f47c5b5e3698dd8405baea617788d4003ad659cc54f19`  
		Last Modified: Fri, 28 Jun 2024 22:02:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae3cd65d7beffe16ba59aa0b02887b3a28797635c7531723828f95074015857`  
		Last Modified: Fri, 28 Jun 2024 22:02:17 GMT  
		Size: 12.5 MB (12533953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c607aa73bec40d66c5d63e7f836e6a66ff972a1947d7f689bb28f6f5d3ab44`  
		Last Modified: Fri, 28 Jun 2024 22:02:16 GMT  
		Size: 211.7 KB (211728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-focal` - unknown; unknown

```console
$ docker pull tomcat@sha256:8a47cf206334ad22645a3258f59f0abf0e1ef146e9a82bd05a701320c964d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7bb9b91b5840f836bc1213e47b5dfe19d05ffecb44a13b9c9ab13aa9294e19`

```dockerfile
```

-	Layers:
	-	`sha256:6ec0666375280ab25c6d4361576dfee71891764ba23a6ab0053bd914fdbe6699`  
		Last Modified: Fri, 28 Jun 2024 22:02:17 GMT  
		Size: 3.5 MB (3500233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb05cc813c864b842ac227c39c85c799890b54d3f5fb5f4cc0999955b0cac5f`  
		Last Modified: Fri, 28 Jun 2024 22:02:16 GMT  
		Size: 22.5 KB (22519 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:617bba2215110e2f8e222945f8f52e52ac5be9129c175f729a16bcdda8d46dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111422533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f5da73d2a1b6c8e1b1da983645b027a5c7e00c4e20947c361401597939163c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81db69d14bb46f0b6f105f1f4e966a454cfad03453bf41c1c8b72dbaea27602`  
		Last Modified: Wed, 05 Jun 2024 04:03:18 GMT  
		Size: 47.1 MB (47089429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe58f434b7dd6258c10909b4c9a1a90af7bb1d9a077b1632c935744c07adede`  
		Last Modified: Wed, 05 Jun 2024 04:03:11 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f53fd634e60de994e3f23e07634b360cf52d0c91ad954ab9e97f871402a8cc`  
		Last Modified: Wed, 05 Jun 2024 04:03:11 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f36c1e03241527d6df177d43e3808180266c47ad0fd450b77ae2eed262cab6`  
		Last Modified: Fri, 28 Jun 2024 22:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b713f492652175b1f7c28f138c313cd0d07b948b05b98488b29e659a5e911a`  
		Last Modified: Fri, 28 Jun 2024 22:05:15 GMT  
		Size: 12.6 MB (12556143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f8816a7704aad10d7e813d0fd9087f5e3830641a652a0868ddf32452c3aa28`  
		Last Modified: Fri, 28 Jun 2024 22:05:14 GMT  
		Size: 237.7 KB (237716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-focal` - unknown; unknown

```console
$ docker pull tomcat@sha256:63d568ba10eb8e703e39049cb8e39470f7d0879e7161b22808bf80055d27d60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3526368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85844aa6bf22914385075c90739c3c3615e3f04455363a38dc705f71b34abb5b`

```dockerfile
```

-	Layers:
	-	`sha256:c7f27c8c329b849c22b9bb3e8f6888fdbbbd429228aa01024e3336f3ba9b662c`  
		Last Modified: Fri, 28 Jun 2024 22:05:13 GMT  
		Size: 3.5 MB (3504432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a417998c83d475cfcf040e1a61f274b3d27ce77dd9b2231fe2b8fa05831f5256`  
		Last Modified: Fri, 28 Jun 2024 22:05:13 GMT  
		Size: 21.9 KB (21936 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:7b3120d2cbc661e29c919a80462dba62f2bce8bdc5f7b1a378e5dccbc5274db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100232857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571db2dfa46c25d04ab18c59515d2fd04380880969b0d4ce71fd4cabc284a1aa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4890a1ef55966f920cf0990695cbf55df73dbb89a813469692a9818846fe0b3`  
		Last Modified: Wed, 05 Jun 2024 03:14:03 GMT  
		Size: 43.8 MB (43831397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe3771df01fb841c532cdae48b8088e8847565eee4b79d136a2de41d566a104`  
		Last Modified: Wed, 05 Jun 2024 03:13:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77339174614c64c1518e5f183a14fe51637dc8b704995724a3d375b230c6083d`  
		Last Modified: Wed, 05 Jun 2024 03:13:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5a98b954b9db087f3b7d59f0347fb0ff7806d02a993d6a00b0351957e997c`  
		Last Modified: Fri, 28 Jun 2024 22:03:59 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ec89251ec078a2547681ef0fc72f291ed88da42a1b526b1a1694955eaa32b4`  
		Last Modified: Fri, 28 Jun 2024 22:04:00 GMT  
		Size: 12.5 MB (12527797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86702e3db9d3fc1cc2f1299ffb3780fb84f512030cfba29ba7a6a1f8d6764f85`  
		Last Modified: Fri, 28 Jun 2024 22:04:00 GMT  
		Size: 213.7 KB (213690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-focal` - unknown; unknown

```console
$ docker pull tomcat@sha256:17de3d26510db225dedaf837adb210ee8d1551e27bece71e2b6710d10664cf83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceb20a6e22ae39ec7d796426815419c7123c3c03830123b753be88617377a87`

```dockerfile
```

-	Layers:
	-	`sha256:c1b2d62133a81932f17d17e4f271f10973cbcfce3fb6b4c4e936eff19dbff35a`  
		Last Modified: Fri, 28 Jun 2024 22:03:59 GMT  
		Size: 3.5 MB (3500436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca8109d4bca75389d9695d3df63487767c2450cab98746559cc3a927e806215`  
		Last Modified: Fri, 28 Jun 2024 22:03:59 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json
