## `tomcat:10-jre11-temurin`

```console
$ docker pull tomcat@sha256:d2acc51f06dc30f809db0f4f69a61293cb08def7bf2941e59145e4c74923bca7
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

### `tomcat:10-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:cea8f3519b266a3618543b63e72aaa2562a5da1dd250dc5742222d4ab4346fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105353609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4170483b5b0e80094ff55abe5b629ad039cf3e49c2e7729b2e43c611b8101`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 09 Oct 2024 17:25:06 GMT
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
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:802008e7f7617aa11266de164e757a6c8d7bb57ed4c972cf7e9f519dd0a21708`  
		Last Modified: Fri, 11 Oct 2024 09:51:09 GMT  
		Size: 30.6 MB (30610919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da442b6a7976140ebd8a1198ded145af219e86718e91c0816eb4754dfa915aa`  
		Last Modified: Wed, 16 Oct 2024 02:16:59 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada76ce4a6f427d64a42908d3db2ef1966de69b6343835ce80d8545336c5f8e8`  
		Last Modified: Wed, 16 Oct 2024 02:18:44 GMT  
		Size: 47.2 MB (47199066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400fc196bca450ba217d511355482eab9da2ee72ac0721df243981af451a8858`  
		Last Modified: Wed, 16 Oct 2024 02:18:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c6243d5fa53f13b9953b3ab873a976576dd843344f4f5676ded16be17540f`  
		Last Modified: Wed, 16 Oct 2024 02:18:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b06ed83030bf174a4b23750d023806576fee5fe1d3f64f10f710ba56d2ed0f7`  
		Last Modified: Wed, 16 Oct 2024 16:52:54 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15162de741f0be14b9b07a277ca8a61ae9fdf55cffe370e3946d861a7a5a0e1`  
		Last Modified: Wed, 16 Oct 2024 16:52:55 GMT  
		Size: 13.6 MB (13557040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603e3f9321fd794fc8c2119cbf23a30100c11bf1a32943d544251a4c7808005c`  
		Last Modified: Wed, 16 Oct 2024 16:52:55 GMT  
		Size: 212.9 KB (212902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:b0d419c91e650dfd0b7c296d34e74fdbac6e28006bf099091cc2811bb50aa15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089b75c5d0ea19b61f18e93dbfab0fbf34c4f86dfdeb0d735bb72e8fb3fce748`

```dockerfile
```

-	Layers:
	-	`sha256:b160b9518e93f9267f351bd33e4da0cd86843865f5abea1a7f677b14f2df0dbd`  
		Last Modified: Wed, 16 Oct 2024 16:52:55 GMT  
		Size: 3.1 MB (3064150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60aecce28ee777aec32c2a2d64d9b3ae4d8113fe0b34b4318ec1dd4f166d11af`  
		Last Modified: Wed, 16 Oct 2024 16:52:55 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:942bf5ff1117ad60f5a23143931ab3cd9aec7fa32c469ad512ac25c5e79d9e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99908311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc3b91c8b99046be6b11586993484487d77f505f60df064ef93e2afa8df226a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Wed, 09 Oct 2024 17:25:06 GMT
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
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249e0f259e41b9eabe172538e41f6fdd2856d872ba698b9d718ebdc1e63a1f0f`  
		Last Modified: Wed, 16 Oct 2024 01:33:46 GMT  
		Size: 13.1 MB (13135129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4ace103975751c79b3a457ae7244fc7b4fc92fa556b59bed8ffc9bdf4edd79`  
		Last Modified: Wed, 16 Oct 2024 01:35:34 GMT  
		Size: 45.3 MB (45320377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbadb334c6ffd5aa8164a7a4dbc9ec7c4a130294b81cfbb026d7598034469d5`  
		Last Modified: Wed, 16 Oct 2024 01:35:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca845324dbe623eed1e8eae91a314f7d91a99d9609d3a023c7f7aec18c059c74`  
		Last Modified: Wed, 16 Oct 2024 01:35:27 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46e036ba05a4786ddd914f517d59af467724d1453b69a8e4c9ea69720a0ccf`  
		Last Modified: Wed, 16 Oct 2024 03:24:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b76ef063ed68e36c6fbe91703055eec91eae56614102f22c974059716b4016a`  
		Last Modified: Wed, 16 Oct 2024 03:24:18 GMT  
		Size: 13.5 MB (13531713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933eb436ae85c818f2a9a21db557b75850d673560af4f958f60c2b72f5ecfbd`  
		Last Modified: Wed, 16 Oct 2024 03:24:18 GMT  
		Size: 183.8 KB (183819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:7c2863bb76bb897f96f1caf1359da1ef24f7271ae5d70205d5cc81cd053da99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d22b570a851fedbf2db927509a79d7df9c908b4cda0b08563a71ec50051d05a`

```dockerfile
```

-	Layers:
	-	`sha256:230d1829315dd420a3be4b245fef7cccc96b801d8a12162cd05e6b72c6a7eeef`  
		Last Modified: Wed, 16 Oct 2024 03:24:17 GMT  
		Size: 3.1 MB (3067782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a18e85fbd6798b8706c6497b63498b2550fc1da3e3b928c6207ce7062147139`  
		Last Modified: Wed, 16 Oct 2024 03:24:16 GMT  
		Size: 23.9 KB (23865 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:23865dfeb1609c9c360af0b8e84fe05f588ace35f3e2bf12606c4eaccb0271fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103083425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bfee1b5d0117ff304e3a8b217f1dd67e8efdf10641bca19ed57b664566832`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 09 Oct 2024 17:25:06 GMT
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
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf81e66fa50a74466657a4cd87ecbb55a60193bc2fd0d891a8cfee51b5d007e`  
		Last Modified: Wed, 16 Oct 2024 01:17:24 GMT  
		Size: 45.6 MB (45557334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954d8582d92e1ba2f3cd51b22cf7b3a63a34f350d1db2286d2681db0970f0f1`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d55cecd5117dfdb0d0cb27bfa425c664e190b08c8ca3ccb82fcee60d1fd4e`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1291a3efe0fb63d85dc8cc8c1cf60f624fc1d1734be78bc6b09829573601a285`  
		Last Modified: Wed, 16 Oct 2024 07:40:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaef7392850f91c2e461064fa966dd22b70690a86ab211addd00ab8a6b2f18b0`  
		Last Modified: Wed, 16 Oct 2024 07:40:34 GMT  
		Size: 13.6 MB (13559509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eca2e7487621e6bf871e0e45d83d6ba6f51d762616ee329732bf8378252a39`  
		Last Modified: Wed, 16 Oct 2024 07:40:33 GMT  
		Size: 212.7 KB (212741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:0f6747acf951bf08f15952f91ca63229fcbd80fdace693810289b67fb9d4126a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339e9032cd31b551c8c8b6a67484ef4eea74e472c531b75f33744d293b7d1423`

```dockerfile
```

-	Layers:
	-	`sha256:ebbb84277ac81fa8eb534b990f24d7bde89203cbdd1ec802285637959ebfb25f`  
		Last Modified: Wed, 16 Oct 2024 07:40:33 GMT  
		Size: 3.1 MB (3065296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654ee3ff6e5bcb88421c7ff619ef8b92a47d0e280085103a6b9fa9e149a4a135`  
		Last Modified: Wed, 16 Oct 2024 07:40:33 GMT  
		Size: 23.9 KB (23922 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:11dde209b318415318f8ba3154e2788aa49ae2ecbeeaa7303e799ff9b218f0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106893835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16531bc99d71e7de7e48d25d2cd36f75f2b73dfc40656f57fd7e37e385a3b6dd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 09 Oct 2024 17:25:06 GMT
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
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2821b1345206fcb4dc812596cd95469ddd38c966efca097a8d6bba9b94dbb`  
		Last Modified: Wed, 16 Oct 2024 01:44:24 GMT  
		Size: 14.9 MB (14914194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d9db5890aab0419e4b31bf7851afc860bec63ced53f08296d38a7e79f4dbcd`  
		Last Modified: Wed, 16 Oct 2024 01:46:16 GMT  
		Size: 42.7 MB (42651948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cfab88f9296d2e6b82bd7c1709122c8846318c3085ccf87fb7a36b1f46cc5`  
		Last Modified: Wed, 16 Oct 2024 01:46:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def6fbc39bffd1c7707c92f0a36850f2bd9421714e67dbd54c5b1738180af3b9`  
		Last Modified: Wed, 16 Oct 2024 01:46:10 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcf0fce90e4ad710794325b901f95da3295d7c1e3ea487f92c5d4218187dd77`  
		Last Modified: Wed, 16 Oct 2024 07:52:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2374664ef489bbbcc25b010408cc43ed91f347f08cb5181e918a90958713af2a`  
		Last Modified: Wed, 16 Oct 2024 07:52:51 GMT  
		Size: 13.6 MB (13570242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3259ee24f20b2706186c188492d3460ff5f7ef8e78bdf6ee7eb82a226386d09`  
		Last Modified: Wed, 16 Oct 2024 07:52:51 GMT  
		Size: 243.8 KB (243846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:cbf7b16db385461c9d2448a8743b4130509cec2a2d317025b8c9b6b727968763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a415ca04eb4c81a0d86d526a1a4cf6a9761d1af9fe38826869f782c7fd2de1`

```dockerfile
```

-	Layers:
	-	`sha256:c6b00cb8aa6e38c7e6ae50398b96bf04dbfb9f87df4cc0db975e7e2e3551c172`  
		Last Modified: Wed, 16 Oct 2024 07:52:50 GMT  
		Size: 3.1 MB (3068091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54a534496a83467080d78605b351e15b71ae052305bdc0231817228c96e71ac`  
		Last Modified: Wed, 16 Oct 2024 07:52:49 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:e4486e030be664756c4055ed338cab468f944c6d7ab04d62731b921c2ecdd02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99464648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098bbb9b25ca8ab3bde5de628dc457ff6110e0bcf0196a605234b17e67734bb8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 09 Oct 2024 17:25:06 GMT
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
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4154e706a872d69678b9815a958201c73822602cf188b0f18fdec44d1c455483`  
		Last Modified: Wed, 16 Oct 2024 01:26:30 GMT  
		Size: 14.2 MB (14195095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83068151c16ed981250fecef8c2ffa838079358656cbd0ebff15c714faac1c0`  
		Last Modified: Wed, 16 Oct 2024 01:27:04 GMT  
		Size: 40.8 MB (40817319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc92f6719c42a2950327208d54dbb6a16c426eb906d7e672e8a924adc2626550`  
		Last Modified: Wed, 16 Oct 2024 01:26:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4106a603b77acc81c6ac3f034f2e4d4ad8f6a47ef0e1149063441aaf45a27e1`  
		Last Modified: Wed, 16 Oct 2024 01:26:59 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1732e362c3e42608763fa57a730d271cd6a764d4f78d3d2835d153beb6a8bc2b`  
		Last Modified: Wed, 16 Oct 2024 03:02:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaa97778554f9f22fd9fc37ff2aa3e3f912571f1e22ac2330c0d214ace4daca`  
		Last Modified: Wed, 16 Oct 2024 03:02:50 GMT  
		Size: 13.6 MB (13567756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047beb26b3d0ef23d8c08bfd65c6cad9194625efb5d23bcea4d345df7b5ddc0c`  
		Last Modified: Wed, 16 Oct 2024 03:02:50 GMT  
		Size: 220.4 KB (220402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:fb4456ff28c8b6043f457866f5e468e930738915ec99f156541644e58372dc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c09a95641b541ce75e39f3c602df92a1218e58160ad06b25ffadddcd49efc8`

```dockerfile
```

-	Layers:
	-	`sha256:5ffa73e39f125da1e20d2c1955eae22ff7b316ac92c865c9e5f0a28fb3c9e566`  
		Last Modified: Wed, 16 Oct 2024 03:02:49 GMT  
		Size: 3.1 MB (3066363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afc3b1be1294e3720de9e2a96b797ffdabca4fa4184ac416ef3e2da67cf4c61`  
		Last Modified: Wed, 16 Oct 2024 03:02:49 GMT  
		Size: 23.7 KB (23708 bytes)  
		MIME: application/vnd.in-toto+json
