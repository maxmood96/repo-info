## `cassandra:latest`

```console
$ docker pull cassandra@sha256:0ce1e13b45d1f0206b7fa0af9d6e1d5588caaa57f4ddc70c9fbc474b80a1902f
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

### `cassandra:latest` - linux; amd64

```console
$ docker pull cassandra@sha256:2f70c5a39f50fa092328dbbfda995f0442e8840aab9805f4131ccbb44f55fbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174619394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b032693265cb56ef0d123bea783d24f53fc92a09a7f7a16ffb34ef22e3f64903`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 05 Sep 2024 20:24:30 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 20:24:30 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_VERSION=5.0.0
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_SHA512=cf91d9a5fe370a3b7eab9447852c491de1c17aca5a71c5ff06a672d210f8d6500d973f2d1827250b071ab5e7d6d5d58c0e79dcef5b134913b4a610674d6ae7ed
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
VOLUME [/var/lib/cassandra]
# Thu, 05 Sep 2024 20:24:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 20:24:30 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 05 Sep 2024 20:24:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161e45ecd8d096f978edcb483c5ed70580526e02a1f8155653ca1c6c192f097`  
		Last Modified: Fri, 23 Aug 2024 19:27:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd5828763dc50dc5ea1bbeecc1f9a67b7489a411457edd8501f2e9d346966f6`  
		Last Modified: Fri, 06 Sep 2024 01:01:07 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25b94078fd8a713b56939e1ea90b3e08154a199005fa202b0cbf2afcb58628`  
		Last Modified: Fri, 06 Sep 2024 01:01:08 GMT  
		Size: 12.4 MB (12407384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc85036be93785767256bbb6e12148377e2b8625e96eb792b24a08ac479fee7e`  
		Last Modified: Fri, 06 Sep 2024 01:01:08 GMT  
		Size: 1.1 MB (1097784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29830e298f6038acde148ef8a4c7583ec8c84bb0dde6edb896cf9ac9cc99cd8`  
		Last Modified: Fri, 06 Sep 2024 01:01:08 GMT  
		Size: 70.5 MB (70517205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1030340eb86a0d0a8bb07b8389909a02237a2011f39669617ab4e7737bf685a`  
		Last Modified: Fri, 06 Sep 2024 01:01:08 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:a56c381f2844feb51fe863dc06d4426061326b2f34f5b2511536e5f508121209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4263843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbe096f021087352070f770ce6e45e99636bf625f840e1a8015f13ad6d7553e`

```dockerfile
```

-	Layers:
	-	`sha256:479b9d9f1f1d81de6b65c83d8bde33a87f81cb1c75232d5effcf2f9ffc9ec7c2`  
		Last Modified: Fri, 06 Sep 2024 01:01:07 GMT  
		Size: 4.2 MB (4228005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935d1d9abdd3bdceff20b7526b6b10fc9e3aedf2c3181eeae64cb109189dac93`  
		Last Modified: Fri, 06 Sep 2024 01:01:07 GMT  
		Size: 35.8 KB (35838 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:833b8b85eb14d5f5f35c1979394b6a34db47241f2f6dde4f5dd8aeeb463baabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148433597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b1f20e10ae2c01acffa56da78b4f0aaac2b42e455e4702e2d518fbd1762462`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 14:24:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 14:24:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 14:24:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENV GOSU_VERSION=1.17
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 19 Aug 2024 14:24:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 14:24:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_VERSION=4.1.6
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_SHA512=3bae2a75aefc139ceaa9beb4709f9ee533517937ae292aba0102788cbf08f94f503c707124beaf06e28eca20dacf00a729da326c178bda432adfac2cd32b91c6
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
VOLUME [/var/lib/cassandra]
# Mon, 19 Aug 2024 14:24:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Aug 2024 14:24:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 19 Aug 2024 14:24:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b092dd5a78dc4cf071309a2972d23807d1b19451ad8ff7aae557e8af16e175a`  
		Last Modified: Sat, 17 Aug 2024 01:35:54 GMT  
		Size: 12.5 MB (12463290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85c47667fa215653013d654ba494068ce4964a9aefb516d812fe43458330206`  
		Last Modified: Sat, 17 Aug 2024 01:37:59 GMT  
		Size: 45.3 MB (45320000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c617fb6e3beb3d3663a933cd60734199e75a66df29790942f2c3439f7cb512`  
		Last Modified: Sat, 17 Aug 2024 01:37:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d005f41915d0d38af212575f14ace6152891778b5d92b40b555cc006cd9b0936`  
		Last Modified: Fri, 23 Aug 2024 19:00:00 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41be35d86371e349d57223bf6f40aa17c3e06382a47e8d791d4b95aa991f74c0`  
		Last Modified: Fri, 23 Aug 2024 20:03:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc80748d37f1725960c7b497a1256065dbb8f2ceabcf0aac5143dff48c74f3e`  
		Last Modified: Fri, 23 Aug 2024 20:03:24 GMT  
		Size: 11.5 MB (11477667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b99f09bf2229d8048dc91ac10a570bbf056baf2841d43223e3706afa3b7b0cd`  
		Last Modified: Fri, 23 Aug 2024 20:03:23 GMT  
		Size: 1.1 MB (1064645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35622c68c8a83737c31c5f571dd2669ed00cf351046f7e19f22eb088b2eac55`  
		Last Modified: Fri, 23 Aug 2024 20:03:26 GMT  
		Size: 50.6 MB (50567727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596b8cc6c0b8db6c2254976cbf29ac6456c5444cf761fbcdb29209fabe74c6ee`  
		Last Modified: Fri, 23 Aug 2024 20:03:24 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:b8562406968cbc833ff68ad1c7df136ad94b09d9a6155b8c2cd5216f83d02173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a42059573f4c95dda27dd5588e2168bfc4e54505d905966792926d5e1c5efb5`

```dockerfile
```

-	Layers:
	-	`sha256:a0a5d8ad52af904f487992a26616f84e167f511ada69f2f319d2402e61a57fc4`  
		Last Modified: Fri, 23 Aug 2024 20:03:23 GMT  
		Size: 4.2 MB (4192532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef8e6a78052ba39ec5878e9a0ab4ffd8976a8bdc2835187d4cd7260126bcf6a`  
		Last Modified: Fri, 23 Aug 2024 20:03:23 GMT  
		Size: 36.0 KB (35979 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:fdee44211b9a16f071d70e0fd0ca32bf57e5907eb587cf7e531a5e03696e66c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171888942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102fb1fd7a694b304236e3b6623f15503a2a6522c6c176cc0fc1a76d340f471f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 05 Sep 2024 20:24:30 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 20:24:30 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_VERSION=5.0.0
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_SHA512=cf91d9a5fe370a3b7eab9447852c491de1c17aca5a71c5ff06a672d210f8d6500d973f2d1827250b071ab5e7d6d5d58c0e79dcef5b134913b4a610674d6ae7ed
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
VOLUME [/var/lib/cassandra]
# Thu, 05 Sep 2024 20:24:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 20:24:30 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 05 Sep 2024 20:24:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb77f528c512363c2e55cc3efe3d29552b31cde41662414b5316cc3adc2516`  
		Last Modified: Fri, 06 Sep 2024 01:01:37 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8163fb05ff694e1612eed9d726af4a7ccb06a0b2fb74071ff09a61c0e1f0702d`  
		Last Modified: Fri, 06 Sep 2024 01:01:38 GMT  
		Size: 12.4 MB (12379853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f0055bdb6318f20ca45019d229922928bbf30afefebd67d8cd67008020185a`  
		Last Modified: Fri, 06 Sep 2024 01:01:38 GMT  
		Size: 1.0 MB (1029704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383c3721662f10b49e72f2938adee209cce379c88677b818b72e2f432f2384ea`  
		Last Modified: Fri, 06 Sep 2024 01:01:40 GMT  
		Size: 70.5 MB (70517461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcb121604263255f1e5ef79e6577583b7a79b7974ca310cf2020f34b8fe211d`  
		Last Modified: Fri, 06 Sep 2024 01:01:38 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:6109f5d902d465edf4b3776e113e1cbde1e64510c88f85680dc1ca12e4a09590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4264605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007d7b4e363cb9590113eb276defd37b9afd04946ac774e349989d56a3a37a30`

```dockerfile
```

-	Layers:
	-	`sha256:775ad2d42f33e17d427b4dc9bb0d5746470865210fa0c46ccee4a9d94649a94f`  
		Last Modified: Fri, 06 Sep 2024 01:01:38 GMT  
		Size: 4.2 MB (4228404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7adee213d0b4040fab1c158e45b175b956699657a48f5cb144f6ee99076a34`  
		Last Modified: Fri, 06 Sep 2024 01:01:37 GMT  
		Size: 36.2 KB (36201 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:7ef9d377562deb610cba0c890876ea659591beb3f6221cd800d58fe7fc53dac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181166514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae93fbcaa5a3f4c47684a3ef7ef6bedc8d8d1c9adebb4378859a64d302d36f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 05 Sep 2024 20:24:30 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 20:24:30 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_VERSION=5.0.0
# Thu, 05 Sep 2024 20:24:30 GMT
ENV CASSANDRA_SHA512=cf91d9a5fe370a3b7eab9447852c491de1c17aca5a71c5ff06a672d210f8d6500d973f2d1827250b071ab5e7d6d5d58c0e79dcef5b134913b4a610674d6ae7ed
# Thu, 05 Sep 2024 20:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
VOLUME [/var/lib/cassandra]
# Thu, 05 Sep 2024 20:24:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 20:24:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 20:24:30 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 05 Sep 2024 20:24:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c03ba7cf8f4f911330fd6ac5a615501e6f0267f9f09dde12d3f8954ddb0ea`  
		Last Modified: Fri, 06 Sep 2024 01:46:14 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2024eaefb45dfe601ff0576af148cbe011b9d3745e3484db8a234526e1e365ce`  
		Last Modified: Fri, 06 Sep 2024 01:46:15 GMT  
		Size: 13.2 MB (13205722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24afb8f73b90f970edf28ab16456d68af41655613515f4341c2139e317fdee20`  
		Last Modified: Fri, 06 Sep 2024 01:46:15 GMT  
		Size: 1.0 MB (1018932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b482ad3d7caa248682607725a20acbf3f7d6e3539d4fd1994607aa94354343`  
		Last Modified: Fri, 06 Sep 2024 01:46:17 GMT  
		Size: 70.5 MB (70517900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb067ba397f7999bc9036fb54737aa20376ee0b647a8aa71ea75818ca6c5e01`  
		Last Modified: Fri, 06 Sep 2024 01:46:15 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:5fc4d893ad665d5c5806829f96bdbba7e7229de109a85ad07369bb181d4e8ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4268777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e65e3553182a08e8d98f0bf12e4e35609f2e3983ab321bba82715e7ac001da6`

```dockerfile
```

-	Layers:
	-	`sha256:abf493a3d2f4542c22225ddcd7e33e8dc4c337ff584b3adf14f3ed4288e9263d`  
		Last Modified: Fri, 06 Sep 2024 01:46:15 GMT  
		Size: 4.2 MB (4232871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8564ff674992923d42891e0ff3cc5ad78ee7beff2d38448c5e4cf5cc95780cea`  
		Last Modified: Fri, 06 Sep 2024 01:46:14 GMT  
		Size: 35.9 KB (35906 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; s390x

```console
$ docker pull cassandra@sha256:9e3cdf2fee1d7ecfb428c41f53484b04eeaefbe298e6a3d2c206603cd6f5cca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146232283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c1bd923e5a01342347eb69c289771c28181263ec260e242a0a9ceca791f23a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 14:24:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 14:24:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 14:24:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENV GOSU_VERSION=1.17
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 19 Aug 2024 14:24:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 14:24:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_VERSION=4.1.6
# Mon, 19 Aug 2024 14:24:25 GMT
ENV CASSANDRA_SHA512=3bae2a75aefc139ceaa9beb4709f9ee533517937ae292aba0102788cbf08f94f503c707124beaf06e28eca20dacf00a729da326c178bda432adfac2cd32b91c6
# Mon, 19 Aug 2024 14:24:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
VOLUME [/var/lib/cassandra]
# Mon, 19 Aug 2024 14:24:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 14:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Aug 2024 14:24:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 19 Aug 2024 14:24:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53d190393eca7947899727783f31b4d629b8cb328dd252d9cf9e1f57f52823`  
		Last Modified: Sat, 17 Aug 2024 01:33:01 GMT  
		Size: 40.8 MB (40817132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7494c9a7e12442d8d3b7e7296f1a1231b234cdff9fa8892908bd413186609079`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a24efbce9923f1d97c259e8e4ad520ca7f8b4fca7b20ac51689a5644df5f9a4`  
		Last Modified: Fri, 23 Aug 2024 19:47:07 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0aa5516181d2eacde1cdc5754b6d91119385dfc96608750ba42811d1073139`  
		Last Modified: Fri, 23 Aug 2024 21:10:38 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ccea29e34806ef6c46b376d09cac195487e70aa4e1676278d6f6086b245b0`  
		Last Modified: Fri, 23 Aug 2024 21:10:39 GMT  
		Size: 12.2 MB (12184139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71818433f8c310dded9b6239c3acd54482f3aaa7d219f6a7e9bccbb4f8c2641d`  
		Last Modified: Fri, 23 Aug 2024 21:10:39 GMT  
		Size: 1.1 MB (1064243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3726ed25aa4163429ee76c4249a73abc6fb8ebaecfb22037fd9716d1548885af`  
		Last Modified: Fri, 23 Aug 2024 21:10:40 GMT  
		Size: 50.6 MB (50567860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93d9ffa7e5e168189816e9ab9fc070708f95e87d9edcda3a64c1eb576956a2`  
		Last Modified: Fri, 23 Aug 2024 21:10:39 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc8569a4a47e4d2ff341712c1ba880eeb4bb3eff26387a73ad21da19a8b38c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377d4fa53bad2246b7dcb8877a4c364f22764a32e253c7776d782cb6710cd1ad`

```dockerfile
```

-	Layers:
	-	`sha256:982187009f15cb831db278399a44cfe909b673aa4c9b6f13368ea1c2c79f48a8`  
		Last Modified: Fri, 23 Aug 2024 21:10:39 GMT  
		Size: 4.2 MB (4192155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd3bbdfeb68086c13d2cddd2fcf6f9146785f28194fdd3505eeb1cf378ec2a5`  
		Last Modified: Fri, 23 Aug 2024 21:10:38 GMT  
		Size: 35.8 KB (35838 bytes)  
		MIME: application/vnd.in-toto+json
