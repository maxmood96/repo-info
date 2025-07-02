## `tomcat:9-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:d6bf1ec0458326ed787c01112146ec5525d37f4cb938b6cf388d7f27392b89ef
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

### `tomcat:9-jre11-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:81bf5ac9754f095d3798c378da9667843d20dc7e255f118181a8d66484d8de40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106869357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c5b35bae88a122935a39b143a5e0a38eeae66c6b382dd25131e74b0cab295b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5273dd58cf483b4655a5043751fff02d87880209d2ccb59df92a7d35e64efc`  
		Last Modified: Wed, 02 Jul 2025 03:10:11 GMT  
		Size: 16.1 MB (16146386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592ba7769f536f237a67eac07aadc1cd3c11904890dfaeb6e4c5926745e25985`  
		Last Modified: Wed, 02 Jul 2025 03:10:13 GMT  
		Size: 47.2 MB (47222550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e8271f284578f993012718352928bad128571676507501f1d078e3ee56a5be`  
		Last Modified: Wed, 02 Jul 2025 03:10:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2bf46a201f5eb1f12a9c691b9af155766c5378516200e4ad12c924d67e896`  
		Last Modified: Wed, 02 Jul 2025 03:10:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8eda3c949f3bf4a41265fb616db5595c6d4b965d23248e3df7fa0c77571637`  
		Last Modified: Wed, 02 Jul 2025 05:12:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9df49a6274d547d4b32b31290522bf9730d422feb855176d2a97b73ab49a0ed`  
		Last Modified: Wed, 02 Jul 2025 05:12:18 GMT  
		Size: 13.7 MB (13732551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db1de553adbbbb44197264e3741c990dbc9d990b9d571c324dfdf62a359e410`  
		Last Modified: Wed, 02 Jul 2025 05:12:16 GMT  
		Size: 229.5 KB (229542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f51ee055ce9e7049d8a8813b16f86ee2b4b66d6b2574357fee8b0cb25f62a873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12afbb8660c5653f58d6b7475a2be8ef66501c3d7447050903fe5f05ba0fcf8d`

```dockerfile
```

-	Layers:
	-	`sha256:6f992089105e7e991e751c59f48854b09cfa73688cbcd533cc491fdbcdf09116`  
		Last Modified: Wed, 02 Jul 2025 08:36:57 GMT  
		Size: 4.0 MB (3950361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed60fa067ea1f706a630f53856a46ca91c30e6d15c71bf4ebdbd2ecb2edc720`  
		Last Modified: Wed, 02 Jul 2025 08:36:57 GMT  
		Size: 21.3 KB (21256 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:294b097ffd76ebf2fc7e3e077713d707803a8fbe044d71b8bc6b374f63974770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101739953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffa523fcf4848347eef39e3a5523bddacd43482d36f0efe8a3153cccbedc84a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Tue, 03 Jun 2025 13:42:56 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c869906112a22f8bcfcd7276bcc7d904f46535968a6e8d65eb57940c3ac442`  
		Last Modified: Tue, 03 Jun 2025 14:52:52 GMT  
		Size: 15.9 MB (15890981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02be6d8f2d815b94a6fa59c206fdaa6b302f49a503749787a98c0a443d12362`  
		Last Modified: Tue, 03 Jun 2025 15:02:21 GMT  
		Size: 45.3 MB (45336703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df86b5d62108a00fee019d0ac854bdbbedd83cef949e5b09548208f616b9ebd`  
		Last Modified: Tue, 03 Jun 2025 15:02:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548b32d25609c6890710f6bcaf22f2f6d70da77c70f3c1f510b78b229a4694b2`  
		Last Modified: Tue, 03 Jun 2025 15:02:11 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a079d0a0690c7112d5a2edeb14ae84e500e193db06d3624a845763f097ef14c`  
		Last Modified: Wed, 04 Jun 2025 22:12:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b305e60d62ce8b6aab27827fbfd3b40bb279774eb3421641547daae8d07937d`  
		Last Modified: Tue, 10 Jun 2025 18:10:07 GMT  
		Size: 13.7 MB (13666701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cf5a0072fd0733665cf52a3b1aa5e32b17aa3de79af90961f7c5fd295d4482`  
		Last Modified: Tue, 10 Jun 2025 18:10:05 GMT  
		Size: 202.4 KB (202450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:abbdf731472d51f1f5001ac9eed4a75e0cbe3a52763b7937965b89e4faffa642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a89f0a4b758cf41defc67110eb2e0e4eb243eb7d020396e0ba037e75e777c`

```dockerfile
```

-	Layers:
	-	`sha256:1f94fcb17c9466b1322b46cf8972afffc68dbb74d2116c13f0f376881e9a7d6b`  
		Last Modified: Tue, 10 Jun 2025 20:37:42 GMT  
		Size: 4.0 MB (3953959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98254f7c334ddcd953b409074ac369cf7c7b6c6b26ce6bf94559a4919e5202a7`  
		Last Modified: Tue, 10 Jun 2025 20:37:43 GMT  
		Size: 21.4 KB (21372 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3ea7cb55d9a1ee594e580430214d7015e2f779fd9677756b09a5607e4fb61ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102971324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c2a121aea709f71391dc04fc77599d383ba241ead80fa215529d4198951d5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfe0c2e8be99f8d950a6958a0c910d4d550d66bf0da03d2cb05a26a4ba8061`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 16.1 MB (16059839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7e26e3b7b1fa7347f5fc61494deeb7d8590c6dd8859be548f1af7bee117a6`  
		Last Modified: Tue, 03 Jun 2025 13:37:18 GMT  
		Size: 45.6 MB (45585113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb458c2fb343ac08df2174bebb03229610ede8dd7323589ec018476e303944f`  
		Last Modified: Tue, 03 Jun 2025 13:37:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc4225a392a9d972a86cc8a8f73f5521d7550ea658d20bccae8fed9d8c103df`  
		Last Modified: Tue, 03 Jun 2025 13:37:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfb0e7b8354523251b553a1beb3e18ac1f45b5bc5749b43308cc48b24109ea`  
		Last Modified: Tue, 03 Jun 2025 15:08:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2cdd2ff5e4affa85dc33c1b6d4a626961ed74355df4bbcfef1c9861e8e16d9`  
		Last Modified: Tue, 10 Jun 2025 19:22:11 GMT  
		Size: 13.7 MB (13739511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba3371a0cca252c51fcd8a4114f8509b9f5e27c15245614cebd7364f50afa57`  
		Last Modified: Tue, 10 Jun 2025 19:22:09 GMT  
		Size: 228.6 KB (228640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:522c1db5e4ad281e15bda0ebe0d17bbf3538ed5dbd9f7e50f573486b8d830e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6e5a2a2c039f14ff5934b247f53f0a872501ef8df970961d56ae6878d2274e`

```dockerfile
```

-	Layers:
	-	`sha256:974b88e0395d8addff054ec0cbce3dc6b86415c0c13ca16682d4eaa34273b276`  
		Last Modified: Tue, 10 Jun 2025 20:37:48 GMT  
		Size: 4.0 MB (3950648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b8eca098d5975c82303f219a2743f6da09ae8fb84c371ed9c9db07d18f2657`  
		Last Modified: Tue, 10 Jun 2025 20:37:49 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:9e2c15e3f1d992df464053d72d19fda96a4d43dcf920d645da514e378187f222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108757235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1f6b85c9d64ff7b4e6d6e63b6fab08823279909e0a8c3e3e1132b85457b327`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de0e8a8949ec849c4e2d822052efc995cbfd8901f78e2be800be3fd9735154`  
		Last Modified: Tue, 03 Jun 2025 14:13:03 GMT  
		Size: 17.6 MB (17618370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d820aa9116d6c6b5c08565d3e5c755290a90302e718cdf979940b6524951754`  
		Last Modified: Tue, 03 Jun 2025 15:02:16 GMT  
		Size: 42.7 MB (42676874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ab41ad2f54ec5fa836689ece07252eacaacd73f14c56abd66d01a957a530dd`  
		Last Modified: Tue, 03 Jun 2025 15:02:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82093d74892efae414ec161ba6fdb84ef5509b0189b007ef2642ddaad51737d`  
		Last Modified: Tue, 03 Jun 2025 15:02:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044dc28b0f904a1ee076f65370175b6c536a7936b5da419c3c772a570d2c8dc3`  
		Last Modified: Wed, 04 Jun 2025 11:28:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb650687ee72393bf35af300bad323cf22d0314d9ab3667cac5d25d6df0061`  
		Last Modified: Tue, 10 Jun 2025 18:43:54 GMT  
		Size: 13.8 MB (13759936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00ce83efd32f9c18e057d5368b60d509736b2e7fc4f049dbf79622cfa6947c`  
		Last Modified: Tue, 10 Jun 2025 18:43:52 GMT  
		Size: 259.1 KB (259055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:202b5df9ac2c870e122aa8228c05a249e505530fecfdeb96e6fc24ddb47a3252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2881d6e085268a0581c20451362e4c642f2b4abecc2e609814a0786bda21d0`

```dockerfile
```

-	Layers:
	-	`sha256:065226a41605ae981f90d95a54817c3605026d5589c0da468e98e4e1f6253e61`  
		Last Modified: Tue, 10 Jun 2025 20:37:54 GMT  
		Size: 4.0 MB (3954455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d11dfad923e6aa483077f350205308eefc0e2896cf5228c3ccd2801865aee2`  
		Last Modified: Tue, 10 Jun 2025 20:37:55 GMT  
		Size: 21.3 KB (21308 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:2f72d0ff5a280c345558033b116492c4568b2a940df41b53b93fcab818cd498f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98947352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e612370d26c9480b2036582a887945e9bdeb28f3197b99ebfa4683cb822c66`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7407b9fdf832fa4e3a41a2319aa3e0d04f31104a25092c677a83bf06472d7`  
		Last Modified: Wed, 02 Jul 2025 04:15:41 GMT  
		Size: 16.1 MB (16144420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d44ff17cb22eac99cf00f83bc194e7b7c39ec2691e815b55c5adfd8227202ae`  
		Last Modified: Wed, 02 Jul 2025 04:17:14 GMT  
		Size: 40.8 MB (40839888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bba4298ceb86f772fefc81abe88a15c5f73eb427851ff2ce03aae37b3a788e`  
		Last Modified: Wed, 02 Jul 2025 04:17:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc812aed2ad119cff382a7a654b8d390816bb730c5fcf99361b5735aab3bd8`  
		Last Modified: Wed, 02 Jul 2025 04:17:09 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aeed9e733d1b91afc2a67a9f00337ed7c3896490c15fff3637fc65e1d6db426`  
		Last Modified: Wed, 02 Jul 2025 07:35:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0ddf0ed7edcf293a8afdcdd5b7b1b033f61716199e141a2c80c3bc6e3cd268`  
		Last Modified: Wed, 02 Jul 2025 07:38:13 GMT  
		Size: 13.7 MB (13727405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d3b1013d402a6769d69c490f8601314125a76a64f0e8e0b226b4598701b364`  
		Last Modified: Wed, 02 Jul 2025 07:38:12 GMT  
		Size: 230.8 KB (230823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3c45c1862487adc44022264007b28cf4aaeae213278fea1f84b77a53528f9487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3973214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152d6424682f6af69c02174fbd56e491d885b706c99c715bc5b0178ba2e8a3de`

```dockerfile
```

-	Layers:
	-	`sha256:fde5fec445dae4826f915064302cd3880526bb70dcedda3baf018dcca6483f8f`  
		Last Modified: Wed, 02 Jul 2025 08:37:18 GMT  
		Size: 4.0 MB (3951958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47445db7cd46916e812965c37fbec6711b6e924bf91ada280a99e2f9bcf85b7`  
		Last Modified: Wed, 02 Jul 2025 08:37:18 GMT  
		Size: 21.3 KB (21256 bytes)  
		MIME: application/vnd.in-toto+json
