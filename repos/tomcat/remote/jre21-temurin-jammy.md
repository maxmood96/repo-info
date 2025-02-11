## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:1abd82058f8781b99bbf6e2489a910e8fefc8f417d3b9554b92df2fffe4376bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:b4c707e2aa05aeb9585ec98244bdc242cb42128424bfa8d823d05db9433301e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112595684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63456c15fbcbedc8db4df68fd31118442ad8c546dd6725e4e71cab29427e6b7c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Feb 2025 15:16:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 15:16:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_MAJOR=11
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_VERSION=11.0.3
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_SHA512=860701b16fcf0ab4674ff8c0a61f79b6427bb8bfc44a88f9251fe39f179f2912341f9621b97e38f31959b27ac3efff9e845b49017d954243bca00e23ea965114
# Mon, 10 Feb 2025 15:16:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Feb 2025 15:16:00 GMT
ENTRYPOINT []
# Mon, 10 Feb 2025 15:16:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b8e353effdf25ad74bbde76a3242135d6d12fe14be177b7108868c3150b48`  
		Last Modified: Tue, 04 Feb 2025 04:40:12 GMT  
		Size: 16.1 MB (16135187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379395aa081f5fd7e867ea654d17431258dab5353139b32bc5fa9c09edb8c19a`  
		Last Modified: Tue, 04 Feb 2025 04:40:12 GMT  
		Size: 52.9 MB (52876031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e1b6de86675cf06530c6496ec8374d300561fc2cdacf984c524349c6062ae`  
		Last Modified: Tue, 04 Feb 2025 04:40:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea28f6f7f0aa0864f252fa90ca3f85687428d91dd6f829f2ba81dc8719e2e3be`  
		Last Modified: Tue, 04 Feb 2025 04:40:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4366b15344693300422b144788173ce7b7551c12c1ea13d284c2790d7b5cff84`  
		Last Modified: Tue, 11 Feb 2025 01:27:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12a96e6d7dc61df7dc012d9a52cf333aaee63ac0391cbbd9bb47cb16cfe5303`  
		Last Modified: Tue, 11 Feb 2025 01:27:36 GMT  
		Size: 13.8 MB (13816280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd6d1b0a7a658c4f8b066b48645da3d798ea35b0c1fb4fc0704b28142d674cd`  
		Last Modified: Tue, 11 Feb 2025 01:27:35 GMT  
		Size: 229.6 KB (229601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:23fe652b1a0fc7edb26fb35e02d3d3f358bb3c9a93bc51a71502eb701d96b44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9f709532733f7eb3561531663a6ce1076be8c2725260db2d41212ca874bd3d`

```dockerfile
```

-	Layers:
	-	`sha256:5d7a8df5bc80b79c069c60e1856b805f851bf17b165944f48f65b0cfafe87a23`  
		Last Modified: Tue, 11 Feb 2025 01:27:35 GMT  
		Size: 3.8 MB (3769662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e9f07cd25e26f4806b747d41bd4bb2ef7fe7f7ad7b45114bf83287fcbb7b524`  
		Last Modified: Tue, 11 Feb 2025 01:27:35 GMT  
		Size: 21.6 KB (21580 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:353fb56b000dd03f9a17677b7ab46648f6799e9b591bbecac1dad6c35d963ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109519643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586fa0e754f4729c11c1020239a23901a8e9bc6d5d44d4e18afc41afb6b7d71`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Feb 2025 15:16:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 15:16:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_MAJOR=11
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_VERSION=11.0.3
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_SHA512=860701b16fcf0ab4674ff8c0a61f79b6427bb8bfc44a88f9251fe39f179f2912341f9621b97e38f31959b27ac3efff9e845b49017d954243bca00e23ea965114
# Mon, 10 Feb 2025 15:16:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Feb 2025 15:16:00 GMT
ENTRYPOINT []
# Mon, 10 Feb 2025 15:16:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95725c2df89972119cbe127fa685617010a1c1e038ad8fa77f3a2ce55dced587`  
		Last Modified: Tue, 04 Feb 2025 09:25:22 GMT  
		Size: 52.1 MB (52058393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385b34446c3df21cb4021820b3d3adc4a6c71cdc68b1c961bff59a69117811`  
		Last Modified: Tue, 04 Feb 2025 09:25:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f159f3116700a25149bc46b10b2c56185ebc43fe2b614133fd8a0c0bb25dc991`  
		Last Modified: Tue, 04 Feb 2025 09:25:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704c1e31335e7df2a47128e42aa39c716845023a40968ef71791dc0ed027925d`  
		Last Modified: Wed, 05 Feb 2025 04:43:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1ab3429777542a2d301fbb7a52aa8071f43037226928aaeb632623b3f6ca4b`  
		Last Modified: Tue, 11 Feb 2025 01:28:40 GMT  
		Size: 13.8 MB (13819232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129b16bcb2b4f528aaa35dec4c5cfbb1f2f055ea2f7ff1d90526b914bf119981`  
		Last Modified: Tue, 11 Feb 2025 01:28:39 GMT  
		Size: 228.5 KB (228547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:a0a89f40b513502b85139f70206347551c18c403a7d664ff16716323ed5a5c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb68da804c501ca66981c1a61636991171e766a673b540dcd15128550f3a8206`

```dockerfile
```

-	Layers:
	-	`sha256:905013a13cf43b607cee463577a613d65a9ada7fc304092c0430a94bb67f5ffa`  
		Last Modified: Tue, 11 Feb 2025 01:28:39 GMT  
		Size: 3.8 MB (3769343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652def8230a7a992930d457635a6ca1aa6317f5f97a138d3c61de4556c68dc42`  
		Last Modified: Tue, 11 Feb 2025 01:28:38 GMT  
		Size: 21.7 KB (21739 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:7b28eeb34360dc26deb09c3897f3b42779347542be9efb018dc73e9afc81e972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119098795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fab9c4711fdf6004f8e6c2643fb01da98f91320e8e06210efb0dc1b815ca84`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Feb 2025 15:16:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 15:16:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_MAJOR=11
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_VERSION=11.0.3
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_SHA512=860701b16fcf0ab4674ff8c0a61f79b6427bb8bfc44a88f9251fe39f179f2912341f9621b97e38f31959b27ac3efff9e845b49017d954243bca00e23ea965114
# Mon, 10 Feb 2025 15:16:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Feb 2025 15:16:00 GMT
ENTRYPOINT []
# Mon, 10 Feb 2025 15:16:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71de2d980599cbec4dab5c3bd7274078312e68d7cc81171b5d8bda1a98eb2403`  
		Last Modified: Tue, 04 Feb 2025 07:32:10 GMT  
		Size: 17.6 MB (17642335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435fcf10bf81a5ef917029ead19e990e3ff0a4e193038999c648c2631097a48f`  
		Last Modified: Tue, 04 Feb 2025 07:48:19 GMT  
		Size: 52.9 MB (52915069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1afa04b461e33531c028ee10c388148ef95888eaebb52afd7f162cd48d1fff9`  
		Last Modified: Tue, 04 Feb 2025 07:48:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab258ea4c329b5efa03c3fcdd7e6b3f7af187288f825972811b81ea22d0c00bf`  
		Last Modified: Tue, 04 Feb 2025 07:48:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64302daee7499cb7c77b7e9f850ed3835233394c2a2e7cf27e4c5e9aa25f5af7`  
		Last Modified: Tue, 04 Feb 2025 23:10:16 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abbe313a83ee95320dc4079eb2940d692cc7170575ed7161c95d5d8b8bef5a5`  
		Last Modified: Tue, 11 Feb 2025 04:59:31 GMT  
		Size: 13.8 MB (13831863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b9a4c757bfe0d0441071647c5ac0ef8939f7228b2ed23efa4c85e4aef1650`  
		Last Modified: Tue, 11 Feb 2025 04:59:31 GMT  
		Size: 258.9 KB (258948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:a82e5415da00a6a7b883f54189b5c7ad447cd3220973a8de78d69e2f49db74fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b135f7fc93c69ff99fd9e52388bb8ba9d147a62aa35f97369f7920307b6d4b88`

```dockerfile
```

-	Layers:
	-	`sha256:02c7f9e651f3568927ef064ecc0d21f5e854961ba748bd54580758a3fc66866b`  
		Last Modified: Tue, 11 Feb 2025 04:59:31 GMT  
		Size: 3.8 MB (3773604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dbf1e48bf04ab578ae95c8134009995144a8df498505125a9fb0f25e505d2c0`  
		Last Modified: Tue, 11 Feb 2025 04:59:30 GMT  
		Size: 21.6 KB (21638 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:5bb1481e24dea71db68a23b3aef5f38ef9df318e55f75aad1cf8cd887b69adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107651248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4c1892a0adc6c58b1f3921319cd533fe2dd76006af595fec0ccda73ed39937`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Feb 2025 15:16:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 15:16:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_MAJOR=11
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_VERSION=11.0.3
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_SHA512=860701b16fcf0ab4674ff8c0a61f79b6427bb8bfc44a88f9251fe39f179f2912341f9621b97e38f31959b27ac3efff9e845b49017d954243bca00e23ea965114
# Mon, 10 Feb 2025 15:16:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Feb 2025 15:16:00 GMT
ENTRYPOINT []
# Mon, 10 Feb 2025 15:16:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c64c26afd0885ce3d2d456d35ff90e813c65ee4e2f59dd40604fa8b3e90414`  
		Last Modified: Tue, 04 Feb 2025 07:39:56 GMT  
		Size: 16.1 MB (16132604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e748dfd1fa969b853ba3697791f039af4c55a839a5c50e477217176265f1b`  
		Last Modified: Tue, 04 Feb 2025 07:51:22 GMT  
		Size: 49.5 MB (49462943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653884e7c258812fac56cda1ca97c1deafd240ac6d359765356d52bae405c045`  
		Last Modified: Tue, 04 Feb 2025 07:51:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b2b89b98ed384dea007d5383048dcbd69e1889f47389b95507238f8cc2014`  
		Last Modified: Tue, 04 Feb 2025 07:51:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1382cf59890b152f778818b5453406d3b13d148dcffeccb22e855a182252d3f5`  
		Last Modified: Wed, 05 Feb 2025 05:56:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f7dafa7c49bd85ef1446d198e26891964495c0fde8dae0624a5cb71098b00`  
		Last Modified: Tue, 11 Feb 2025 01:46:35 GMT  
		Size: 13.8 MB (13821404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff8a08807cb1d83aa300fc4303d6c67a72fcc2d4992e87bee62f587c44ff376`  
		Last Modified: Tue, 11 Feb 2025 01:46:35 GMT  
		Size: 230.7 KB (230723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:20902168559ab220821d5c183be3010536e12ef7e59fa579140a218efcf060bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bb381b176a7d1e34679b706a2f66e924245da4f29c12fda4c72f8b68f2570e`

```dockerfile
```

-	Layers:
	-	`sha256:291d5403986af7728c00d9189850fc2f0c5ef508b23dc8ec9a77e324b086bfe3`  
		Last Modified: Tue, 11 Feb 2025 01:46:34 GMT  
		Size: 3.8 MB (3771253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648f4fef3f68ace14f851dd813ed792173088518bde16deae95cc45c77d5c1b9`  
		Last Modified: Tue, 11 Feb 2025 01:46:34 GMT  
		Size: 21.6 KB (21580 bytes)  
		MIME: application/vnd.in-toto+json
