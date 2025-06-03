## `cassandra:3-jammy`

```console
$ docker pull cassandra@sha256:0329b41bfedef9e4fac5a3b027a13c8b7dd44baf2b90a061f7b2447f0e612b8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `cassandra:3-jammy` - linux; amd64

```console
$ docker pull cassandra@sha256:541f695b67504e04e521cacd1b6104068bb2ea88a87faaa05e9a1ddc1360dd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130622950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef020d7a5ad36701b8b8318dbee09fe305849a506af0fed85f6bc9adfd84827c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 24 Mar 2025 23:38:01 GMT
ARG RELEASE
# Mon, 24 Mar 2025 23:38:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Mar 2025 23:38:01 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["/bin/bash"]
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python2 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GOSU_VERSION=1.17
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_VERSION=3.11.19
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_SHA512=42d7732c2b81c65a960101d1146603d430de341adcdf8d0ffc649753a340cf64dad696050f2ec01faff5f15e726f4f2a459f0b3ac281569b957f7726f51d43e0
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
VOLUME [/var/lib/cassandra]
# Mon, 24 Mar 2025 23:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a224f9894ba047ca5b3d6023bfb9174c431179bb9c7a79ca11293c8c026479d`  
		Last Modified: Tue, 03 Jun 2025 04:16:28 GMT  
		Size: 16.1 MB (16146423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63c6d278455097ff718309185800dd81a9cfe39e91d39839fc764b8d2532174`  
		Last Modified: Tue, 03 Jun 2025 04:16:28 GMT  
		Size: 41.9 MB (41888833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f4f302542daa31d81fa33ef55c90a8da0fb4da5864f6fcf093277b67211ed6`  
		Last Modified: Tue, 03 Jun 2025 04:16:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf6cb36e84fadd539362306006afbf713e7d029a567950c7fe606db04ac9253`  
		Last Modified: Tue, 03 Jun 2025 04:16:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd2e9b5f8d4ffdc14a73b98d8096b575493481ca87b0387049851fe79ca0b44`  
		Last Modified: Tue, 03 Jun 2025 05:15:36 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f7475045a7571c6a16d8d3fbfe888f1886c6f4307ddb589195171013ccc809`  
		Last Modified: Tue, 03 Jun 2025 05:15:36 GMT  
		Size: 9.4 MB (9378249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501a58c03ba2d0b57311947d9be7dc7995227d59f9e515169af760325e9a02a8`  
		Last Modified: Tue, 03 Jun 2025 05:15:36 GMT  
		Size: 983.7 KB (983726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432efbeaf2355d5a61e78bf38946880e161a6d1d6cda69061df3bfd0b6d97688`  
		Last Modified: Tue, 03 Jun 2025 05:15:37 GMT  
		Size: 32.7 MB (32687231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f66a3c74881b2b22862bb53e15cf0db8ac9f679d9174cbd36236a603199b3f`  
		Last Modified: Tue, 03 Jun 2025 05:15:37 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a0a257c51c5bd12cdd446622f254a6cddcf1e6badffb2982130ec65d0870ee`  
		Last Modified: Tue, 03 Jun 2025 05:15:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:3-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:f04e38780a5c485dc7488b9f00600ea53f2033ef1a3ee39117c82fd5f7d91105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4542898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5194518cc4b2275c9584f8249ff6ac6ae7a661b5a22a3384293979097d542948`

```dockerfile
```

-	Layers:
	-	`sha256:e60b3d49c4ce8f02d8543c47962a49b5c8f7e34810d7727ffbf26d2aa9f8c94f`  
		Last Modified: Tue, 03 Jun 2025 05:15:36 GMT  
		Size: 4.5 MB (4504276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c6bc764e84302982a471ffa7b1ec9db367abe98deb24b3e99b73df57722311`  
		Last Modified: Tue, 03 Jun 2025 05:15:36 GMT  
		Size: 38.6 KB (38622 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:3-jammy` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:3fdd8517486e9e81b466d392d8865c78c41b7d921b9901f9a3ff3e52e0637d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124398112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c6a6fe4670d8215bfbed8003b7dca0f692c76129ebc8034b89c597282fc364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 24 Mar 2025 23:38:01 GMT
ARG RELEASE
# Mon, 24 Mar 2025 23:38:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Mar 2025 23:38:01 GMT
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["/bin/bash"]
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python2 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GOSU_VERSION=1.17
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_VERSION=3.11.19
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_SHA512=42d7732c2b81c65a960101d1146603d430de341adcdf8d0ffc649753a340cf64dad696050f2ec01faff5f15e726f4f2a459f0b3ac281569b957f7726f51d43e0
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
VOLUME [/var/lib/cassandra]
# Mon, 24 Mar 2025 23:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Fri, 30 May 2025 23:34:57 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c869906112a22f8bcfcd7276bcc7d904f46535968a6e8d65eb57940c3ac442`  
		Last Modified: Tue, 03 Jun 2025 04:20:51 GMT  
		Size: 15.9 MB (15890981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4610cfefa7479f69d838e3aa0d8a5a8874b7146dfdf0cd0847a9aa8075e59bb`  
		Last Modified: Tue, 03 Jun 2025 04:22:28 GMT  
		Size: 39.4 MB (39362854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07f26fbfd9f5801e51f72776cc878b0d2fe996432dccb0c635fcac7b6e6f840`  
		Last Modified: Tue, 03 Jun 2025 04:22:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903775714e31e9c02e706443b917793440ec34356c451247158592b3eeb6bd89`  
		Last Modified: Tue, 03 Jun 2025 04:22:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa99d98c3336a519c55ec552ac70941fc87db9c5072fe8567045115b454e743`  
		Last Modified: Tue, 03 Jun 2025 05:47:45 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552146b44248a2294ad8ea852efe92926a2de745ae66072e48c6b274c4489e3a`  
		Last Modified: Tue, 03 Jun 2025 05:47:46 GMT  
		Size: 8.9 MB (8860241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1adfb8ad2eaeb69729123d08b84249386ae35aa47a7c89b16cf4f71c01f55d`  
		Last Modified: Tue, 03 Jun 2025 05:47:46 GMT  
		Size: 950.8 KB (950772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48076f665a8d4a9d781744ec6faae3c935a79b348ff72d9d2a9374031920b82`  
		Last Modified: Tue, 03 Jun 2025 05:47:47 GMT  
		Size: 32.7 MB (32687308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d8471cb9c5cc7b33d408f09c5438c4e1aaf01bfd0794b5ec32a36ab7c1d8d5`  
		Last Modified: Tue, 03 Jun 2025 05:47:47 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30200cbb7a7db6eb12f7aa8a428ef75d9755b7bea595835d6098746791b6031c`  
		Last Modified: Tue, 03 Jun 2025 05:47:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:3-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:0e93a2f0c753262f4006eaad6bdcd21c929542e7a6309c8de47e77320a934bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4550842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde35defca3444ff7eb88ee468d800e6d1cc74e8a9d4d34fa13e2242f80241`

```dockerfile
```

-	Layers:
	-	`sha256:a8f85e7f1953f0ec6695e8891cc2867f6b80dd92d4cd295911402458c51cf914`  
		Last Modified: Tue, 03 Jun 2025 05:47:46 GMT  
		Size: 4.5 MB (4512076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92a90a7a592b863c20fc5f7f264751e1da30ddba328747c665391de9d1caf42`  
		Last Modified: Tue, 03 Jun 2025 05:47:45 GMT  
		Size: 38.8 KB (38766 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:3-jammy` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:6185e7e56eca46dca3b748898d5663b0152f3dbf3c463e1a2c418608d01f6081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127262662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6d5c14ce4a3b73c0276a203267ebe4f7acbbe75270c75007bb8d6ac9effd6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 24 Mar 2025 23:38:01 GMT
ARG RELEASE
# Mon, 24 Mar 2025 23:38:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Mar 2025 23:38:01 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["/bin/bash"]
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python2 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GOSU_VERSION=1.17
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_VERSION=3.11.19
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_SHA512=42d7732c2b81c65a960101d1146603d430de341adcdf8d0ffc649753a340cf64dad696050f2ec01faff5f15e726f4f2a459f0b3ac281569b957f7726f51d43e0
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
VOLUME [/var/lib/cassandra]
# Mon, 24 Mar 2025 23:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a012351716029262feccd21d93c2eefbe543395255454bd5fbe2c647d7688`  
		Last Modified: Mon, 05 May 2025 16:49:48 GMT  
		Size: 16.1 MB (16059611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9be09f0a4dc4412fb888fb64d1ce62bc4f2665014768f631a4b98d30e0f2ee`  
		Last Modified: Mon, 05 May 2025 16:51:08 GMT  
		Size: 40.9 MB (40879133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d9f2774a3adb3b8894d13f02a242e85d6bb2a0a75e386e2ce34286a1e643e`  
		Last Modified: Mon, 05 May 2025 16:51:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5dbc11cd2ce947e030c2f2ddbacbb3040fa54f9b080fc87583d31f8b51c891`  
		Last Modified: Mon, 05 May 2025 16:51:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74580e0531099ff29bc8ed40c498bfb01a2b40b24ea156525f6ca7e167ebe953`  
		Last Modified: Tue, 06 May 2025 00:14:58 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a6bcc421bb188d989bcd88ea84ee14d975344c6a8bbd714c287ff013dda0a1`  
		Last Modified: Tue, 06 May 2025 00:14:59 GMT  
		Size: 9.4 MB (9362509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c4915bfaa5b1d95b3b3bcb2029310e816008d26e97c817245e0063b77fa799`  
		Last Modified: Tue, 06 May 2025 00:14:59 GMT  
		Size: 914.4 KB (914448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8193f4f530db52c8c11d3760afc3cca7292d63cee7d164d249599bfd2593989`  
		Last Modified: Tue, 06 May 2025 00:15:00 GMT  
		Size: 32.7 MB (32687255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df0d1b08a6f3dbb7fdaaf12878a4426b6f6399769ef64f977ff768522fa18d`  
		Last Modified: Tue, 06 May 2025 00:15:00 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6567c1ce1a3cce2cc7c311f42a4307d5c83a55bf93ea8320ac7eec5e6ea4deab`  
		Last Modified: Tue, 06 May 2025 00:15:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:3-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:2d10f9b2e5316bd60b11a9b5120c9e0c12f6c339494d51791d7563d492149fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4511405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d26b425ab2bdf4aa0fa649819ca34a7e2016301dc04e70719655e146212ee0d`

```dockerfile
```

-	Layers:
	-	`sha256:d49fb3447aec94f5de8dbf669b24fdd3938468069985013ae9a05bdc39ab8671`  
		Last Modified: Tue, 06 May 2025 00:14:59 GMT  
		Size: 4.5 MB (4472595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3adff229a404e6657ad70d34a80097c80f8fc5c1378878cc25c355d739660c9e`  
		Last Modified: Tue, 06 May 2025 00:14:58 GMT  
		Size: 38.8 KB (38810 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:3-jammy` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6105c0d5a4d68702abfda1b43918c9e0e4f970d12ee5d83a09deb62a7966d285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136819179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba05346ecbf9ee6ec5bbda968bd12a36fe41677544b51af32727f7979dacc80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 24 Mar 2025 23:38:01 GMT
ARG RELEASE
# Mon, 24 Mar 2025 23:38:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Mar 2025 23:38:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Mar 2025 23:38:01 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["/bin/bash"]
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python2 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GOSU_VERSION=1.17
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 24 Mar 2025 23:38:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 23:38:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_VERSION=3.11.19
# Mon, 24 Mar 2025 23:38:01 GMT
ENV CASSANDRA_SHA512=42d7732c2b81c65a960101d1146603d430de341adcdf8d0ffc649753a340cf64dad696050f2ec01faff5f15e726f4f2a459f0b3ac281569b957f7726f51d43e0
# Mon, 24 Mar 2025 23:38:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
VOLUME [/var/lib/cassandra]
# Mon, 24 Mar 2025 23:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 24 Mar 2025 23:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Mar 2025 23:38:01 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 24 Mar 2025 23:38:01 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec33a1aac040bccef1eea8d18ca590aec33573ce5507988fad5185d8737eaf2`  
		Last Modified: Mon, 05 May 2025 16:36:58 GMT  
		Size: 17.6 MB (17617818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c18750931b5eb29fa59dd54dd0303d7b1a72f52f3e189f891f3972e5297b078`  
		Last Modified: Mon, 05 May 2025 16:38:48 GMT  
		Size: 41.3 MB (41259952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c38050fee91b33f35bab8a49a04ab8bd01882960bea4a32a583bccb59d0a41`  
		Last Modified: Mon, 05 May 2025 16:38:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc24b046e69ae938151e52bbd494115e5ecd801c380e9b4b27cd2be0592f3a86`  
		Last Modified: Mon, 05 May 2025 16:38:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138badaa54ae3ed1ba762f5a6cdcac579b76828d27988fec01dd6ecfbc55ff19`  
		Last Modified: Mon, 05 May 2025 21:26:42 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16e2d2ce5c776dbadc0810c6a1c7912e15e55fd5d53e7b676c4308cc3a13b9d`  
		Last Modified: Mon, 05 May 2025 21:26:43 GMT  
		Size: 9.9 MB (9900720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2eb8ec7c2a48ba94859d7298b0fb734d06c7b28e23ef1921b25ab2e0a1e0f4`  
		Last Modified: Mon, 05 May 2025 21:26:43 GMT  
		Size: 904.7 KB (904728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70f780545a0a378a2d1dcaf8f039406c9127fe88e0d9a7f3b5193773fb728fa`  
		Last Modified: Mon, 05 May 2025 21:26:44 GMT  
		Size: 32.7 MB (32687252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee24a2b120c2d532bfcb580db8eb5593d985143df3d6a4300c2587c2a32db5`  
		Last Modified: Mon, 05 May 2025 21:26:43 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed76f275cc27a196357a661b422dc5eef5584c8e2d6519f4483762bb47f6ee19`  
		Last Modified: Mon, 05 May 2025 21:26:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:3-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:4e26abc67d6ff7f453e3fbdaf8adaac4467f45595a247b84d42d0cf7f7f9d594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1298343ddac4f5c37dc3c61cceb447beb4609838aa2db456744ce9d5cd2abe2`

```dockerfile
```

-	Layers:
	-	`sha256:8f19998ee8420c01e5b7d54d55e9007b15ba9c45bbd5b02579f9d55775c2284b`  
		Last Modified: Mon, 05 May 2025 21:26:42 GMT  
		Size: 4.5 MB (4477054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbed28edc0bacca80785ce66b7e21a6eb6f880d87ff4467105fb4c8ab6076ce1`  
		Last Modified: Mon, 05 May 2025 21:26:42 GMT  
		Size: 38.7 KB (38685 bytes)  
		MIME: application/vnd.in-toto+json
