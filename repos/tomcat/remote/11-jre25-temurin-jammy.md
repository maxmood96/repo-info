## `tomcat:11-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:eb89129474e1d3e016cab83196fa5ac31c047501b1ab7e1555e97f7d20eef256
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

### `tomcat:11-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:f5658eecccd35aa708fa90a43e5b2501d701ab0f49c06dd53c3d434790c343e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118401511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff822c2553fb06142847138c292ead66a9c1b30cf44c4cb325279bfecd1647`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:42 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:35:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:35:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:32:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:32:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:32:37 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:32:37 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:32:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:32:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:32:37 GMT
ENV TOMCAT_MAJOR=11
# Wed, 15 Apr 2026 22:32:37 GMT
ENV TOMCAT_VERSION=11.0.21
# Wed, 15 Apr 2026 22:32:37 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Wed, 15 Apr 2026 22:32:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:32:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:32:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:32:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:32:47 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:32:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c1baff944b46f4c81c5c401a1f9f2295060e71c5e996fdb656ad42d63f9951`  
		Last Modified: Wed, 15 Apr 2026 20:35:39 GMT  
		Size: 11.4 MB (11406115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145b7cf2fa5c96bec1aa7f45ff3e8b8c47cbd4ae4bcd5bae167829a49e29257`  
		Last Modified: Wed, 15 Apr 2026 20:35:40 GMT  
		Size: 62.7 MB (62708362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b3c3e151073b8c53bce5c241b3ae6d992925e61b5f436b4dbec596e200f3a7`  
		Last Modified: Wed, 15 Apr 2026 20:35:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46dfb449ceda09000d4f9e6c6221809ffcbaddb125cd74bc5b0a8d6bf3163d`  
		Last Modified: Wed, 15 Apr 2026 22:32:56 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eb4577aaded20c9a7dde40a4fc34d865d535c3aad11625e432ac52d2a112c6`  
		Last Modified: Wed, 15 Apr 2026 22:32:57 GMT  
		Size: 14.3 MB (14334544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59880c6cbadedf581aa18569eb29381d9c87d90100fd9b1e2981cd3c21c20578`  
		Last Modified: Wed, 15 Apr 2026 22:32:56 GMT  
		Size: 213.5 KB (213477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e2ac0d18f666d5e3d1bd4fe0d7376b2b04838da20efb342ff2869ff8046b5e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24de3cb8a61f87e8afd20fea43b05220656d6cef7907d1f0fac058c682ba220`

```dockerfile
```

-	Layers:
	-	`sha256:87b22f368ee7958c1c7f3d74122bc872e7ec31c6f961a65e0da05d3a8d49b808`  
		Last Modified: Wed, 15 Apr 2026 22:32:56 GMT  
		Size: 3.7 MB (3707987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f284ff7b5750b623b752593b1dbedd8f0942c73cb77e712887936359ecec2e4`  
		Last Modified: Wed, 15 Apr 2026 22:32:56 GMT  
		Size: 21.5 KB (21537 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:521b65d1d4f3865e22d955dfdf5a84aa133940369784186cafef6213151a7e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115180707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583221163eb1859ee59eb5ba7bc7e1fee313c515224c0c795888a61807dddfe4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:56 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:35:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:35:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:41:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:41:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:41:12 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:41:12 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:41:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:41:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:41:12 GMT
ENV TOMCAT_MAJOR=11
# Wed, 15 Apr 2026 22:41:12 GMT
ENV TOMCAT_VERSION=11.0.21
# Wed, 15 Apr 2026 22:41:12 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Wed, 15 Apr 2026 22:41:12 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:41:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:41:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:41:21 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:41:21 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:41:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743312518012ffd24165e334de2316b6de1877ac5d64bcb115215024d36d0977`  
		Last Modified: Wed, 15 Apr 2026 20:35:30 GMT  
		Size: 11.4 MB (11354712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d67bd4b115952626863003d0775bf47bbc516d33a5f8691226d6d914ef0fdc`  
		Last Modified: Wed, 15 Apr 2026 20:35:32 GMT  
		Size: 61.7 MB (61669449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e67f5b299cb2fe551294b184ebc9c615d30f6e6449db42ddb5272624858c55`  
		Last Modified: Wed, 15 Apr 2026 20:35:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b66c08a2845b5c7ca117941c2e31f4a36609258ef3a47af1a91647226d4f8`  
		Last Modified: Wed, 15 Apr 2026 22:41:29 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad448b16925f3bf3513fe96951227425bf150f1eebb05445371871156dd7e7c8`  
		Last Modified: Wed, 15 Apr 2026 22:41:30 GMT  
		Size: 14.3 MB (14335000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f9bfacd709fda4fbc14106ce515c70d6a1eaeb45a48f5b215f6bc6acffd623`  
		Last Modified: Wed, 15 Apr 2026 22:41:30 GMT  
		Size: 212.5 KB (212487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:9b29acf04eed55356a05cebe126ebb65e47393946b03308b227ad7c1210f4268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577a16268908e049c2962482eb05128266b7781dd7e333ad1936a0000b4d718e`

```dockerfile
```

-	Layers:
	-	`sha256:8f07a259be614cc90f5d94b91c058ac4c6103e065dc2ea6091afdd2b5449112e`  
		Last Modified: Wed, 15 Apr 2026 22:41:30 GMT  
		Size: 3.7 MB (3707650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129ec60b728e62443d1d6cd5d1cc4be33078987658a3baba168002d3dd5f6976`  
		Last Modified: Wed, 15 Apr 2026 22:41:29 GMT  
		Size: 21.7 KB (21695 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:99d8543f225f469abe8bcd53d45e07e564f6e84cabb451e57cc870d95ac50426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123264972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27596498a5a5793e217aad49ab0245e427fe1c554b97f02b4429bb9adf9be0c0`
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
ENV TOMCAT_MAJOR=11
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_VERSION=11.0.21
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Mon, 06 Apr 2026 19:09:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Apr 2026 19:09:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 19:09:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Apr 2026 19:09:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Apr 2026 19:09:13 GMT
ENTRYPOINT []
# Mon, 06 Apr 2026 19:09:13 GMT
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
	-	`sha256:b44073b3cef92f0ed2ae78d5cb347d0c821eab5f06de4eb087e112f6e74c28bb`  
		Last Modified: Mon, 06 Apr 2026 19:09:33 GMT  
		Size: 14.3 MB (14349124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a002f3e393769db36695bd716d71cc4d693fbffe5a687b8e12bdd79dd99b`  
		Last Modified: Mon, 06 Apr 2026 19:09:32 GMT  
		Size: 243.3 KB (243267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:cdeeae0776c3df932fe245b4ec6d1103b1d63057f8b19e9c1855faab9f662139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddd548f8a4f166783fc50c73368ee2c1474804e3d2ebae3edeabf83d95853af`

```dockerfile
```

-	Layers:
	-	`sha256:58e907c6e200b5f743ac80013d6402b3a99e339c817abd86b54d7e93fe0b217a`  
		Last Modified: Mon, 06 Apr 2026 19:09:33 GMT  
		Size: 3.7 MB (3711333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f6fcb4df397da1a02fb38183fd4459fb392187a3626a49c4d99cdfffdbb00a`  
		Last Modified: Mon, 06 Apr 2026 19:09:32 GMT  
		Size: 21.6 KB (21595 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:fcd1876b1da8d88206e15327c66bbfdb82fd3221c03b48dcccf65ac438e68a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114576940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5279a03d87cf706e857e93ea4816a9d9505a401bef2a4b377ee69180b07a957`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:47:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:47:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:47:10 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:47:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:47:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:47:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:47:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 01:22:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Apr 2026 01:22:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 01:22:59 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 16 Apr 2026 01:22:59 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Apr 2026 01:22:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Apr 2026 01:22:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Apr 2026 01:22:59 GMT
ENV TOMCAT_MAJOR=11
# Thu, 16 Apr 2026 01:22:59 GMT
ENV TOMCAT_VERSION=11.0.21
# Thu, 16 Apr 2026 01:22:59 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Thu, 16 Apr 2026 01:22:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 16 Apr 2026 01:23:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 01:23:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 16 Apr 2026 01:23:04 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 16 Apr 2026 01:23:04 GMT
ENTRYPOINT []
# Thu, 16 Apr 2026 01:23:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f19aa0d0411a5c0643187a344eee948bcd0bb6b44180ff22d32df9e8c9c1738`  
		Last Modified: Wed, 15 Apr 2026 20:47:46 GMT  
		Size: 11.5 MB (11499282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a43b76c1e35285b5333200051098c535b647ba5dcf020a8ea2d56d106abe92`  
		Last Modified: Wed, 15 Apr 2026 20:47:46 GMT  
		Size: 60.3 MB (60322031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2025a7c91e2d067a841a08a1f69e13fd7db34f71a4255d398f9333df24ae2748`  
		Last Modified: Wed, 15 Apr 2026 20:47:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa3b143a64a5c3683a310e42f2651c878473ae23774309bda03431d5d8534b2`  
		Last Modified: Thu, 16 Apr 2026 01:23:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49c68b932511de94aa6e027796e9933c6d65438ff70a40c0ab339215f6e40d1`  
		Last Modified: Thu, 16 Apr 2026 01:23:18 GMT  
		Size: 14.3 MB (14336171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8ef8f16915c4ae55bdaf224b751c29c3b6247a48966725dab06cd37b1ca0f1`  
		Last Modified: Thu, 16 Apr 2026 01:23:18 GMT  
		Size: 214.6 KB (214638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:46a2312256de3e3ad1f1a2527671ef4b8611bee37860995a90f2a8b3bc44fec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523054d2cb6793aebe9f6595247fbb607787c6be73329d6d97092cec3bfa855`

```dockerfile
```

-	Layers:
	-	`sha256:0ead75929ce580a72e382021cca3fc7627c389b4a1ebb7404db3fb580d699475`  
		Last Modified: Thu, 16 Apr 2026 01:23:18 GMT  
		Size: 3.7 MB (3708972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d5625255f011e88819c366b3d696871f8538016af35cddf04cacc6be01ef3b`  
		Last Modified: Thu, 16 Apr 2026 01:23:18 GMT  
		Size: 21.5 KB (21535 bytes)  
		MIME: application/vnd.in-toto+json
