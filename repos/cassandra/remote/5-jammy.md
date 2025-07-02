## `cassandra:5-jammy`

```console
$ docker pull cassandra@sha256:bfdc26dc00fafa267e40b3c8899ee90df34df37fa8f3ad85afb7a7cf0b4ff54e
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
$ docker pull cassandra@sha256:ff945e324f533a9ed8bcc3000960d18fb51e829b76187674071616487e9b3dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177427958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ad075d2582f56b1e01afec9b1be4531217531a79a9667c298daeb4b63ba184`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Thu, 10 Apr 2025 20:24:29 GMT
ARG RELEASE
# Thu, 10 Apr 2025 20:24:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 10 Apr 2025 20:24:29 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["/bin/bash"]
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GOSU_VERSION=1.17
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_VERSION=5.0.4
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_SHA512=16de8bb78af94dabfd916825f492de7040a7311791bc1d630f14707d88f7132e51ae38dad7ebbaf13d2d154af0bdeefe318d680798b8e247ae4117cbc0e2f6df
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
VOLUME [/var/lib/cassandra]
# Thu, 10 Apr 2025 20:24:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25706e9e719c4df9907a583a3af1bbbc40149b54bc63ac893255b24d05ebe2ff`  
		Last Modified: Wed, 02 Jul 2025 03:10:17 GMT  
		Size: 16.1 MB (16146410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5006e0852115f86cb2b9abb297c58242bffb3b63d6b9d8cb26aac444a36837d8`  
		Last Modified: Wed, 02 Jul 2025 03:10:18 GMT  
		Size: 47.0 MB (46958370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e412a6aa107b415b5ed7736de94863c64915907b34bd70dd1f95411c12465394`  
		Last Modified: Wed, 02 Jul 2025 03:10:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023b21e1d611c552afa7c4c7b7112fca2b91d703f849cf0388c5f572c201088`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabaaf6abd3b643c9934e21f95be30e080a769c887f3402216594f32840be629`  
		Last Modified: Wed, 02 Jul 2025 06:03:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ed377728e4d37783e9a32b8bceb062f61603163b2ccfa116d95c18ef4c656c`  
		Last Modified: Wed, 02 Jul 2025 06:39:38 GMT  
		Size: 11.5 MB (11504820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c96b3addf5299b754b0e3ca6ffb965883923db880787089dc3689d88685ddb8`  
		Last Modified: Wed, 02 Jul 2025 06:03:34 GMT  
		Size: 983.7 KB (983735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19125d3cdb15b3b886aa18b9bbdc4fb4fa7a0a0126b6dee9cf1e2c006c751b5`  
		Last Modified: Wed, 02 Jul 2025 06:39:39 GMT  
		Size: 72.3 MB (72293546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e81de2eb4af3da385dc68cb702df232d8e27241522f058cffdb97f148fda2b`  
		Last Modified: Wed, 02 Jul 2025 06:03:36 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:9e77812a9af92b6f6aa448386f76a185f58b8fbc4ec61a936c5f7f8d7ad723ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3031f55abfbddabd65f671a0e9bdc8e41563e26f1b8b553b079fd26aa59c0704`

```dockerfile
```

-	Layers:
	-	`sha256:8d9a34f670a4f8f012c2b98ae4a0307a7e53482ceed5d487b1ffcbd034dbe596`  
		Last Modified: Wed, 02 Jul 2025 06:39:15 GMT  
		Size: 4.7 MB (4652804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da5ab62230c4994c697b8515a7daca402f201144102a2ecc8124a858bc41aa0`  
		Last Modified: Wed, 02 Jul 2025 06:39:16 GMT  
		Size: 35.9 KB (35861 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:bfd084dd74a0e4d533586166a6857d3fee3ca86b841a0c4a626355debb7fe297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171133637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a6b2591cb460b477cdb33b4d8f6d3bd38c35fc6510b75ef55aad7c6355b76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Thu, 10 Apr 2025 20:24:29 GMT
ARG RELEASE
# Thu, 10 Apr 2025 20:24:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 10 Apr 2025 20:24:29 GMT
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["/bin/bash"]
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GOSU_VERSION=1.17
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_VERSION=5.0.4
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_SHA512=16de8bb78af94dabfd916825f492de7040a7311791bc1d630f14707d88f7132e51ae38dad7ebbaf13d2d154af0bdeefe318d680798b8e247ae4117cbc0e2f6df
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
VOLUME [/var/lib/cassandra]
# Thu, 10 Apr 2025 20:24:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["cassandra" "-f"]
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
	-	`sha256:ad9d29412214f0bb3ae1ca6359ffe2b06eab1e2dce8df2cf7f5cf6067f800f30`  
		Last Modified: Tue, 03 Jun 2025 14:52:58 GMT  
		Size: 44.6 MB (44627699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae939c27ada554e34c95a9535bdc2d49f6b3b35ef107b23539241bdafeea8253`  
		Last Modified: Tue, 03 Jun 2025 14:52:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae37adf9efe32eb808814e960ab7c2d390d122c21de591ef17d179e3eb92d5`  
		Last Modified: Tue, 03 Jun 2025 14:52:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a284371cd82b5772e5810e0bd9c364ac5c1300b36d22b6fd8ac758ffc91c8503`  
		Last Modified: Tue, 03 Jun 2025 18:47:45 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb1fc397ebcc6afa3c3647845e7813aacb75cc9efb4d641dcd3dbdc21c071b`  
		Last Modified: Tue, 03 Jun 2025 18:47:47 GMT  
		Size: 10.7 MB (10724713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e9bad198faeeb7f077dbb8b4a39fc27c8e8be5cddc5b51c8810948e3f8cfe`  
		Last Modified: Tue, 03 Jun 2025 18:47:50 GMT  
		Size: 950.8 KB (950780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b75e425e6f3d5bcc7519f663e8d2e559376ddf01bc9cbc30f5dd4f8c664488`  
		Last Modified: Tue, 03 Jun 2025 18:47:59 GMT  
		Size: 72.3 MB (72293601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c92af301f44fd95e3a43c3923e17f9853e7e4b0add699f3b3a9687492d26b`  
		Last Modified: Tue, 03 Jun 2025 18:48:03 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:0e02e6f5993d80f1490be04439aed6ff9547fbc6eaf6759762b4eae76e5033c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5518d0e19f254b9c12b9098510c7d60b4efde503f109fe4afe485ca3afcfa18a`

```dockerfile
```

-	Layers:
	-	`sha256:97d58ee50d7fc127ce9851a62c5476ea671fec6f753ea13cb074103b08195306`  
		Last Modified: Tue, 03 Jun 2025 18:48:07 GMT  
		Size: 4.5 MB (4486589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27a554ca4c84fd016b9b1c3836b88a1c7f043b977ee5cf9926962316c4baccd`  
		Last Modified: Tue, 03 Jun 2025 18:48:09 GMT  
		Size: 36.0 KB (36008 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:a047508658e9b737ec78fa65ca8696696d23af7a0a0b57c47626384a86b77576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174556194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b775ebdd6d22a073cd130ca50ba904167eae9ab7a3dd36159d4e29a456708d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Thu, 10 Apr 2025 20:24:29 GMT
ARG RELEASE
# Thu, 10 Apr 2025 20:24:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 10 Apr 2025 20:24:29 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["/bin/bash"]
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GOSU_VERSION=1.17
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_VERSION=5.0.4
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_SHA512=16de8bb78af94dabfd916825f492de7040a7311791bc1d630f14707d88f7132e51ae38dad7ebbaf13d2d154af0bdeefe318d680798b8e247ae4117cbc0e2f6df
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
VOLUME [/var/lib/cassandra]
# Thu, 10 Apr 2025 20:24:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["cassandra" "-f"]
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
	-	`sha256:1f181eb73bb6ad9b3ede3ff2f5338e69c4a35396cbac54071a5b54dd357117fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 46.5 MB (46474291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4faeca29dfbbf9936faeb2e530a85cbc9340a33951b4a9eb39e6a08205384`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5d1030645941465b3a74306b718b8de08a9e502f0aa56b18085d4618d97b1f`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9431f990a9f2b4f6e8dcf3af528ce363416703b409521bc537f0ac5fbf8759d`  
		Last Modified: Tue, 03 Jun 2025 13:32:06 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d343e985cb8c1c4efddacc4cae42bd7a2490695d7dcec9cad5fe28c266fd63e0`  
		Last Modified: Tue, 03 Jun 2025 13:32:08 GMT  
		Size: 11.5 MB (11453077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0deb5c8ea221fa9a736b2dd16d993e799ea0e0b9f60b665ed407852959e09a`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 914.5 KB (914458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17296d4253651a8df001c3cb5403dc54d6a15cb40b73617974e10bf7cf87a3ac`  
		Last Modified: Tue, 03 Jun 2025 13:32:34 GMT  
		Size: 72.3 MB (72293546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c616685693d6bd02fa8776880947d5948f2f5c814c58c1a75fc76f42f5fe2`  
		Last Modified: Tue, 03 Jun 2025 13:33:26 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:4f5fb8f013590303bfb1da451f168c805a01dc14957f768f1d71baf4dfd48f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4519888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b147f3de27dfb0e4f2946b1926284b44e55e43972899e91b8ad3e7e68caa14`

```dockerfile
```

-	Layers:
	-	`sha256:a762353d08aa94e4ac3281bb7394825644302cab8e9ab360fce97c367566e6f6`  
		Last Modified: Tue, 03 Jun 2025 14:18:23 GMT  
		Size: 4.5 MB (4483831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c136a9fe624639cbdf2c99407a433af67e679ea638c0aa5e0738f8598e90d6a`  
		Last Modified: Tue, 03 Jun 2025 14:18:22 GMT  
		Size: 36.1 KB (36057 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; ppc64le

```console
$ docker pull cassandra@sha256:93bd55af1594b5b4913a109eafb692783c3b55d8fe883fcfdf7545b579977ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184155417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2124aa094d4b89a4c36b57b24e92b2ba2bed1cf1f7f3f54c0987dec1a148e1f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Thu, 10 Apr 2025 20:24:29 GMT
ARG RELEASE
# Thu, 10 Apr 2025 20:24:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 10 Apr 2025 20:24:29 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["/bin/bash"]
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GOSU_VERSION=1.17
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_VERSION=5.0.4
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_SHA512=16de8bb78af94dabfd916825f492de7040a7311791bc1d630f14707d88f7132e51ae38dad7ebbaf13d2d154af0bdeefe318d680798b8e247ae4117cbc0e2f6df
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
VOLUME [/var/lib/cassandra]
# Thu, 10 Apr 2025 20:24:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["cassandra" "-f"]
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
	-	`sha256:b79f30d38b005774b0911c0a0640149bf11a43bdf266dc4d765433cdb9bfc8f0`  
		Last Modified: Tue, 03 Jun 2025 14:18:19 GMT  
		Size: 46.8 MB (46769833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c328778fc1a35ea67caff4d1fdb01a581b916f07c9c4d4b7758b35549536ca8`  
		Last Modified: Tue, 03 Jun 2025 14:18:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4940f46337f2d55ea79f2f6bdea1449504fc2633f81d12009da06395bb06f9a`  
		Last Modified: Tue, 03 Jun 2025 14:18:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bd7a265e71a0ade7251321d1c445c32c8b9b2d7dd92e9906f86079b5bb240f`  
		Last Modified: Tue, 03 Jun 2025 18:48:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7de41fe14860b96a0cdef39e01c0262b71f4ac7a504b58beba7983a879f674`  
		Last Modified: Tue, 03 Jun 2025 18:48:38 GMT  
		Size: 12.1 MB (12123201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cbd48e0c77498b069a6336417aff4cf6338c2ddad22411a28661420bb5ccc3`  
		Last Modified: Tue, 03 Jun 2025 18:48:40 GMT  
		Size: 904.7 KB (904735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba86a9959acced036f4dd61c9d711fc9b8094c2d654a8912c49b7da43aae6cc1`  
		Last Modified: Tue, 03 Jun 2025 18:48:48 GMT  
		Size: 72.3 MB (72293514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df35f104dbe75d7d334cbb5082ce4a22595a012b09d4082317e1e0d4305e1d3e`  
		Last Modified: Tue, 03 Jun 2025 18:48:49 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:8d0aced762eed9b8e43566c1f175cda6277761725b8b8aa9981099f5ca7b88d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49176dbc7c0647566f6eb8267714caf5534b5f194276e87682e77a6a3f5c750b`

```dockerfile
```

-	Layers:
	-	`sha256:464e12cc49f24e7bab2b2152524cee05d6b0decfd5b55112fd5a2baebb698a19`  
		Last Modified: Tue, 03 Jun 2025 18:48:58 GMT  
		Size: 4.5 MB (4488488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32230e5d78a49ae38b78a09a5fe86ec813f93a91d18d9a39e067f24a6d31b735`  
		Last Modified: Tue, 03 Jun 2025 18:48:58 GMT  
		Size: 35.9 KB (35933 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-jammy` - linux; s390x

```console
$ docker pull cassandra@sha256:726422b1f0bcfcebf4c8e2ccf305adbc77dd91b5dc39323dd656092a819dd688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172612384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61889ccbccd65de742dc5a9c84e27db10eafe1367276e63520a6c430eec8724`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Thu, 10 Apr 2025 20:24:29 GMT
ARG RELEASE
# Thu, 10 Apr 2025 20:24:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Apr 2025 20:24:29 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 10 Apr 2025 20:24:29 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["/bin/bash"]
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GOSU_VERSION=1.17
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 10 Apr 2025 20:24:29 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Apr 2025 20:24:29 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_VERSION=5.0.4
# Thu, 10 Apr 2025 20:24:29 GMT
ENV CASSANDRA_SHA512=16de8bb78af94dabfd916825f492de7040a7311791bc1d630f14707d88f7132e51ae38dad7ebbaf13d2d154af0bdeefe318d680798b8e247ae4117cbc0e2f6df
# Thu, 10 Apr 2025 20:24:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
VOLUME [/var/lib/cassandra]
# Thu, 10 Apr 2025 20:24:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 20:24:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 20:24:29 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 10 Apr 2025 20:24:29 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b083bb928961c2c7996d495007331b50b7da602cad00b66781c07e7118c9394`  
		Last Modified: Tue, 03 Jun 2025 14:13:00 GMT  
		Size: 16.1 MB (16144355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488d5d8106ce381c68977236ddb865aed01ba664d86a2a199770719a82afafa`  
		Last Modified: Tue, 03 Jun 2025 14:53:28 GMT  
		Size: 44.0 MB (43960915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0ccdf4a2e452831fcde3f5339b6b340300388219842b1405f35f287219e06`  
		Last Modified: Tue, 03 Jun 2025 14:53:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa91a862670de4da5926a34a72dd28e49dd2e804f1a4c5aac92b21b4a3a4b113`  
		Last Modified: Tue, 03 Jun 2025 14:53:24 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad36374927b93b53e309c4a53e9bfde7cb9cb691766270132a3fcfbdf22e851`  
		Last Modified: Tue, 03 Jun 2025 18:49:02 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ee8419a4e46967fe8e46a5a231b1f3ada687b2bf5bdc4353367df88ab72011`  
		Last Modified: Tue, 03 Jun 2025 18:49:05 GMT  
		Size: 11.3 MB (11258756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9fc7771a6712256aeaf4152b8b17a5acc25653dc0feff33eeae0408ac70359`  
		Last Modified: Tue, 03 Jun 2025 18:49:07 GMT  
		Size: 948.7 KB (948714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948de043824eb20686d01fdec1272301fe4eddc71b473e3b443d02ea010a5271`  
		Last Modified: Tue, 03 Jun 2025 18:49:19 GMT  
		Size: 72.3 MB (72293649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7504058ce7b4640148fa39cc96db869cfc06a728b495023751d24edbb102ba`  
		Last Modified: Tue, 03 Jun 2025 18:49:20 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:06b18e5516d61d23d8e841bc43c56a37291d8f66bec515f28787d9d0137e88d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76774eac1cb5813ce88c04a9fabc09249d661e1d56c1d5c42732974106b6fb0`

```dockerfile
```

-	Layers:
	-	`sha256:01e0513121aa9b575b195dc7b51adc8286f65ef2254207f90f7c2372a6bd3450`  
		Last Modified: Tue, 03 Jun 2025 18:49:24 GMT  
		Size: 4.5 MB (4485581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f86021456bfff8f328d9a5f29450cbc4cf1fe56dd24017fdc8257b4f1ccc9e`  
		Last Modified: Tue, 03 Jun 2025 18:49:26 GMT  
		Size: 35.9 KB (35861 bytes)  
		MIME: application/vnd.in-toto+json
