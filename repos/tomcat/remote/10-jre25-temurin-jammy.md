## `tomcat:10-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:bfa00a8f966fa7f9ceecb612d9b3e9fe81c41226ad2a69951973289d4d4726bb
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

### `tomcat:10-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:19e0e22ac9f2c8a090fbbd60f48e778a663a5de1d2a1e77a2be81632a47ab9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118381214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cad0f40acc5dee51bc392fbff511aff1dd6b15bedb320b194f1b8bae28b186a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:49 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:11:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:11:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:11:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:11:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:10:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:40 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:40 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:40 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:40 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:48 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aadd6bbaba2c1658aa88955060e069c13b9a6220529210f6218937a4684152d`  
		Last Modified: Wed, 01 Apr 2026 20:11:24 GMT  
		Size: 11.4 MB (11405179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764f16fe8726ff63fd80cb37f1315d800a10765a26e7de67ea94175321c9f6c`  
		Last Modified: Wed, 01 Apr 2026 20:11:27 GMT  
		Size: 62.7 MB (62708384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e354014f3e042d349c3be1a024869fc85753cf0230f22d2f5a4e2422898f88d5`  
		Last Modified: Wed, 01 Apr 2026 20:11:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba906394bc548f73609f533e51dfe01fac6d780bb2327857d4c8e286bed4d7a`  
		Last Modified: Fri, 03 Apr 2026 18:10:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eda795f37127b8b5ae036ee8fce100d7ba4e62b9b0fd24800e67b88b23f71f`  
		Last Modified: Fri, 03 Apr 2026 18:10:58 GMT  
		Size: 14.3 MB (14315201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ca6344c908d5ea2ebf8dc070b581e415201a5afac1e2cb9029ef98e2160fd4`  
		Last Modified: Fri, 03 Apr 2026 18:10:57 GMT  
		Size: 213.5 KB (213519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:03885fd362df0027aa58a5db5a10374257ceb6fdaadf3100756648c527e47008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb6ad5664b4333d6b3a0283d1bb398d0d608697bb9f1148564689af29265ae7`

```dockerfile
```

-	Layers:
	-	`sha256:c4293a167d13f0f09670ffaea650c3733f70e59b3c0fec6eb5cec59e0218b011`  
		Last Modified: Fri, 03 Apr 2026 18:10:57 GMT  
		Size: 3.7 MB (3707667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2660245c44275e21a4b56eea3f7f1c99cccf4d5e011121135f02646c384e092`  
		Last Modified: Fri, 03 Apr 2026 18:10:57 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:33d64b4aad02d642940a8c4117bf29a6f1dbd7db84784befedb7f76282524b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115160746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cca0875baaebb9a0428810dfa7d8dd0cf656a97073e9fdee6269674cb41898`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:11:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:11:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:11:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:11:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:10:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:21 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:21 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:21 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:21 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:30 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:30 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f4f25709133c1089eb93eff20c7bb1c529a9b2281921de903be9c8ecd33d3`  
		Last Modified: Wed, 01 Apr 2026 20:11:30 GMT  
		Size: 11.4 MB (11353690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec132fc78ea3afb24a6b88ef0f0f987c22f45a258a9c340f1d5194423d310ce7`  
		Last Modified: Wed, 01 Apr 2026 20:11:31 GMT  
		Size: 61.7 MB (61669461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e354014f3e042d349c3be1a024869fc85753cf0230f22d2f5a4e2422898f88d5`  
		Last Modified: Wed, 01 Apr 2026 20:11:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecf0319ae3601b8071e30ef4b3d12f26a75ca9188e13fa892abf4688f07b6da`  
		Last Modified: Fri, 03 Apr 2026 18:10:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8610ea3023fc76f94ef0223f0e0a75c1cb1e07dbb36026b4f61350af73428d96`  
		Last Modified: Fri, 03 Apr 2026 18:10:40 GMT  
		Size: 14.3 MB (14315589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081c74e23bc2bb170a6357434327ad0d89988fe74437e26c966062eefb5ec765`  
		Last Modified: Fri, 03 Apr 2026 18:10:39 GMT  
		Size: 212.5 KB (212547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:46b23b9f895ae62c1c507afce883632c74e5c2070897a1d0f6d3ec45dc3dc0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eac0be7ad649ea38bea2677b3d07de378f185a7d1a4cf16d27451dfe12f29ad`

```dockerfile
```

-	Layers:
	-	`sha256:4064f4780c5c5da0093558453de194b6f827f531c6e347cb3854ca577014f728`  
		Last Modified: Fri, 03 Apr 2026 18:10:39 GMT  
		Size: 3.7 MB (3707318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1b7136f32fa974e50af57fb92402e84e96e8ca17c9b7804f8367ca0df64618`  
		Last Modified: Fri, 03 Apr 2026 18:10:39 GMT  
		Size: 21.4 KB (21361 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:2899165a91751d6849e1d901117cff3b7dd0c4a0c43829d78cdc818581113942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123242992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c66fd243fc51d0c5d343410d1f9f7efca106612eff1c796bbdad2f4252a8879`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:26:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:26:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:26:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:26:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:26:34 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:27:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:27:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:27:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:11:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:11:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:11:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:11:16 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:11:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_MAJOR=10
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_VERSION=10.1.54
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:09:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:09:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:09:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:09:18 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:09:18 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:09:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147a9beadb81a1d33481f390636557db99f92cf2948b902b1ea12e9e885b65d`  
		Last Modified: Wed, 01 Apr 2026 20:27:39 GMT  
		Size: 11.9 MB (11893177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fa3e1feef8fec397180c6adbbb2c8cbea141774183f90990a311b96474902`  
		Last Modified: Wed, 01 Apr 2026 20:27:41 GMT  
		Size: 62.1 MB (62127226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c756ce39e20d209b8627f7c9f756a6a22d1329ed2078552a26a280dc722b3b7`  
		Last Modified: Wed, 01 Apr 2026 20:27:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34616904fac3f1ca3b01fd31fc6fbb59aa5422ffcc0b3b300f3db9da5531525`  
		Last Modified: Wed, 01 Apr 2026 22:11:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05085dc961dab072bb1eb41fa2aa6b7031d6a7dc0271971d937cf6e9f6865981`  
		Last Modified: Fri, 03 Apr 2026 18:09:46 GMT  
		Size: 14.3 MB (14327152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46238bf5c78f6f5b6a160bf7a02baaa589d2d4157bd62f8cc6ce4404fc99ea3`  
		Last Modified: Fri, 03 Apr 2026 18:09:45 GMT  
		Size: 243.3 KB (243259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e430287bf37aba0cbc81d2ff78cefa6d39ca6390c76ca84acf870f4d9040eb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaf08c030a9e8cab5900638428f042eb907eb5168ae04cdf55e64d4068400b1`

```dockerfile
```

-	Layers:
	-	`sha256:3f5c20463049bfad716d345767a69e6e53c3c8ef9e9229a3d4bb6e2230f1bc56`  
		Last Modified: Fri, 03 Apr 2026 18:09:45 GMT  
		Size: 3.7 MB (3711007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620944a82940ef196872a84caebb6ee50f9de24bc11b39e977c9b98df6308755`  
		Last Modified: Fri, 03 Apr 2026 18:09:45 GMT  
		Size: 21.3 KB (21265 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:43f99ae69f9dbb7555b052521313efd912239249d0d35036ebd45d54e27e57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114554424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05bb6de042494c2e0836eac4af3d6d90def81953c0354b7ecbee355e99b0f58`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:13:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:13:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:13:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:13:44 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:13:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:13:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:13:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:39:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:39:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:39:37 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:39:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:39:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:39:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:39:41 GMT
ENV TOMCAT_MAJOR=10
# Wed, 01 Apr 2026 22:39:41 GMT
ENV TOMCAT_VERSION=10.1.54
# Wed, 01 Apr 2026 22:39:41 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:09:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:09:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:09:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:09:16 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:09:16 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:09:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6b68915582a456490cd19023117787b15b5ff800ad05ede15ac7b96beaf237`  
		Last Modified: Wed, 01 Apr 2026 20:14:18 GMT  
		Size: 11.5 MB (11497814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b184d9a91ee3c692113ad7979093fa54c84bc43bfc0026c460a7bfc691a98d6b`  
		Last Modified: Wed, 01 Apr 2026 20:14:19 GMT  
		Size: 60.3 MB (60322088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234ccdd42ce0f499447941d86e2b1c80e77ca60023abd029f80e2f7ac290b191`  
		Last Modified: Wed, 01 Apr 2026 20:14:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836c270de8c6afc5bde2e8ab929d8199b986488d98b7bd2be226ef2f02be54ee`  
		Last Modified: Wed, 01 Apr 2026 22:41:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34859a40e695e58337c9ff2e65a52aa6cf903e4b3c3845e236514c9e947251`  
		Last Modified: Fri, 03 Apr 2026 18:09:32 GMT  
		Size: 14.3 MB (14314600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69914c46dfa3e4e23f485fb6c3e906e4144e82970a111323ffede3de9553f103`  
		Last Modified: Fri, 03 Apr 2026 18:09:32 GMT  
		Size: 214.7 KB (214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4c248e24caccf4ac25025e26b10aa0e27eec813fb12a8b23a1b720be9ae29adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c6fa9c90f8bac57ccb16554a59fe2a38e3048082de90cce33db801f417506e`

```dockerfile
```

-	Layers:
	-	`sha256:68db6b3cf72578e26c2afeaa90dfc12a4b6a5de511cabf47531e531fa0726a1f`  
		Last Modified: Fri, 03 Apr 2026 18:09:32 GMT  
		Size: 3.7 MB (3708652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee8ca609b91c0ef6c7dab2e3b3eda78ffa1642942f1fe6518a243bb3ce37169`  
		Last Modified: Fri, 03 Apr 2026 18:09:32 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json
