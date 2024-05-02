## `cassandra:5-jammy`

```console
$ docker pull cassandra@sha256:a4b1c2bb96fa9b15260b26eac8ac2bafb47321e735ede26dd144d1b933495891
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
$ docker pull cassandra@sha256:80554850bad515492fc502ad601e3ec6e50c1a3eb83b09019921133d80cf39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183419275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a225b021e8a6b0e656a7cb9023a953678b55c8ff31b3750ea8fb3e00a47b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 20 Mar 2024 22:45:06 GMT
ARG RELEASE
# Wed, 20 Mar 2024 22:45:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 20 Mar 2024 22:45:06 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GOSU_VERSION=1.17
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 20 Mar 2024 22:45:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce394e5c05f6275f1a3d93ef078caadf4c6e88066e708ffa5cea964ded0c3c2`  
		Last Modified: Thu, 02 May 2024 01:15:30 GMT  
		Size: 12.9 MB (12905606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e026920ea2a9fd70b5b270aaa34672572276e0d92b9da71ce0b58a571ade52c5`  
		Last Modified: Thu, 02 May 2024 01:18:52 GMT  
		Size: 47.3 MB (47256136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d0df997d9c75c7ce45795a94101aa9b3c64050bf0b5c2ef92ecb36cfa36cdf`  
		Last Modified: Thu, 02 May 2024 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c863a9ccf459944a17dfde7fb73751761675f48f9812eff6de4bc2a9aefbb151`  
		Last Modified: Thu, 02 May 2024 01:18:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c9275b0b4eb05a45fa295954728db61477b12dbed0cbd5aab031026c76311b`  
		Last Modified: Thu, 02 May 2024 01:51:22 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7acdd3216362fc0ae53b95ac6eee27470011e0830535957eee64e14ac9300c`  
		Last Modified: Thu, 02 May 2024 01:51:22 GMT  
		Size: 12.4 MB (12399671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59149e3ba21d34e60a1363e68b708da2420198e8f289c1f6f40ac5295f6cf59`  
		Last Modified: Thu, 02 May 2024 01:51:22 GMT  
		Size: 1.1 MB (1097658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf0821d23b88a493d8a85445813c882299ab5722cab2c16332a3dd9cc15db05`  
		Last Modified: Thu, 02 May 2024 01:51:23 GMT  
		Size: 79.3 MB (79316718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2873e4fdc3aa003e2eb464d279238842a70f1148320c8ac29e4d2b37901f89c0`  
		Last Modified: Thu, 02 May 2024 01:51:23 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:8d67da2366c1f993c711c95ed1089976b4548e8e68a5370c6b756cb98a396059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b7bd62c6128865d566cfa65d0222ca245abaa8a2a880608ecf5d1563613c22`

```dockerfile
```

-	Layers:
	-	`sha256:f93e4d99f9c7ad501e21e192d2e7dcbc189264df270226c1c142a2142f5e02f7`  
		Last Modified: Thu, 02 May 2024 01:51:22 GMT  
		Size: 4.2 MB (4184560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2f234120bd7f10ae5493be11b45158c125b3d12d4a49cd1836384358eef1bc`  
		Last Modified: Thu, 02 May 2024 01:51:22 GMT  
		Size: 36.0 KB (36018 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:a3849ea523739182012ab7a70049977ce52e6a8ff8cd976fbbc1a7de0d820767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176807222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18651bfdb1463d5afae776d22daf5570d60b6915a46bd1e1e47078c7396b380b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 20 Mar 2024 22:45:06 GMT
ARG RELEASE
# Wed, 20 Mar 2024 22:45:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 20 Mar 2024 22:45:06 GMT
ADD file:ab2e95a123b006ac900aaaf0d1858b88941c8d319f47e41733db6f0f5fe98b87 in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GOSU_VERSION=1.17
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 20 Mar 2024 22:45:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:b7e19bb2918236ac8ccf2faf405ff5a9521a86762ef07ef60917aa41d6dc8155`  
		Last Modified: Mon, 29 Apr 2024 07:54:39 GMT  
		Size: 27.5 MB (27536224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e5c703cbff6ae09d1210453797a0781455500f04990cb48a4001c468ac0921`  
		Last Modified: Thu, 02 May 2024 01:27:59 GMT  
		Size: 12.5 MB (12494270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c065091e5f2b9eecaa7cada683e288c305ae4bffbc03fad16f6051ed64e586e`  
		Last Modified: Thu, 02 May 2024 01:31:11 GMT  
		Size: 44.9 MB (44917088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd20d0118ddfcc4fc2c234b1078d6ed652866bb20cc64e07f33ce177dc95039d`  
		Last Modified: Thu, 02 May 2024 01:31:04 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c4e0de1285fe045e5430fa0e22cb6db7675ebe382a21394cc0725a81c8a23`  
		Last Modified: Thu, 02 May 2024 01:31:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dfae19eaa335fc45792945c560edbb52bb0e9da46be202178d07c1b7361334`  
		Last Modified: Thu, 02 May 2024 03:06:13 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b9179e2814c3f11571d5aa7ea16ec5bf7ef91796379ae9b05cc8290c2ce16`  
		Last Modified: Thu, 02 May 2024 03:06:13 GMT  
		Size: 11.5 MB (11471672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caed3f8c68b4d52d6ab848cb2c64a20824c19e47c11c38630f54b98452c0cc26`  
		Last Modified: Thu, 02 May 2024 03:06:13 GMT  
		Size: 1.1 MB (1065916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46822ddf0c642d5af05eaf51eb4d7ebdc6cec529e208d8b2a685ae156a67f8b`  
		Last Modified: Thu, 02 May 2024 03:06:16 GMT  
		Size: 79.3 MB (79318220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643487d41849aa12b5db98e9b71dbcb51def697e06950908eccc3f2f78b90c7f`  
		Last Modified: Thu, 02 May 2024 03:06:14 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:52a52c54b290febf0002bcd20c47b1cb4c3c9afed5be78f110fc74e707dcdf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78d3778c1f53bceb58e4ee310fbd3edc2e68b60372f765814c28bc483b3a20f`

```dockerfile
```

-	Layers:
	-	`sha256:60edacd1d2fabba386027ca196dba678bdda67636d7c7b717ef9736f265ba75e`  
		Last Modified: Thu, 02 May 2024 03:06:11 GMT  
		Size: 4.2 MB (4186127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d32dccb4e9ea164de0dfb2a123747f9ca1dfd5a8dee12ba874ea4d2aa7ad18f`  
		Last Modified: Thu, 02 May 2024 03:06:10 GMT  
		Size: 36.1 KB (36143 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b3e714d578f1da72c9d6a3d6235f881a996c42efeceec3097dfeeac7f71bbbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180692423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e8985b1a8391b68fb5f87f73b7e19e6cc6d3a3893a6a9a1ebd06ca7025baf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 20 Mar 2024 22:45:06 GMT
ARG RELEASE
# Wed, 20 Mar 2024 22:45:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 20 Mar 2024 22:45:06 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GOSU_VERSION=1.17
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 20 Mar 2024 22:45:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1725094f1f7082f023c1a047ec828bf8229f9aa4b95de8dfcf3433a5664a8625`  
		Last Modified: Thu, 02 May 2024 04:20:25 GMT  
		Size: 46.7 MB (46716197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e995ccba802f11ec98d823c76df9fc769ae179b10b0a6b239f526dcd74f907aa`  
		Last Modified: Thu, 02 May 2024 04:20:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7fbbe7faa2fd420d969dafb00e3a6a0cc66074e4786e50e8c8b4f22e7f754`  
		Last Modified: Thu, 02 May 2024 04:20:20 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfb4e0d2e0cb6e757c4a7600bd2139912b7d3aa05494577cae20299d69e41a8`  
		Last Modified: Thu, 02 May 2024 11:09:33 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7248e9e75c64ec73e167e3d79b0c16780daa1bb294876de9b760cf468141d`  
		Last Modified: Thu, 02 May 2024 11:09:34 GMT  
		Size: 12.4 MB (12377244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106d372637ca32a73b370308923e70ed408fa1d535f75e701d55686a78d0302e`  
		Last Modified: Thu, 02 May 2024 11:09:34 GMT  
		Size: 1.0 MB (1029803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c463a51097d00a9fbb6b33bc03b4b7a1b3944acc8e9e5326fe2ac1f4381f0`  
		Last Modified: Thu, 02 May 2024 11:09:37 GMT  
		Size: 79.3 MB (79317126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417615e6893debc75231ee6a461c634c8400f0f8d4283764fdf0702db9663b4f`  
		Last Modified: Thu, 02 May 2024 11:09:34 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:9663f32cec4d7afe705ffaa9ff6efabef3a0d77ed7c02f115bcfad01858b5b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faec836f1dc129f2c4d840dbb8feca17702cfc26beefd227ab5847ab93c4e7bd`

```dockerfile
```

-	Layers:
	-	`sha256:f1fc5213d5590b735d465d31497e4e1fd5b09d99795bda779949cae271509b38`  
		Last Modified: Thu, 02 May 2024 11:09:32 GMT  
		Size: 4.2 MB (4184870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe184f21a9d7fc7ffc652b0697eb4d5896fe3643b63a96e61f50371caabbae9`  
		Last Modified: Thu, 02 May 2024 11:09:33 GMT  
		Size: 36.0 KB (36032 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; ppc64le

```console
$ docker pull cassandra@sha256:b88420246038166001f29370102d1faf6c28204b66112e105adb1318d0ba2836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189993264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf34c4c4122efe42174066603742accb11d7d52633b1f2e625cbad91115bee6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 20 Mar 2024 22:45:06 GMT
ARG RELEASE
# Wed, 20 Mar 2024 22:45:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 20 Mar 2024 22:45:06 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GOSU_VERSION=1.17
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 20 Mar 2024 22:45:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0de467fd0448940d36a45afa474251ce2e8bd6e8f60ef7eb65adb86c07161a`  
		Last Modified: Thu, 25 Apr 2024 20:52:58 GMT  
		Size: 13.8 MB (13767010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139c1ea4e64d0b726f7d19518870f27a28d6bc36f6ac3db66d8eb91060a294de`  
		Last Modified: Thu, 25 Apr 2024 20:56:22 GMT  
		Size: 47.1 MB (47088915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8b1496c6d2c3bf4eee8880414a7a0f10b22fecc23b08012e3d6e7580bd8ac5`  
		Last Modified: Thu, 25 Apr 2024 20:56:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016cbc90916d690e8bd5221d91fa763a9df5fed03fdf320b50d50025a43d31ef`  
		Last Modified: Thu, 25 Apr 2024 20:56:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421a1471c03bf4dc0a501fc2ecf6a398c42bc0a1d9d34923a5d7ebef726199a`  
		Last Modified: Fri, 26 Apr 2024 17:35:21 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfa1fc1e45c5f322728a272b3a4e4bc4c647654dd3d33b33584f3907f4026`  
		Last Modified: Fri, 26 Apr 2024 17:35:22 GMT  
		Size: 13.2 MB (13208742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c92a99d1f63dcfecdf3efb0aca481bd27eb8f7c6418f2b882548b41e93708`  
		Last Modified: Fri, 26 Apr 2024 17:35:22 GMT  
		Size: 1.0 MB (1018970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748b65a885bf0b2c5720289f7cf5a2e88ac06a2d716e454662848f3ac05baad6`  
		Last Modified: Fri, 26 Apr 2024 17:35:25 GMT  
		Size: 79.3 MB (79317473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa74a28d4be1a8a85391486c44fcdad0bfdb0528cc52737fc9463c0cc2ca8554`  
		Last Modified: Fri, 26 Apr 2024 17:35:22 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:ead967f188e4d275da3d8a644e151283f190315210fe1ef1076317fef0d812ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4226105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0be781da28f3ccf9cb7989c0571d43d078bb2219679b81afff4e9ec666081b`

```dockerfile
```

-	Layers:
	-	`sha256:89e428ad6b929512702c503686072ce152fffc0cd599b681c95b5f7ce601723b`  
		Last Modified: Fri, 26 Apr 2024 17:35:20 GMT  
		Size: 4.2 MB (4190848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e9a1632783bcac40abbfe08dba5a5a485ce638f13aa854e962863f85a99a34`  
		Last Modified: Fri, 26 Apr 2024 17:35:19 GMT  
		Size: 35.3 KB (35257 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; s390x

```console
$ docker pull cassandra@sha256:1749c17966ab75d0b5072009c0f1cf8f753030e13e5ebcac4266f5891a53dd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178024195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019f7125c10add630fdb8b869e2e97a3f3f95bba711cbb954be339a170161764`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 20 Mar 2024 22:45:06 GMT
ARG RELEASE
# Wed, 20 Mar 2024 22:45:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 20 Mar 2024 22:45:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 20 Mar 2024 22:45:06 GMT
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GOSU_VERSION=1.17
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 20 Mar 2024 22:45:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Mar 2024 22:45:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_VERSION=5.0-beta1
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=d67aa211858f090dca6ea2ac84ed405bd4791aaf493e3c8e5b24fd44e54aa3132eeca3f4e310d6d1aad1ca105515011d6e177d169a6e94af0a257ffc95b4f175
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 20 Mar 2024 22:45:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 22:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 22:45:06 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:a9e3c76851ed4cb17ff69f864b6230094c69b50fc344074f5cccf18cabee6dbf`  
		Last Modified: Thu, 25 Apr 2024 20:58:17 GMT  
		Size: 28.6 MB (28637471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256964579a885020253dbe5c22f56c46052445d333305990618830cec3421a61`  
		Last Modified: Thu, 25 Apr 2024 21:19:46 GMT  
		Size: 13.0 MB (12986661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed742935159ae2c8d2eb3c9f9c197cd910b010bd4da24fa3b3742f4d490ab32a`  
		Last Modified: Thu, 25 Apr 2024 21:21:38 GMT  
		Size: 43.8 MB (43830966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb485526c73c1b0a7f4587028c9115bb0d739697e08a0ecee6641e11aca6ac9`  
		Last Modified: Thu, 25 Apr 2024 21:21:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c371f0304c7553249d1955cd601fbf909fbe857da6c62e96f58b2ea42297afaf`  
		Last Modified: Thu, 25 Apr 2024 21:21:32 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f918caa77eb673e013ef4007cb1449082fa49d8028eb36a41011b65c75f757b`  
		Last Modified: Fri, 26 Apr 2024 19:52:32 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74055404fc526780bfbca70976f65e7cdf897aeaae125e1e6eff276568525dd5`  
		Last Modified: Fri, 26 Apr 2024 19:52:33 GMT  
		Size: 12.2 MB (12184156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee48691e7a46751b9f6d87d5ed1d4c789ba3d3e617fcac4bbeadec58d077a04`  
		Last Modified: Fri, 26 Apr 2024 19:52:32 GMT  
		Size: 1.1 MB (1064236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4319e4d2beed14c83ce6403275e83bf56e3b722fc01ed9457b39d73bbbabaa2`  
		Last Modified: Fri, 26 Apr 2024 19:52:34 GMT  
		Size: 79.3 MB (79316858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e43484574dec14c0c2eaf85d6ee09148ee5c7b7695007673bc69e05af9786e`  
		Last Modified: Fri, 26 Apr 2024 19:52:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:b30adf4b32d541ff8e32846eab5fa863364958133bd0cd5973c574ec087acb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7705779ffedf7e0c1387d261544ab27120105d460fc40a1e66bcfa9d97ce355e`

```dockerfile
```

-	Layers:
	-	`sha256:c43318800d535d3dcf554d501f71aac573f925d1a2b873199411d333d31ea47d`  
		Last Modified: Fri, 26 Apr 2024 19:52:30 GMT  
		Size: 4.2 MB (4187200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359b6159141d47b43b873c423f446c1ea26d5038c12f34800451161ac1db421e`  
		Last Modified: Fri, 26 Apr 2024 19:52:30 GMT  
		Size: 35.2 KB (35200 bytes)  
		MIME: application/vnd.in-toto+json
