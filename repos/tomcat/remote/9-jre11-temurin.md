## `tomcat:9-jre11-temurin`

```console
$ docker pull tomcat@sha256:8635e0738d7cce890bd4acfc1a56cb0c151d2514cb1bec86e9bc5ed98abb2bc0
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

### `tomcat:9-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:bf23f2dffde0c1b6ef6eaba95e05f531a3a6f274c5234d10126d73b092db18b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105173863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11b91b84a34b955f4cec13d8213dffdaf8658d02c30ca94158ab97f5c9325c5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Sep 2024 14:16:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:16:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 17 Sep 2024 14:16:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:16:43 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2b658c0415582a9e1e9e5e778b5a30dcef669f8cfb52328d877f5119fa975`  
		Last Modified: Wed, 02 Oct 2024 02:20:50 GMT  
		Size: 13.8 MB (13770567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa9eed7cb1fe73fb7fb80a2a223e66dbe321a263f737758e89dc3bdaf42c569`  
		Last Modified: Wed, 02 Oct 2024 02:22:31 GMT  
		Size: 47.2 MB (47198919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2358c19bd1bfa6f9d7cab7b84976adefed241e2d412033ac048da74c7460b80d`  
		Last Modified: Wed, 02 Oct 2024 02:22:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34572a6f166dfe595c46b9f16dc601b0ad136e1cc665f45c0a739a36c17be8e3`  
		Last Modified: Wed, 02 Oct 2024 02:22:25 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47d960ef7063e3a2f43dbc44dfc76155f60004b9950d188b9de54de6bd6d7b1`  
		Last Modified: Wed, 02 Oct 2024 03:57:07 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf1de557439424364d4d44b1a5a15af8c113e8ae3ab3a7adeb18ac0b0f60d27`  
		Last Modified: Wed, 02 Oct 2024 03:57:08 GMT  
		Size: 13.4 MB (13377983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df312f74014eb3c8547645e9fb9742e15dd12cd0cc56680a8d0b53dbc66c5405`  
		Last Modified: Wed, 02 Oct 2024 03:57:07 GMT  
		Size: 212.4 KB (212445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:24507b1f9be6a3db0a1b21625cdddff007ec77845d5160b809c7ab63ae32c7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3084698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74082a1e5f4310e5793f03f7c4f4a670d813e936e8c5850f0ee7689456d3ffbf`

```dockerfile
```

-	Layers:
	-	`sha256:af3dfd19d7370c9f09d93b65a04187620013a37c921bbd3cf8518463653c2dba`  
		Last Modified: Wed, 02 Oct 2024 03:57:07 GMT  
		Size: 3.1 MB (3060936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:884e401f82efa1f0219779400a12a2a59fcab95abd4012c4db3d98bc1c578a47`  
		Last Modified: Wed, 02 Oct 2024 03:57:07 GMT  
		Size: 23.8 KB (23762 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:b736839472221e5c3d8e4ee76c4ad90b257d60c9b229e983d08164b0955ec0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99686832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b15f89818876129bcb4704f7b317673c7a145cb95236e1afe4757c383fc4372`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Sep 2024 14:16:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:16:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 17 Sep 2024 14:16:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:16:43 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5afde08068e6888b550cae3a7ffda1ff056862f0e466bdb789146e4038eea`  
		Last Modified: Wed, 02 Oct 2024 01:50:03 GMT  
		Size: 13.1 MB (13134649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd715c1710ea2cd7a74f1be42f111695e5a758e07f0a3cf19e76f0368c1d4fdd`  
		Last Modified: Wed, 02 Oct 2024 01:51:47 GMT  
		Size: 45.3 MB (45320681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe97a0e03633bbb1baec1ef018b82d566bc7a10a09360f32651256061502709`  
		Last Modified: Wed, 02 Oct 2024 01:51:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f460145935b2268e43e20ac82b1dc159fe00310e7a55b22db961eae66e61f56`  
		Last Modified: Wed, 02 Oct 2024 01:51:40 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b203b3457d32d2b200537642c7f016ced0928503609ca5bbff135566a774b3b2`  
		Last Modified: Wed, 02 Oct 2024 05:35:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01508b3d987c12f70016ca219d9e703d65842931ded4bbdc4387bf3e637f1218`  
		Last Modified: Wed, 02 Oct 2024 05:36:28 GMT  
		Size: 13.3 MB (13313688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ca704ee310e32e71c2ff720b6b4d039c060e19d331c61c8063781fcb79c1c8`  
		Last Modified: Wed, 02 Oct 2024 05:36:27 GMT  
		Size: 183.5 KB (183500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:e9b3556abaf73632172c7d62faf3a2c0a5c5a13118efca342ab64d8e03c29147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273a704fa0c15b794f352b7f6afb635e6eed193d4dd46a7ea87ea95d653a3eb3`

```dockerfile
```

-	Layers:
	-	`sha256:67a9fda38c3c2f208822f5ba475a6c2d2e19803a74f91aa0e58d0f1088b2863b`  
		Last Modified: Wed, 02 Oct 2024 05:36:27 GMT  
		Size: 3.1 MB (3064568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6bea10fd80b2ca5650b9b35ddd27b9a9cda490ba289dac0ab5ccfeee76d7b4`  
		Last Modified: Wed, 02 Oct 2024 05:36:27 GMT  
		Size: 23.9 KB (23938 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:516d3482f23d7acd4376bd683962acc881b4ac1d189eac94f863b895afad978b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102909590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f61e00dae941ee791b08011983dd57d36d1466e6ca4950e73fa5bbdee100b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Sep 2024 14:16:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:16:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 17 Sep 2024 14:16:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:16:43 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a1f6703825bc1ab890a74dbcf6461f732a29cb694c6d7c8c6ad9977ab58df`  
		Last Modified: Wed, 02 Oct 2024 01:26:57 GMT  
		Size: 45.6 MB (45557310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ff191c9dd4f08b1ad924a59b3c126887f036a38c7bad1aae8e12272bbbf93`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85053618bd30c13b6f45f967fb5b27aa26228d70e12cee43591fce42647d7417`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897552c0959b1fa28e1cc35ca8b483095b168b407a946de2bdaf9a2a2d0091a7`  
		Last Modified: Wed, 02 Oct 2024 07:18:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cab23e461e81db6fb4ce5be8caf92e4b75c552207ae14f06b41e7c51527a1ce`  
		Last Modified: Wed, 02 Oct 2024 07:19:36 GMT  
		Size: 13.4 MB (13386785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5290242d0ee3afba4b03d331704aac21abe2b38a15d94ec0cc5078e9f0e9f122`  
		Last Modified: Wed, 02 Oct 2024 07:19:35 GMT  
		Size: 212.3 KB (212286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:5a97769802d3cf66080e521fd0c6e599ba5bb6d6a25d85612cd8daa0ad39f293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3086076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4134c393c55aa53cb57cd66b3421224a778c7e2554cb265094edd7113d22be3`

```dockerfile
```

-	Layers:
	-	`sha256:85e4691dbd989706419f640d4ca6cd60956b80ed12006e6f7f4c87c66d2395dd`  
		Last Modified: Wed, 02 Oct 2024 07:19:35 GMT  
		Size: 3.1 MB (3062082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9684fb24111ab5063e99771f64790db3a676f07b6928d5a81b69c98b8d781a29`  
		Last Modified: Wed, 02 Oct 2024 07:19:35 GMT  
		Size: 24.0 KB (23994 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:9814ee644ed01ef18e3941543758f71062f17ecea2170f06df658cdd456406c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106741575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6470387fd2b50a61304a3c42454b500a28e7cb1afc7661e7e4ef75f1d1203e23`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Sep 2024 14:16:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:16:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 17 Sep 2024 14:16:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:16:43 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8142fb4132be3efdcf8ea435bb4f9c7886f7dd7050b7ff796718a886a738003`  
		Last Modified: Wed, 02 Oct 2024 02:05:51 GMT  
		Size: 14.9 MB (14913665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdd4ba783d4fcd23afa4a18ec10b060bda844bd6e79c1f1a51b1a1950d4c6dc`  
		Last Modified: Wed, 02 Oct 2024 02:07:52 GMT  
		Size: 42.7 MB (42652117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72e859160f0bffee207c987ad388adbee9a4be9ca250e73036e8320e3eda57c`  
		Last Modified: Wed, 02 Oct 2024 02:07:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba745757ab3007572fea0eed148ef3468204f11691a479a4acba80f55246240`  
		Last Modified: Wed, 02 Oct 2024 02:07:45 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563dcaecdf56ac2a2d5662d61bb3252d647e1f8e8460aea5f5005714555ddca2`  
		Last Modified: Wed, 02 Oct 2024 08:19:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cb177be6e0232516920a5b44a6197a1e7afbc58457d92ec880955f8f7220c8`  
		Last Modified: Wed, 02 Oct 2024 08:21:05 GMT  
		Size: 13.4 MB (13411894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dad4af795e152b2b99e4c060afd32bbe82eeec392497ca43ce9d908af159a18`  
		Last Modified: Wed, 02 Oct 2024 08:21:04 GMT  
		Size: 243.5 KB (243505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:e6b912cf7ce65fb6b932843f940c09ca9e56159d5364d30daeddb1031303515c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f16312a302de204c12283f69a2f86b7605b8c39b6c9f1e896211e1aa81a172`

```dockerfile
```

-	Layers:
	-	`sha256:e8a679df895467f4e8c620c6796e4f1300186d2b07733e97d1a60e66570bd243`  
		Last Modified: Wed, 02 Oct 2024 08:21:04 GMT  
		Size: 3.1 MB (3064877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eb12d29f550097c13c63c378cd7c18c033df56eae20024709cfda1ddb6ec5a6`  
		Last Modified: Wed, 02 Oct 2024 08:21:03 GMT  
		Size: 23.9 KB (23862 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:35ab4de16b0e2debf2219e5cb855ae3b9869cddee1fe5a09b653a54045e5597b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99289114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f5bf9823315d03430ee233837718514f73b9ed96eddfc7f353597fbf5f494`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Sep 2024 14:16:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:16:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 17 Sep 2024 14:16:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:16:43 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a6e9212f8934753e011511ba4cde1df5296a5eb6cc208e49c877430107e44f`  
		Last Modified: Wed, 02 Oct 2024 01:22:01 GMT  
		Size: 14.2 MB (14195040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5331cdc956c4066a0feedc740b02b16f00be6b0660da86d3d8f3b2f557e25fa2`  
		Last Modified: Wed, 02 Oct 2024 01:22:41 GMT  
		Size: 40.8 MB (40817523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc3f26f4f121d2c6a1b3c90f478929aea1aa99399830b78b1289f46154dbedb`  
		Last Modified: Wed, 02 Oct 2024 01:22:35 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736bc78c2c8b1876c291ea35e4cea7781653f156eacd1f12f202b4579e0fe33`  
		Last Modified: Wed, 02 Oct 2024 01:22:35 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c238d816dfe0280f15cc5089e810fa77ef8a1ee3cd61ead9f51101bb44421226`  
		Last Modified: Wed, 02 Oct 2024 03:21:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c69ab4d3b446a923ded7ff2197c382af434a3fec2ddada63b78abb01dee1ed`  
		Last Modified: Wed, 02 Oct 2024 03:24:38 GMT  
		Size: 13.4 MB (13388236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1c3d1ab8cae5c72bfc609f46a369e6e184b48c14082606ec073f2125009082`  
		Last Modified: Wed, 02 Oct 2024 03:24:37 GMT  
		Size: 220.4 KB (220401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:720a24d19617078675a519c26dae744559a1c31e7257009c64b0be0dacc6b4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3086929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26729bd17be04b5f2ea7d2113dfedf14c7c148705a1f9ce77270c69cc1f1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:860012e59319300560be0a8141c30f274d479f30ab218ec16f80d14c82768fbf`  
		Last Modified: Wed, 02 Oct 2024 03:24:37 GMT  
		Size: 3.1 MB (3063149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cdef8c0475e2abfc174ffae7dceb12a264733e357588efcde7f77ae46b87c1f`  
		Last Modified: Wed, 02 Oct 2024 03:24:37 GMT  
		Size: 23.8 KB (23780 bytes)  
		MIME: application/vnd.in-toto+json
