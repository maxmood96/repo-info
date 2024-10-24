## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:4194761d7493bb2f5978172e65bf0c9dba7a5dbf4bef9623700ab9c0406bf14d
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
$ docker pull tomcat@sha256:e54f11d48f6fd541f75fbc0b9c4e811a103e199eac57348f409f6bc6e6705b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112309972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0d421d1b7ceb53a255efee96dca378044a388064aa6457bbecf5bdd7a51baf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edefee3c927b04ff0aa92f648384218aae20f0449dcfdc56d4da14932e7c67a6`  
		Last Modified: Thu, 24 Oct 2024 01:00:16 GMT  
		Size: 16.1 MB (16142399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45d0c4af0e693e9813b214cd438cc32b8f851779ab655a4bb5aaf37383c8f1`  
		Last Modified: Thu, 24 Oct 2024 01:00:17 GMT  
		Size: 52.9 MB (52870645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b71518ebe7e588756fceaa52111bff28114a1eb16e075cd4ff5b0793912890`  
		Last Modified: Thu, 24 Oct 2024 01:00:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7e35a6ba915a2a3fcd792719fe71b725880f0e8c7d872d780e275ff39195fc`  
		Last Modified: Thu, 24 Oct 2024 01:00:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acddcf74bcb0ecaff5ecb3dd8996b157d457bfebfe92aaf0922d23c46ad269b`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1339c69c053c2aeb1bd0c933ec1c948d772350f366acf890d51cc14f5ccfab1`  
		Last Modified: Thu, 24 Oct 2024 02:54:24 GMT  
		Size: 13.5 MB (13529422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9a3543e4ca9f47d6771ed2a54b1a3229908a9e38d472b9350129d6cbb50a3`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 229.2 KB (229173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6ca9f8c0e3adac0bb919ed0756c4d17fa6d33f3a158a6e8a39df4f448a4e1933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3797390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e94cdbbc43b1185c2e5053afdfb38b633020e9ae6f437c21ea6183dd003d6f5`

```dockerfile
```

-	Layers:
	-	`sha256:62255256559d510336e28dab43e58544b8ac89e2261729d79d7864df53ae1286`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 3.8 MB (3775298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0caf731736ceab468d4ab545ccbc1ff6972d0f09e3a39d9753a6ff0aaa124ec`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 22.1 KB (22092 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:fa2666fb314e94869e478f8fab84c10a41e021c247e27ef80079327c97b22d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109216997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6299ca1cc5dc77e0ade95745fc416ebcde125ca7067a353ad6d758d554677690`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed9c9e35560f5ea4cc537cf880b4795762d4daf47470f9a6f261201526c0bc0`  
		Last Modified: Thu, 24 Oct 2024 01:17:46 GMT  
		Size: 52.0 MB (52035054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51ac66e2ab77ed76cc919d370bea7ad9a77519936255caf8cf830cb262335d0`  
		Last Modified: Thu, 24 Oct 2024 01:17:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf197725d6f541a08df1d8988ee0e2ff6f55a3119704585ab8fe35897a932d0e`  
		Last Modified: Thu, 24 Oct 2024 01:17:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e3e396bb55d5e2fcc6c1229ffff6085e6ab4038ff2e71a42feb1cf60b7aca8`  
		Last Modified: Thu, 24 Oct 2024 12:33:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5363cf69d20a31b2fa897e730965f900e26daa27fc2fa7269d721a2a40dabd3`  
		Last Modified: Thu, 24 Oct 2024 12:33:25 GMT  
		Size: 13.5 MB (13530466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d112f741a7ca9b0289e15ada2d0c01a9f0ab6ea8b6d1203931b5206f8edb62ca`  
		Last Modified: Thu, 24 Oct 2024 12:33:24 GMT  
		Size: 228.4 KB (228382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:30a23920c01bc3d8ada37dda897cf1b67ecbbe4efaa8ff22eea4bc79973bdaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3797230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4f59b0d471297e8b00944fed65e7692491c8e52d176a20ef4e2c7db35efc17`

```dockerfile
```

-	Layers:
	-	`sha256:2592467b53b99e69b571476ff8341f6abf41b35fc15da97884da761b961a388f`  
		Last Modified: Thu, 24 Oct 2024 12:33:25 GMT  
		Size: 3.8 MB (3774977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91627204cd0f5b250177b0bea72c960b6911f67bb7a2ba9a14f77eb5e853820`  
		Last Modified: Thu, 24 Oct 2024 12:33:24 GMT  
		Size: 22.3 KB (22253 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:fd471b4bdc7f15d9e370823e005eceb68d521a259b7cec013f811a3eef8f5dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118819885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140e480bca9e3e743468cb59a69d3a8bb6e3f83fd4a7050133b69099b2d0bb91`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25f263398f52f1fd5d2971288c49651f0246bd2f3011467de92f438e928adaa`  
		Last Modified: Thu, 24 Oct 2024 01:20:37 GMT  
		Size: 52.9 MB (52917314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3ea9fe1d971300b827dd8ea674c842e5a5df48673a9d7371fa33775cb7fcf`  
		Last Modified: Thu, 24 Oct 2024 01:20:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a18372e0222a6f110ed2a5448578a820bbb5ff4bac49e6b56a9aa08d2dcd7c`  
		Last Modified: Thu, 24 Oct 2024 01:20:35 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35621d2720164605360c709cb1ee24b73e565c4d0c918d2ab79d678b3b7e6dae`  
		Last Modified: Thu, 24 Oct 2024 09:53:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3a0b5db154689d4729cadea2f38f4f16b076c0a919898eaba4c3f8d2d31d1`  
		Last Modified: Thu, 24 Oct 2024 09:53:23 GMT  
		Size: 13.5 MB (13543955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d948be4a03cfb1e322bedd061fd6f302b516d359acf6e2977e071cbf881567d`  
		Last Modified: Thu, 24 Oct 2024 09:53:23 GMT  
		Size: 258.8 KB (258826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0ffdeea753674e83026a528f10a418ada4c8461c036129773e0afb68bbefdce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24e4d095a1faaf96c50508d755e3601bf50cf669874fdbab3abf48c97d1a9ab`

```dockerfile
```

-	Layers:
	-	`sha256:caa149bc7bcd266cc4e726ba8885ee62e5d18338e55a4f61493312684d0b1f92`  
		Last Modified: Thu, 24 Oct 2024 09:53:23 GMT  
		Size: 3.8 MB (3779238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5372d0630b88d56b4ae503ba5d47bdd324c0f391c3a0a810f3f135ffe11a06e6`  
		Last Modified: Thu, 24 Oct 2024 09:53:22 GMT  
		Size: 22.2 KB (22151 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:7863d2cbfe8f5a0b36fb7300957f712eccab4814a174b54cca19336052c6e22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104396509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8469ea896a364156933e321f442b91c9a470c61bd0b5d54cc3dc13b03f4e0c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930446b1bcd01fe732ccd6c0777d5a5556f080ae138efc45b08957e86a30da0d`  
		Last Modified: Sat, 19 Oct 2024 03:55:21 GMT  
		Size: 13.0 MB (12970024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f74b8fc4cc56b6306b6dfcabe22b04d2bb68f27a44dce4caeef54ac242caff6`  
		Last Modified: Sat, 19 Oct 2024 04:09:07 GMT  
		Size: 49.7 MB (49669474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2848e9eb3eb625bedf1cf0847f8ed99a437972eff5058482598d2d0bb7f9c0`  
		Last Modified: Sat, 19 Oct 2024 04:09:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5805bd3747b04a9037c36b8e337eb1a8aca0cc88d53e9563eda8fb597fb9b5a0`  
		Last Modified: Sat, 19 Oct 2024 04:09:07 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58650734e044b20cd59e75d9c711b2f9552e20df73855b71ef7c484185d22319`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f38de937ba2241620f649c94c2009dda4f5e1be8097f91585d42de137fbaed`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 13.5 MB (13533477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7611652255f490bd28e391e975e2c774be75b60fe7ee0596b5cd41b92de2a8f1`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 219.6 KB (219588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d06e7ae67736906fd62ff28d70e4888f7c3a98556af4df84b103a4d4d2af3636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3650839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dac7aa62d5177920a9386932ee98adf7bd12a79cc146f8973c372d3883993d`

```dockerfile
```

-	Layers:
	-	`sha256:7d747d911db8f460718bb665128cf2d3f0419e7a207a55b85db9ddb4146df88b`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 3.6 MB (3628749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3faa4795e0a5c7e3c74448fe7689115b644725d05283faf9e1e3d0a15e8b1298`  
		Last Modified: Sat, 19 Oct 2024 16:10:40 GMT  
		Size: 22.1 KB (22090 bytes)  
		MIME: application/vnd.in-toto+json
