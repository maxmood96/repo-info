## `tomcat:9-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:940fdf625006cf6c548e2c4006144b28a9ad0bbaeab82e7f6254e1352f301d13
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

### `tomcat:9-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:bc18587e335edb008201e405664d8e9f4da5f9219e865cb27dc4b190a170ae8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106659203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0725432151ae15b50e4651fc222e5160bb59a1f24ccf42dd0834439aa01cee9c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_VERSION=9.0.108
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Wed, 06 Aug 2025 20:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:12:57 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:12:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24a8b9e652f47dc5aae4db79deb296bc65f3697a15a864fc909054ac494c90a`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 16.2 MB (16150578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3929ce9ef98d521214361456dc3601b66f098801031407f6deeeec81a92929f`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 47.0 MB (46986099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df735f481adca6219ee0da74f1af97ec6e7649e2f83eb571ef24cb12912ab99`  
		Last Modified: Mon, 01 Sep 2025 23:08:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265f6ce5d5f4b2c356439476a7ff09f37148e2c8c35aa6fb7f10c2f1d0755029`  
		Last Modified: Tue, 02 Sep 2025 03:08:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7185a2ec194e15a25c820bc6701a11bbae79d736073f3cb60686965e19acbe55`  
		Last Modified: Tue, 02 Sep 2025 03:08:26 GMT  
		Size: 13.8 MB (13753269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65791bb48b6f3572cd074176fc5c4539b064820e1acb6c8e41a28e7ca6b31684`  
		Last Modified: Tue, 02 Sep 2025 03:08:25 GMT  
		Size: 229.7 KB (229681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6ae4c3117d447b34de02c46993a78ee6ab4cabed4a2598ab8dffb3a7a8d435c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f12843c18b9cdb2fe2270c47b04670c0f26f0c5f91b809ec5cfa84ed6d52e9`

```dockerfile
```

-	Layers:
	-	`sha256:2ef6819cc08d899c38abbaa41a60d4a11de6897f616e28f2c74419b4b6b0e41d`  
		Last Modified: Tue, 02 Sep 2025 02:36:14 GMT  
		Size: 3.9 MB (3937263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c475534cb9bde6045a3f9bc2a01d0415f2b0d99ae8ff1357251c3603be414def`  
		Last Modified: Tue, 02 Sep 2025 02:36:15 GMT  
		Size: 21.3 KB (21256 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:480feded947546be4b1b5daa43ebb1b941016b9d30fa38c091169fe971fc05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101084522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40763c3fb2f2284f59a8c1f61d80ca43362bb38466e8f48310d47e04a9bb774`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:02 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:05 GMT
ADD file:56dd1608fa49343c3815b8373825d581303e97b21994ce0e1d099bf09251caea in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_VERSION=9.0.108
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Wed, 06 Aug 2025 20:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:12:57 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:12:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6530e67fdf3958f32e486561f05a1170b5fbcd419c51eb435b13993ecadad7b3`  
		Last Modified: Tue, 12 Aug 2025 17:02:44 GMT  
		Size: 26.6 MB (26642919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da254942fc2ae7b2cdf3f227af1c842bdebbd1573712272ea2efe9e8d35cdaa`  
		Last Modified: Tue, 12 Aug 2025 17:25:53 GMT  
		Size: 15.9 MB (15889812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f503b255b93748ab874ab71257f41fd55d66ebd4d034da0f660efe3369f24a0`  
		Last Modified: Tue, 12 Aug 2025 19:21:06 GMT  
		Size: 44.7 MB (44656684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfbf30b8ba33c403afe86b074c1352806ca794fccec9bf892cd15c51ffab910`  
		Last Modified: Tue, 12 Aug 2025 17:43:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecfaf853dba4c6304bdfb28d05743f911a70e978587da396363eaf70556de2b`  
		Last Modified: Tue, 12 Aug 2025 17:43:17 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95239eb1b9301f7297ba796800b2a326525feaba1362aa1a63221e12f508146`  
		Last Modified: Tue, 12 Aug 2025 19:27:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49da91d3af1ca27fed8f03095da816f2db98b8d65e45cb47eb32f61ca4bf5513`  
		Last Modified: Tue, 12 Aug 2025 19:18:55 GMT  
		Size: 13.7 MB (13690019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac95d3cfbd89ed7e1418b4f00250c0abe9146ee029369f2f52f4bbe02bacf0f1`  
		Last Modified: Tue, 12 Aug 2025 19:18:51 GMT  
		Size: 202.4 KB (202445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c82cddd8ff4bfd79c16874b31b4659603f211b8476c3f3b664be87ff2a324b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121d3bb473557784ab9c93504665e3627667a2726f68da4ce483226651f6edfc`

```dockerfile
```

-	Layers:
	-	`sha256:f6f5ecc520d76679ce0cf2b8998b5b82832c6d7b02f2f1daaf7a10bc987a2f99`  
		Last Modified: Tue, 12 Aug 2025 20:37:30 GMT  
		Size: 3.9 MB (3939582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044a25052e5f8e3538d587cfa35ab4825a71d435c0dd6215a661da5f2bb34551`  
		Last Modified: Tue, 12 Aug 2025 20:37:31 GMT  
		Size: 21.4 KB (21372 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:862068c3ed6d3eccb0343eed65d8822fefb85736e87a2d9addfc09a087d55d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103898989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e8bb8b4ac3dcc3d69048376fd3323a58de433a45b2f150faa47bdc329fd90a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_VERSION=9.0.108
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Wed, 06 Aug 2025 20:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:12:57 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:12:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199b54d0379497df50867982d570bbd000004bfbf27017cd65c6f9eab785cc29`  
		Last Modified: Tue, 12 Aug 2025 18:37:19 GMT  
		Size: 46.5 MB (46481606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab45f69caeebdcfc0dcab7f12f318e6a8722b5101f1bf4043e99c86a6fbd7894`  
		Last Modified: Tue, 12 Aug 2025 18:37:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c74bc8d670c7b95bbe286937b0313a59d6ab9dd2b022249a7391012ef0a5da`  
		Last Modified: Tue, 12 Aug 2025 18:37:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb6d708048da6e5396557972008ab0c241b86cb7607bad1e33521ca620713f7`  
		Last Modified: Wed, 13 Aug 2025 14:33:49 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be8c6d19f2416c2480bceaf5cb219c9696e67fd2e6e4218db3c55e9291f6c56`  
		Last Modified: Wed, 13 Aug 2025 14:36:06 GMT  
		Size: 13.8 MB (13763072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac9317cb8f5d096efd2f0d639d246478c2e8fd1f29c57d47b73d6c2f29a58c3`  
		Last Modified: Wed, 13 Aug 2025 14:35:59 GMT  
		Size: 228.7 KB (228682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:222565769de8101c019df938002614494d061623418ca9ad538303c36435d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1a10b3d94961b61b11e147d844b754af835655aba2243ac99b0a481b929383`

```dockerfile
```

-	Layers:
	-	`sha256:c982eb1a4b5b18378c7838fc171277a813b9964f346e8cb4da608921f949b59d`  
		Last Modified: Wed, 13 Aug 2025 14:32:42 GMT  
		Size: 3.9 MB (3936916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc4e07b45a3f5fb4ba0574fd2c820bf3928b7e73b2f55af162def2c3180041f`  
		Last Modified: Wed, 13 Aug 2025 14:32:43 GMT  
		Size: 21.4 KB (21402 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:e8ee856e0cc23486b493a770b72f7d2f8fea539a2694b14edf4168659eeeb2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112936713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12234c5bee830ee107edc9dfc12cbb555430913835ee50794ac7b9915440d890`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_VERSION=9.0.108
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Wed, 06 Aug 2025 20:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:12:57 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:12:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb3c0b1536fe58f1d71970fd65e6541b64df3445d2eea58c017b922d91575d2`  
		Last Modified: Tue, 12 Aug 2025 19:56:46 GMT  
		Size: 46.8 MB (46826228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a22cfaf169bb1a9b3a30f0ff4c03599d0857880062e51c4f97a72acddb9b203`  
		Last Modified: Tue, 12 Aug 2025 18:22:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01334212dd4518b663caa14cbe8cddc3becdda25ad0d628881c8b62086970d9`  
		Last Modified: Tue, 12 Aug 2025 18:22:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18caaee1cc7068b86c9b6cf0ce85b91ccbabc8530f03be1fefb6e756599ea78`  
		Last Modified: Wed, 13 Aug 2025 18:08:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a680f2f5c67758442e932ebb040f39baff18908de17921cb68c853ae7c09dce`  
		Last Modified: Wed, 13 Aug 2025 18:43:22 GMT  
		Size: 13.8 MB (13781474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ce46a780273bfb9b3099c6983cd3293d6a16ac297796d0aa2313204af2de99`  
		Last Modified: Wed, 13 Aug 2025 18:43:20 GMT  
		Size: 259.0 KB (259007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:124004b9e6a365401d09a543045e0dc3ac52cf6eea8663a0c2dd8a408ad1ec18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6292e1603e26ce36080bce8a4065397b53c2a018991876f354ca4c2aae966dc1`

```dockerfile
```

-	Layers:
	-	`sha256:bac61f6006fde6fa460f3269cf44faa6041ea3c1b683675dde37aa4892797e9f`  
		Last Modified: Wed, 13 Aug 2025 20:32:56 GMT  
		Size: 3.9 MB (3941335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9192ec45d1a578898c517ffe1258476216d5bd80bebf25785cae94a39918f0fb`  
		Last Modified: Wed, 13 Aug 2025 20:32:57 GMT  
		Size: 21.3 KB (21307 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:b5925259b1b0830c787091d0dfdcbca4e0558b21a13bda132399d869d0e32bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102111446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429336a4604225424334fd8739cf4090d013e83ce0e417bc7b15f57fc267649b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_VERSION=9.0.108
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Wed, 06 Aug 2025 20:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:12:57 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:12:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ad5d5d8733c993217ed51c06da1f717784940dfd73d260506fcf34539cf5c7`  
		Last Modified: Tue, 12 Aug 2025 17:26:58 GMT  
		Size: 16.2 MB (16150057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3a6ef7bdcd30abb15d630d0ed47ea67815c291f7a3bf5b844731b8f7080ba5`  
		Last Modified: Tue, 12 Aug 2025 17:32:14 GMT  
		Size: 44.0 MB (43973854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64431dfe035d3b486eadae00fd28a970418a01518837b21a8c4bfc68bbd0776`  
		Last Modified: Tue, 12 Aug 2025 17:32:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f71376c7ff52fa7a8da0684f951c61213dc6df3870edee38fa8865fd61665`  
		Last Modified: Tue, 12 Aug 2025 17:32:05 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e431bcf809356e48bc7286f8c53d85b7c7092485ac612b63213eb59a4cbb8fdd`  
		Last Modified: Tue, 12 Aug 2025 21:31:57 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10d9ec6f2f97011b7f57ce7feccd3a8363abff284514f2dc74a930cc2d883f4`  
		Last Modified: Tue, 12 Aug 2025 21:37:38 GMT  
		Size: 13.8 MB (13750870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf61c8530fc248d06e2e9e1ac190d9acca78d0982f3847a6f24e8715c34044e6`  
		Last Modified: Tue, 12 Aug 2025 21:37:37 GMT  
		Size: 230.8 KB (230802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:8471d8f471bb3080b8ffafb5719dfee723a0c9cae0cd77c9ef9328d90041585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f27c1db253031919bb923f78968c4a5a8875945bec070b5a41a4f60fc92a001`

```dockerfile
```

-	Layers:
	-	`sha256:424c5712d93f3b473487acbc60d68aa47bca9096d61d9c9e9e6def6715aa0725`  
		Last Modified: Tue, 12 Aug 2025 23:32:50 GMT  
		Size: 3.9 MB (3938838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2554cad2c47bb4d9e1ac3049452ce4a51d7c45277293786a7696e1b4aa68bb76`  
		Last Modified: Tue, 12 Aug 2025 23:32:51 GMT  
		Size: 21.3 KB (21256 bytes)  
		MIME: application/vnd.in-toto+json
