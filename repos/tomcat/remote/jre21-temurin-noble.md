## `tomcat:jre21-temurin-noble`

```console
$ docker pull tomcat@sha256:46f846df3ff0a5491d537120f2fc3cbb0782ddfcc86f4636768378319e346d16
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

### `tomcat:jre21-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:b02ddf0e9b0c8c826fa16e1c1801e3d7fa29d7d8faef80a921f77cd121d2a731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111629141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60aad3cbf0a23c268341ad065e7363f12b8966eef47cdac7c88e70222901ba1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:36:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:36:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:36:46 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 09 Oct 2024 17:36:46 GMT
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
	-	`sha256:802008e7f7617aa11266de164e757a6c8d7bb57ed4c972cf7e9f519dd0a21708`  
		Last Modified: Fri, 11 Oct 2024 09:51:09 GMT  
		Size: 30.6 MB (30610919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da442b6a7976140ebd8a1198ded145af219e86718e91c0816eb4754dfa915aa`  
		Last Modified: Wed, 16 Oct 2024 02:16:59 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1623e8aa826f0a9a9d285bbeb75efdbde61cfc11cb91d25027ba5349ce6e29d9`  
		Last Modified: Wed, 16 Oct 2024 02:20:36 GMT  
		Size: 53.5 MB (53513794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29dc564edb627b7f7eca4c4eaa2b175d933a101f7fe4686f3578ffd726518f1`  
		Last Modified: Wed, 16 Oct 2024 02:20:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf778e0236b23d70401bd3d012b13e4ddc6ba263daaf04b88a55e4600d542473`  
		Last Modified: Wed, 16 Oct 2024 02:20:29 GMT  
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
	-	`sha256:928e05090e61d9d0806f9922eba855ae70a011d1069b8983f86678e6deb1d093`  
		Last Modified: Wed, 16 Oct 2024 16:52:54 GMT  
		Size: 13.5 MB (13517808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8686269b00826f0dbe9fe0f63c191c8dd3e13a34d58b98567fe29da3185214`  
		Last Modified: Wed, 16 Oct 2024 16:52:54 GMT  
		Size: 212.9 KB (212938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:7d97df1f7b44a6b287cf8f3e73e117e45ae8e2798f2a6b4ebc9f6c313e393546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5f76e5929b93f3b0a46777efdd5ab4702d50df30f33a6d5fb914585de0ac76`

```dockerfile
```

-	Layers:
	-	`sha256:9cb03ca5b67993f70efacc99f06c8dd457d83e772a9ed9bf292f5be8e0d590d9`  
		Last Modified: Wed, 16 Oct 2024 16:52:54 GMT  
		Size: 3.1 MB (3054379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd3d1e5ca789606780f513f7cafe4eccb5151288cc7c5a26491c0540f1253f0`  
		Last Modified: Wed, 16 Oct 2024 16:52:54 GMT  
		Size: 24.6 KB (24600 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:991df74c9c5da5dcb74049eda9e450b90520fc6d57e266476a649aa0d6ccf8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110129186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2451f9a98c43bb9941e02e7949e3b7722f4f271b2ea9f0e0164cc9a9f5db8221`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:36:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:36:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:36:46 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 09 Oct 2024 17:36:46 GMT
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
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69586b06510b52d48a683ba572c57200b83ed124f6a47bda743a95ce1b7c1de`  
		Last Modified: Wed, 16 Oct 2024 01:19:09 GMT  
		Size: 52.6 MB (52641546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4083ee0ee102fcbdfad3d9bd53251f8108e08f4623d276456a3b8e84b76df6fe`  
		Last Modified: Wed, 16 Oct 2024 01:19:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75f560b5b1a6738b5dbe5a4574ed5c5a933ea3c15a87af3bb1e5becb9694854`  
		Last Modified: Wed, 16 Oct 2024 01:19:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762c41a28e5a6e05dbf03d46f54ac692c428163b904f8207d4c5c39338720e4a`  
		Last Modified: Wed, 16 Oct 2024 07:39:04 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccb469c440d28efaf0e516b592138316e8b173daac330ca698530ed059d6778`  
		Last Modified: Wed, 16 Oct 2024 07:39:05 GMT  
		Size: 13.5 MB (13521060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1907c838d9d51a516eaf4b0a1e28090eeb8a303f97dae46143f329ac8ecf91de`  
		Last Modified: Wed, 16 Oct 2024 07:39:05 GMT  
		Size: 212.7 KB (212738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:1cf9cfea4289a951bc1b3274f8c204902d39b832deb2317391a4aeed0605d6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3079814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea332c4e34aab122d72bb22a0b1fba06fd7c7917f990dae7862ab618b12607b`

```dockerfile
```

-	Layers:
	-	`sha256:60d60d2332b2b40296f24f75d753628008318f633a6e7faaedbebc95c4eb6ccd`  
		Last Modified: Wed, 16 Oct 2024 07:39:05 GMT  
		Size: 3.1 MB (3054942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6059cc63d83468201124f1fcb82734437867466a36c23a78731fd95698200c34`  
		Last Modified: Wed, 16 Oct 2024 07:39:04 GMT  
		Size: 24.9 KB (24872 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:a9245dbbdbcb24e5ff8bdc5809787ba50d0b6bb4546cd3be87116c661b65e6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117780368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519347bdb71ba7180b2b0adab9e6220656e9728a39ac776f8af17668dbf91dd0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:36:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:36:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:36:46 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 09 Oct 2024 17:36:46 GMT
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
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2821b1345206fcb4dc812596cd95469ddd38c966efca097a8d6bba9b94dbb`  
		Last Modified: Wed, 16 Oct 2024 01:44:24 GMT  
		Size: 14.9 MB (14914194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8d79d3f532de1f955fbb25e3897a99fc18c6750911b3384fdbde6e0c8ef72a`  
		Last Modified: Wed, 16 Oct 2024 01:48:21 GMT  
		Size: 53.6 MB (53573730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc4e8f317b09d3bdfb4135d5786ea631d2b41caf9179de1df8b9f7a741cbcf`  
		Last Modified: Wed, 16 Oct 2024 01:48:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f847f72c61ce27548f040b94a17303f4fcde38688c3fffb919d3b7ca7d371ea1`  
		Last Modified: Wed, 16 Oct 2024 01:48:12 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459e285d59e36e0727d7d07506abafc26269e24670308001b85df64545e6907`  
		Last Modified: Wed, 16 Oct 2024 07:24:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1e1ebad004652dda134981da67c3f1e6c33519b275c6740eeb7bb231cb7b2e`  
		Last Modified: Wed, 16 Oct 2024 07:24:54 GMT  
		Size: 13.5 MB (13535046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa20689223e8a45a2e272cadd567976903d401848f19b05f3b8a5bc7ccdc9a5c`  
		Last Modified: Wed, 16 Oct 2024 07:24:54 GMT  
		Size: 243.8 KB (243791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:61e22629e78aa6d4a8e0b27834f24a46ba62a7f380a2bd4e6eac16273e533039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7540c7a7c7de49d7a8a21b8cc062ea27a35a9ddab60ab7854d7a04ca7a0ed51`

```dockerfile
```

-	Layers:
	-	`sha256:3a8526e63b22a84ed410ed170c87c90203ca69ec9035f184733dd83ddf2aaaf8`  
		Last Modified: Wed, 16 Oct 2024 07:24:53 GMT  
		Size: 3.1 MB (3058332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e6b64176f1b0328c1cc36702e69faf691635c12fa817297cf8422d035b8f3e`  
		Last Modified: Wed, 16 Oct 2024 07:24:53 GMT  
		Size: 24.7 KB (24724 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:3ac97764f8109584a438222e6616764b46f0e40a07a81d438ee14406963ff099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108275478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f3072e5cece8cbdaad6749a8d2fa973e5f6f4f6e76fd48f5b0c138823d0470`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:36:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:36:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:36:46 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:36:46 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 09 Oct 2024 17:36:46 GMT
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
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4154e706a872d69678b9815a958201c73822602cf188b0f18fdec44d1c455483`  
		Last Modified: Wed, 16 Oct 2024 01:26:30 GMT  
		Size: 14.2 MB (14195095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe17b323fcec9773b4d01115ddb92ac324f8af67a7b3f6f39bf3f1c7b40f223`  
		Last Modified: Wed, 16 Oct 2024 01:28:46 GMT  
		Size: 49.7 MB (49669769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aace9528441236c85669e95a2ed19865f267f32508c34af2c122b08572b62e0b`  
		Last Modified: Wed, 16 Oct 2024 01:28:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7b57db0400f99e8ad64ad2ab79de4245fd3bc100c79130e66181a17e4e8d4e`  
		Last Modified: Wed, 16 Oct 2024 01:28:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b20512bfa231589e6f864574171752a73d08dfebb5293eb3202934f130d176`  
		Last Modified: Wed, 16 Oct 2024 03:00:38 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb73782a0ff1b92dda9ca769f41686aa5d79a9e4bd398eb68057f8294dfa2802`  
		Last Modified: Wed, 16 Oct 2024 03:00:39 GMT  
		Size: 13.5 MB (13526154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c655197b2cd7a6eced3ef0016e22fc99fe09996b358b08389044eecdacd8c16`  
		Last Modified: Wed, 16 Oct 2024 03:00:39 GMT  
		Size: 220.4 KB (220385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:28efb5317438d8e9cdf175efb0f2e755739b3fc661d299833701168676a0fe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3081210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a924fab879cee3a60632c6e5b1ec98cccb6584254a317760870310f2fe380b`

```dockerfile
```

-	Layers:
	-	`sha256:0b3ffec72617fec91aad2511048fe2a7072b2f638fde766a5286a83bf171a9f5`  
		Last Modified: Wed, 16 Oct 2024 03:00:38 GMT  
		Size: 3.1 MB (3056586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a416b74f282b01ae2e67b975f9b133aa7c17f29c72d5a03a615cb5339200869a`  
		Last Modified: Wed, 16 Oct 2024 03:00:38 GMT  
		Size: 24.6 KB (24624 bytes)  
		MIME: application/vnd.in-toto+json
