## `tomcat:jre21-temurin`

```console
$ docker pull tomcat@sha256:cbd8322626dd0154cfe1bbcad2306ef4723c13aeea3324d6260f1adf839416f9
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

### `tomcat:jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:0477503e35f38c53d3962cf7070b65b00f585f767ac35873ad0e1b7804f2128b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114077585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0822eda8ecaa38dbca5699a4562faef48e9603de09246142bb6a409b1d6938da`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Sep 2024 14:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_VERSION=10.1.30
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_SHA512=9e5f46fdb984d9e48f2608d78352173b7e9b72c384ca0886a9384120d96d2c9302c26d2314e646152605e5e4b044f705feaaf13146b0e72dd535a9625c7746dd
# Tue, 17 Sep 2024 14:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:03:18 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316f85472e42ddf39be81d37cefcaa87cad98b7ca1710864ef2b8e67e9713b`  
		Last Modified: Tue, 17 Sep 2024 01:07:39 GMT  
		Size: 16.2 MB (16177262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b3a3c8c200f13edcec126f24300dcdaeb5d0aff4af43c8bba72985de4ca9`  
		Last Modified: Tue, 17 Sep 2024 01:11:56 GMT  
		Size: 53.5 MB (53513805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e9495ad94208b125347250793a75d8d69f3e1bb895ef90d7abf4e668d59427`  
		Last Modified: Tue, 17 Sep 2024 01:11:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd143379b4af343d0a937acd6774b001b41556b8dd61893000b6912273b345bb`  
		Last Modified: Tue, 17 Sep 2024 01:11:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb78549124f7cf927f58723fb8b84e92926fc443c7a2669d24e334cb534e5493`  
		Last Modified: Wed, 18 Sep 2024 00:00:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46ffd3688c0c1f11983b0820282e5bea978fc8371bc55bd53d7604b8aeb2c74`  
		Last Modified: Wed, 18 Sep 2024 00:00:36 GMT  
		Size: 13.6 MB (13560175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39d9f6b9d305bf1909ba851bcb37e4af62938efc316dba1d509a6109206b30`  
		Last Modified: Wed, 18 Sep 2024 00:00:33 GMT  
		Size: 212.3 KB (212324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:5faff15f426a95f4d2b26dea3ffd65e793b2772d81178e479f02a0206e469c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a4c667a2cd0bb5aec1d998590dd17437d9b379ec455aadaf588032f5736576`

```dockerfile
```

-	Layers:
	-	`sha256:f6139955b5392e81c4dd809f4d1dd51c5043f723f589f481bbdb947cd75720e9`  
		Last Modified: Wed, 18 Sep 2024 00:00:34 GMT  
		Size: 3.0 MB (2984869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc12609f72c4b7f4d35da75b127adaa102120441be94d4fde8313d5aa0f84f6d`  
		Last Modified: Wed, 18 Sep 2024 00:00:33 GMT  
		Size: 24.6 KB (24575 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7d320d695d447077d3152e03cac3d715252b3978578ca1dc64ae64f0eeef58de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111761463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf386e980e78362a524da2e55e7cf4af16645bcf5ada49dd4eeabdac6e369203`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10c682b9856cc71f6540269cbf6510c4d5c4b07d334875eb836c645d4cd40c`  
		Last Modified: Tue, 17 Sep 2024 01:37:44 GMT  
		Size: 16.0 MB (16010924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6c128b04d6307157c70ea0ea9a99d0c7fd21a01eac306478f490da4fa26740`  
		Last Modified: Tue, 17 Sep 2024 01:41:27 GMT  
		Size: 52.6 MB (52641542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659cda2b1238193b2869c9e69387565ca0f46371cc7e93cc2aa90bf2de25cd2b`  
		Last Modified: Tue, 17 Sep 2024 01:41:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142da10deef4b5de133ad95226b39bf0e589716ed2e0243c480d4dae53c2d7d6`  
		Last Modified: Tue, 17 Sep 2024 01:41:21 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c842236f845f7fb2c63648238345ca3009604f8693ba01d7e01e6f0a72ccaad1`  
		Last Modified: Tue, 17 Sep 2024 09:55:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734ed5334f8e8617fa0348a81b57ee0acf30687323b2a29384cb1e43db78b986`  
		Last Modified: Tue, 17 Sep 2024 09:56:20 GMT  
		Size: 12.9 MB (12941100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c6b00387b3dc95f6f9980b092680e122b06063a3599e6ddc4c193120f41129`  
		Last Modified: Tue, 17 Sep 2024 09:56:19 GMT  
		Size: 212.2 KB (212221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:f19bac370af26ed69122f7318d7e71e7bcc00eb40744a8f3d586d767a81f07c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a5f38c8659cd986707bba0e884a8693f1f0d32430c9494f4abad74a8d30ea8`

```dockerfile
```

-	Layers:
	-	`sha256:d50f480efc9f56c713f803e6c497d1ee909c1c2ebd86a26acb73ee692d89ddb9`  
		Last Modified: Tue, 17 Sep 2024 09:56:19 GMT  
		Size: 3.0 MB (2986051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f694426b4b8d3b0cfe7741b9fc89fdd4b07164cb94c3bdd50379991d3e7838`  
		Last Modified: Tue, 17 Sep 2024 09:56:19 GMT  
		Size: 25.3 KB (25334 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:feb000cec7fc3027119700ec7f0dd91044ec1f7668b81ce70bddc5a975ce1fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120454515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadcbbccb209a967ca437dd733db93d056401a28d3553940ee1b5769999c7885`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Sep 2024 14:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_VERSION=10.1.30
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_SHA512=9e5f46fdb984d9e48f2608d78352173b7e9b72c384ca0886a9384120d96d2c9302c26d2314e646152605e5e4b044f705feaaf13146b0e72dd535a9625c7746dd
# Tue, 17 Sep 2024 14:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:03:18 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5238c0d3f97d3a0bb99bc13e9f9d3fe8c0a98a4ff7994e3485eb4e699a551d`  
		Last Modified: Tue, 17 Sep 2024 01:06:02 GMT  
		Size: 17.5 MB (17533628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51a810d0b3156bda2466be4fe9fdab4ca2800d3d961965dd54c813d73da3ea`  
		Last Modified: Tue, 17 Sep 2024 01:10:53 GMT  
		Size: 53.6 MB (53573768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e6ba28e8b22947cfc6b2a2cdd6372625dabaf3b0480d0e2d0346d1d4291d`  
		Last Modified: Tue, 17 Sep 2024 01:10:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f0193786a3d4159cdb9575e4c8fa21a05edaeb0398803816269af4550b50a1`  
		Last Modified: Tue, 17 Sep 2024 09:41:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551fe1c02c2ae459ceb588adc814d74543d294423565d835bf501d5d00699066`  
		Last Modified: Wed, 18 Sep 2024 00:11:06 GMT  
		Size: 13.6 MB (13579269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b702886484549d33261a6eb671489a6e80d5ab0ba4a3c9bca99ff6676c58d6d`  
		Last Modified: Wed, 18 Sep 2024 00:11:05 GMT  
		Size: 247.2 KB (247199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:559e143286d5af9e61ee8ef6d59d94f22da976b681c9c356a9ca7c492af09152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d65f31c5feb7b4acbe1b701c749a32e47712e2041ba766c33b80fe0b976a16`

```dockerfile
```

-	Layers:
	-	`sha256:f0f324f3f38491fec6de82c38c6aef4db9ec6a74dc415d689ed49369e6dc3587`  
		Last Modified: Wed, 18 Sep 2024 00:11:05 GMT  
		Size: 3.0 MB (2989441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:468c373c4efd968e7e346a69fba2e9ef685f5f12cc8d4598f6848b25eabda061`  
		Last Modified: Wed, 18 Sep 2024 00:11:05 GMT  
		Size: 24.7 KB (24698 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:3be55afac14ad332232786be44488db571375337326fa5b0cc78e3458d7ae80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109791152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f6470f6861eecf636281362aef65fbde2647cb87df2b4699021fb6c36710ed`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa806051defda3e7a36ed8367d52c08e84f30e5a78265c4e79116ac5c645d6f`  
		Last Modified: Tue, 17 Sep 2024 01:39:06 GMT  
		Size: 16.3 MB (16280949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548fe2a5a17fc64aca361333808056dc1451db1d6ad07aad8266485fc2e1a8f2`  
		Last Modified: Tue, 17 Sep 2024 01:41:38 GMT  
		Size: 49.7 MB (49669862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faccbe91d8abc2d74cf9315e2ac80d07ba7d795a650066862000956d110bab3`  
		Last Modified: Tue, 17 Sep 2024 01:41:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373ed7a0cbd63612e89cdb819205a6f40cb4be7cafbcf7d945ff548336dd86e`  
		Last Modified: Tue, 17 Sep 2024 01:41:30 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd16b30202a0103432465ac0bfaa9c28ada46811f4c77056efb432ec61a3b7b`  
		Last Modified: Tue, 17 Sep 2024 06:17:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d580303df5b29841df081d80fb3e39afcfe015a00de1803caf6243dcb429d`  
		Last Modified: Tue, 17 Sep 2024 06:19:14 GMT  
		Size: 12.9 MB (12948682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f913e9c4d984c6cd147314ca454e7f90065ecfb22549d374233e19f4f50de1ed`  
		Last Modified: Tue, 17 Sep 2024 06:19:14 GMT  
		Size: 223.8 KB (223799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:020b329ac3c7e075ae1160575cf1083a8ac79180211e5e5699f708fa8fb4afb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75e1bf48a0662408702716e1ea679d10faf3cf82be2e88d05d1dcf8768cd4c5`

```dockerfile
```

-	Layers:
	-	`sha256:b55c8fbd998aa861cb70869002bd391c4b7ff34b6e9b151ad8d0095c07a20149`  
		Last Modified: Tue, 17 Sep 2024 06:19:14 GMT  
		Size: 3.0 MB (2986592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5c35c92ebb9b0b88f056db3afc7db56e92cf4bae2dc98a34c554e744aea946`  
		Last Modified: Tue, 17 Sep 2024 06:19:14 GMT  
		Size: 24.6 KB (24598 bytes)  
		MIME: application/vnd.in-toto+json
