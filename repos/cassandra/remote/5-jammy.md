## `cassandra:5-jammy`

```console
$ docker pull cassandra@sha256:a4d54af6071972e18561ee534e98017c936405393e2ef6596820ec2d47467e54
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

### `cassandra:5-jammy` - linux; amd64

```console
$ docker pull cassandra@sha256:d7e1c9f73c90c2c363d71c91fd19a73cdc7853895e9c22a538aba71b265c68d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187895879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88f3b99a187c206aa7198678d0cf8a1542a174aa23b3e733b517b45511b369f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 16 Jan 2024 18:43:13 GMT
ARG RELEASE
# Tue, 16 Jan 2024 18:43:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Jan 2024 18:43:13 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 16 Jan 2024 18:43:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GOSU_VERSION=1.16
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 16 Jan 2024 18:43:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba25f418af9cdd852d711718b911f4200dbf48ec9e0d514120bd83bf80e5eef6`  
		Last Modified: Fri, 16 Feb 2024 02:50:01 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6d03b083be1f1822d10429a1f55deb7cd34b5ef0c1c44740f813e6258afa7d`  
		Last Modified: Fri, 16 Feb 2024 02:50:01 GMT  
		Size: 12.4 MB (12402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3621598a6949ad73b6f1d241791c7f7ae251ef19f1b514ec64d465cd3ca2b1c3`  
		Last Modified: Fri, 16 Feb 2024 02:50:01 GMT  
		Size: 1.1 MB (1099268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792b4fcea1f26583289d6e92fbd12424f73ede9fac2e98152cdc7a9bf0e0341`  
		Last Modified: Fri, 16 Feb 2024 02:50:03 GMT  
		Size: 79.3 MB (79318778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb7609bd96aaa2ab82fc225f9661dd03160ddf6fadf33588c6749ae1e976569`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:ee0d9be381b0b060732bee7a80d265c2fd945348e1c9929b5bfc1a5c2ae60ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aad7e7c2ed9541796365c51e7f1ad7c21163e6c303df2aafdb31588226bdac`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7767e6b91c684f947fa67d5a52784d310c1a3c9eec7e61b73f386b54e0aa6`  
		Last Modified: Fri, 16 Feb 2024 02:50:01 GMT  
		Size: 3.8 MB (3790191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a94a0d529116aaee9148f752a49e62c574fafdeed66e7f7e6d736db5fca9f9`  
		Last Modified: Fri, 16 Feb 2024 02:50:01 GMT  
		Size: 36.0 KB (36013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:3b4997e5025515805de0be88015d6492dcb6c00917d884154ee3b01f4928b1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181792762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4d93bccd91d55561cd758c71555b371bf594db75ddb8e2a12fa58ae3a847ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 16 Jan 2024 18:43:13 GMT
ARG RELEASE
# Tue, 16 Jan 2024 18:43:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Jan 2024 18:43:13 GMT
ADD file:6767efafdb51cef2acde13d723fa618ffb3cd2155983115496c43ae730e762e6 in / 
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 16 Jan 2024 18:43:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GOSU_VERSION=1.16
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 16 Jan 2024 18:43:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:469ff1e358fe0665e6d5ee032bad43f71c0f28f2231f273ce387dcaaaabf733e`  
		Last Modified: Wed, 14 Feb 2024 02:35:21 GMT  
		Size: 27.5 MB (27532464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e772b5c9a5ba5b718084e53d8d023f0ae531de7e351cc19a4982c01a4b41a76`  
		Last Modified: Fri, 16 Feb 2024 07:43:40 GMT  
		Size: 17.6 MB (17592912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b022ee625596e3739bd37edce11492ee30b887ee03ecfda347adad2d41e3719`  
		Last Modified: Fri, 16 Feb 2024 07:44:08 GMT  
		Size: 44.8 MB (44798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d14fff6bad669ccfd42b40ec388261e0966a749c42eff32e55ec9aae647673e`  
		Last Modified: Fri, 16 Feb 2024 07:44:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bd39c66ca3c30eb63a02eff2092ca19b8d79a0898c55db23b7f3b194f910e`  
		Last Modified: Fri, 16 Feb 2024 07:44:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02cd2c483a39ad202ef132296b15f41a87942c5a1325fb57a5f02297baf1de`  
		Last Modified: Sat, 17 Feb 2024 05:48:37 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c28ac48d1ca113f0f0fb07bd712d2f7ab03fa0c13c41203939412b40b6f356`  
		Last Modified: Sat, 17 Feb 2024 05:48:38 GMT  
		Size: 11.5 MB (11474701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0667f26fdc91ada97246258afbcd42f27943f57c757f27d4b43ee6cb9772c0`  
		Last Modified: Sat, 17 Feb 2024 05:48:38 GMT  
		Size: 1.1 MB (1068716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da08afa27cd1583a8622fa358c926d87d67c3aaf901da4c27b137a9f789b5855`  
		Last Modified: Sat, 17 Feb 2024 05:48:40 GMT  
		Size: 79.3 MB (79321256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b28c90f0953947079329e336c9243d9b1aa1de59f6fe4b14d1012c5a256aef`  
		Last Modified: Sat, 17 Feb 2024 05:48:39 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:523269e07ffc9913371da7e43d772c073cd9f2672c0a7b917e1e95d5a4ee9202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbae667703c7f7bc9e824458b31f01ade9ae705a8010118b5fb74b3d503de83`

```dockerfile
```

-	Layers:
	-	`sha256:f4fbaa8c878ecbf76ea6c86245d07f378fa20ed8ec1192511ca3911f06971449`  
		Last Modified: Sat, 17 Feb 2024 05:48:36 GMT  
		Size: 4.3 MB (4261381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d6b1caa9f75322867cb03aebef9710c8a570b5a8afb14825d9a4e32062e9b1`  
		Last Modified: Sat, 17 Feb 2024 05:48:36 GMT  
		Size: 35.3 KB (35321 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:3036fd980359a363d83be6b90068085f2db8918e3c9378bd375cae3afb58a0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186632091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d5ba57902f92b4e1801a7a90d0aba91ef213e0c2c6024b68667ea2de70242`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 16 Jan 2024 18:43:13 GMT
ARG RELEASE
# Tue, 16 Jan 2024 18:43:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Jan 2024 18:43:13 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 16 Jan 2024 18:43:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GOSU_VERSION=1.16
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 16 Jan 2024 18:43:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbec7b6f8e9cc6900734393a324e830112ae112afe8f339e4af97a524abe7c5`  
		Last Modified: Fri, 16 Feb 2024 12:18:56 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd32332b1dca3b40af37ff0f0adba851fa3a613fb0cf3da3510b1e1ccc16871e`  
		Last Modified: Fri, 16 Feb 2024 12:18:56 GMT  
		Size: 12.4 MB (12378674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56157700e6c7b3c1b6b16069a15e8aadfca3c32a559d92e1a9803a984d086c25`  
		Last Modified: Fri, 16 Feb 2024 12:18:56 GMT  
		Size: 1.0 MB (1030606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20ed017c8639660023d60870652bac5b868247d742d04f96782fc3e20b27bed`  
		Last Modified: Fri, 16 Feb 2024 12:18:59 GMT  
		Size: 79.3 MB (79318726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3eb83787f3f75d96332dfd233987b4bc99fece2f71541193f3ac8f1809f888`  
		Last Modified: Fri, 16 Feb 2024 12:18:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:737501416765937f6ec2ae2d94599b76d3a6235510de96741a14591fc99973b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3910046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25aa07fa252a3a1ab91091f2146484139b4a0c1c8e29063631b81da0b15f728`

```dockerfile
```

-	Layers:
	-	`sha256:cc56101de203a195eac0ec646f29db720facd46992436e25c0ef003f186f46ac`  
		Last Modified: Fri, 16 Feb 2024 12:18:54 GMT  
		Size: 3.9 MB (3874018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb00a0c0f4b7b590a7bf2d780b139591ad70c87a75b20cda8680d4fe6ec7be0`  
		Last Modified: Fri, 16 Feb 2024 12:18:54 GMT  
		Size: 36.0 KB (36028 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; ppc64le

```console
$ docker pull cassandra@sha256:43735da49c74b790d6ea84395d4dc95942dd5e40bc257ea7439c020900c7faac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194922542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2f0549f2a42ebc00d7e94d5425ac49572e5cf4341311e8c80640e74f66f53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 16 Jan 2024 18:43:13 GMT
ARG RELEASE
# Tue, 16 Jan 2024 18:43:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Jan 2024 18:43:13 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 16 Jan 2024 18:43:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GOSU_VERSION=1.16
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 16 Jan 2024 18:43:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc402319b10feb1c6820fa2bc7cfba7869a3473e27191ab283db519e7e6da50`  
		Last Modified: Fri, 16 Feb 2024 03:08:21 GMT  
		Size: 18.7 MB (18726189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f9bec281d586fe857a730cd40136459428c7ccefda7ad98a1e0c5194e2d295`  
		Last Modified: Fri, 16 Feb 2024 03:08:53 GMT  
		Size: 47.0 MB (47012472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d28cb5695f590c46c7d223348d7d58bfba0e23dec221f5343b0dca7a09bcb`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aabc96be0541477c14b4c395f0cedb75eb6388609833afb6cb0da3a3b182c7`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6131ba1a0d1cc104266e7fcdb235550d03326d4e296c661ea7bc8d7b481487`  
		Last Modified: Fri, 16 Feb 2024 07:35:23 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd14e31b28bc1aa7c1e4f17d7031b32233c2d6f973ff4f9792efea100d9f3fd`  
		Last Modified: Fri, 16 Feb 2024 07:35:24 GMT  
		Size: 13.2 MB (13210842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5935564e2892ab28c7532fb5ef14f44fed7ab0df9c648a16d417c5a294ccee`  
		Last Modified: Fri, 16 Feb 2024 07:35:24 GMT  
		Size: 1.0 MB (1020725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b33f88f849160a9b7930c5dfc5a995621dc040e8b75907e88d997ac7480afc`  
		Last Modified: Fri, 16 Feb 2024 07:35:27 GMT  
		Size: 79.3 MB (79319631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ca345a7f3217b22b936cb364cd36381e25a027cbb764ed01fdc384b48043c`  
		Last Modified: Fri, 16 Feb 2024 07:35:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:9984338760ebd2d1146c12707b2ee25482e1ca42407384b5801d03c9dc6f29bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10f511d30534cbb8866a8c8e61fe8f00180c7a6a83c675c3bc697105a177922`

```dockerfile
```

-	Layers:
	-	`sha256:0a7bb4795c5fef423676c0077e33867dbf3c083d47aa34c905ffa21aa2313648`  
		Last Modified: Fri, 16 Feb 2024 07:35:22 GMT  
		Size: 3.8 MB (3817378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:815869bcb144251d1e47f473230e14163ffac9f95f9184aa373cb170159a3c12`  
		Last Modified: Fri, 16 Feb 2024 07:35:21 GMT  
		Size: 36.1 KB (36069 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; s390x

```console
$ docker pull cassandra@sha256:4246674aefde854d3799a2b8ef1f51a5f7b6551c7f6dd33ce1e5a441156ea543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182240374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ece82709d10788376e967c00dc3947b8e79053cd08ea34fcb154b48162b4d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 16 Jan 2024 18:43:13 GMT
ARG RELEASE
# Tue, 16 Jan 2024 18:43:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jan 2024 18:43:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Jan 2024 18:43:13 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 18:43:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 16 Jan 2024 18:43:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GOSU_VERSION=1.16
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 16 Jan 2024 18:43:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:43:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Tue, 16 Jan 2024 18:43:13 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Tue, 16 Jan 2024 18:43:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 16 Jan 2024 18:43:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 18:43:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:13 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 16 Jan 2024 18:43:13 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06439c312d07b9a9a2b1abe400a875c694ea9d34abcd938043094f9fa832631d`  
		Last Modified: Fri, 16 Feb 2024 07:38:53 GMT  
		Size: 17.3 MB (17261530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a98bc508a0ab498758127e894ef7be31f835c290ca2eb4bf51d33dcd69f3b`  
		Last Modified: Fri, 16 Feb 2024 07:39:16 GMT  
		Size: 43.8 MB (43765973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc62b1194733a4e6d63c34bbe6cb119a73c7ee7312f4f386a1257fbcacd6971`  
		Last Modified: Fri, 16 Feb 2024 07:39:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95477c395ccdd2f62b54717915da0157b15ffcd321dcfa0747ae0d633fa98db1`  
		Last Modified: Fri, 16 Feb 2024 07:39:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97ed7ecc39611b1091d585460e6c98f6953ea9405f73c6a3cadfa2c604c1fab`  
		Last Modified: Fri, 16 Feb 2024 21:08:46 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed99af29d4b5d95c2b00bc1fd39478847d6dd5b099d87b86148fd696c3637217`  
		Last Modified: Fri, 16 Feb 2024 21:08:47 GMT  
		Size: 12.2 MB (12185908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c6944d0fcd6280ecfc063bfe60e68dfd0a7682a9e9c8c466dd93bd4acc179c`  
		Last Modified: Fri, 16 Feb 2024 21:08:47 GMT  
		Size: 1.1 MB (1065470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e765080e0d43255e1e756e43835ed46749601edc1237449fe15b12f3845c9`  
		Last Modified: Fri, 16 Feb 2024 21:08:49 GMT  
		Size: 79.3 MB (79318926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6085e087b55fd9448a74657cf2d7b10cc8c01ce9818b8a42b47649a6cf8fe9`  
		Last Modified: Fri, 16 Feb 2024 21:08:47 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:6e2fa3957ca61ce2eafdd995019b46c0ea8c4fa3f9197a5553695ac1b0e86c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e00266dd05cf429e6d094da6c8981b778899cafac4539577b874006e4842ce`

```dockerfile
```

-	Layers:
	-	`sha256:98644cc4a13cd8a37e22cff1407f2cb4f4a1f01c5d457f5f3c8b4124e7a25e95`  
		Last Modified: Fri, 16 Feb 2024 21:08:46 GMT  
		Size: 4.3 MB (4269994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42dea88df7e305c3383e00568e5059f28452aa543288757985f0a96114c0db21`  
		Last Modified: Fri, 16 Feb 2024 21:08:45 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.in-toto+json
