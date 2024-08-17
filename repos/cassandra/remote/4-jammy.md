## `cassandra:4-jammy`

```console
$ docker pull cassandra@sha256:4f50a43c654ac19507699a7354d6bbfd580f6a7570f7aa5a0e0454de6d065f0a
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

### `cassandra:4-jammy` - linux; amd64

```console
$ docker pull cassandra@sha256:fbfcffc259b2276638adfac19e808640254dc16ad5cc42315c9d05096abd8ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154562135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93d56e2abf3c766fa0d7bed83750983ce83c021978011c192d572a346bb3f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 20 May 2024 14:24:27 GMT
ARG RELEASE
# Mon, 20 May 2024 14:24:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 May 2024 14:24:27 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 20 May 2024 14:24:27 GMT
CMD ["/bin/bash"]
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 May 2024 14:24:27 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV GOSU_VERSION=1.17
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_VERSION=4.1.5
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_SHA512=9b76bcba188c34de0bec7327adb5d4d571df7ac485788e577974f361422c229df17d90925eff20d97090581c01756bc7a7fc8b8f01f99297c90276240e27ebeb
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 20 May 2024 14:24:27 GMT
VOLUME [/var/lib/cassandra]
# Mon, 20 May 2024 14:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 20 May 2024 14:24:27 GMT
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
	-	`sha256:a880dee0d8e92fc9854fd2480b4c183eba1429a09ed63d9e60edad44fa8edf01`  
		Last Modified: Sat, 17 Aug 2024 01:12:06 GMT  
		Size: 47.2 MB (47198423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5deab9cbd68168c5b0fe4bf55d9d3be31e0a75abb267f5e59e8973d11616df`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8f4b62f2e68572eaac926164f20363d2538aab091cf56cf29b9e83ddba7d83`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffd9047efd61835de86d795b0c980970706c66a737b65b4d12377e8de0e6e4a`  
		Last Modified: Sat, 17 Aug 2024 01:59:20 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d0a94816d1012e72776a453eff4efd6d3a8c04aef82a3fa4d991f760df058`  
		Last Modified: Sat, 17 Aug 2024 01:59:21 GMT  
		Size: 12.4 MB (12407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de9824387bb3f1ecc274f263e2c10f372f6927d4f5797ac8b4bc8f236a4ab5c`  
		Last Modified: Sat, 17 Aug 2024 01:59:20 GMT  
		Size: 1.1 MB (1097783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee736ebefe06ef28248b4ef49efc830a42678941eab41f5a88609c33535d91e`  
		Last Modified: Sat, 17 Aug 2024 01:59:22 GMT  
		Size: 50.5 MB (50541921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61c5ede343a5692cbb1b934b28ced616bd413c0f6a46e1eb01fccaa087b994c`  
		Last Modified: Sat, 17 Aug 2024 01:59:21 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:ba400a332db97d66e5bf972fae65b6cba195ed4265e15658d5a2b5d8d5e639ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4226914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311c47ce6dbf353825e7314fd5c39102d4fde825a50cb8b8ca84627145e497b7`

```dockerfile
```

-	Layers:
	-	`sha256:a3a58282664e2d827e7f53e6c99f292905957534f33c84618e965f1c71bd5057`  
		Last Modified: Sat, 17 Aug 2024 01:59:20 GMT  
		Size: 4.2 MB (4191076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86e1f707cef99c3378d70ad8617fbeab342a008f1bfcd75c69ed3d9b818aeac`  
		Last Modified: Sat, 17 Aug 2024 01:59:20 GMT  
		Size: 35.8 KB (35838 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-jammy` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:c967c23f845f81a2c2c2938b1ae984003608cd4da1baea8c42567d29e573d44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148407635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db54be29a4703a6d9777719316014384f700dc4197115a7c6ab48a4023c57a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 20 May 2024 14:24:27 GMT
ARG RELEASE
# Mon, 20 May 2024 14:24:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 May 2024 14:24:27 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Mon, 20 May 2024 14:24:27 GMT
CMD ["/bin/bash"]
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 May 2024 14:24:27 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV GOSU_VERSION=1.17
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_VERSION=4.1.5
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_SHA512=9b76bcba188c34de0bec7327adb5d4d571df7ac485788e577974f361422c229df17d90925eff20d97090581c01756bc7a7fc8b8f01f99297c90276240e27ebeb
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 20 May 2024 14:24:27 GMT
VOLUME [/var/lib/cassandra]
# Mon, 20 May 2024 14:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 20 May 2024 14:24:27 GMT
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
	-	`sha256:63527976b804f01db443c1dbba8c35f604b92228fec66c66227a2e1ad44be0dc`  
		Last Modified: Sat, 17 Aug 2024 01:37:52 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffb07476a5d9f78c6a00fb40d88e5e11119746a4655f06063db59b27e7e28d1`  
		Last Modified: Sat, 17 Aug 2024 04:08:36 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92236710e6398ffef7b8db665b2b8008e83d8a0807ed1915821c7c7c74e9fd1a`  
		Last Modified: Sat, 17 Aug 2024 04:08:37 GMT  
		Size: 11.5 MB (11477674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ad5a6020e9664d3eac66891f5d4df982907031036c999c84623f965126179a`  
		Last Modified: Sat, 17 Aug 2024 04:08:37 GMT  
		Size: 1.1 MB (1064623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6fa2025dbe0e51d45183aa687c2c60013b2723841a5fd5a1b712607627078c`  
		Last Modified: Sat, 17 Aug 2024 04:08:39 GMT  
		Size: 50.5 MB (50542029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093715493c5ed5f1d436f03f0b7e1502ccaf32dc7bd22a5957847a4cdad58939`  
		Last Modified: Sat, 17 Aug 2024 04:08:38 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:fcf452c94029d6786abca96212a09e34ac77a278ee1c9ca47f3cc62450e24f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c340b586b9efe472c59f165885a86c18d6f8d956f769dba0bbb3576dad2f756`

```dockerfile
```

-	Layers:
	-	`sha256:eb055d5e46055731fa37e5baf24e13fda909beb0022abe7a49a273b49bdf8c1e`  
		Last Modified: Sat, 17 Aug 2024 04:08:36 GMT  
		Size: 4.2 MB (4192516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33d1ed0c1898cc41fd58c26f26ec8e76336c77007ac088e02ad1aade1b3fe4a`  
		Last Modified: Sat, 17 Aug 2024 04:08:36 GMT  
		Size: 36.0 KB (35978 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-jammy` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:cdf528dbe63a748b6b5db38de180a4ac410328711a8eeaaac6a084a290d29142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150724184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c7b1b37009fe31015aadff037eb435d4c521816f989c88adedb9d20393858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 20 May 2024 14:24:27 GMT
ARG RELEASE
# Mon, 20 May 2024 14:24:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 May 2024 14:24:27 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 20 May 2024 14:24:27 GMT
CMD ["/bin/bash"]
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 May 2024 14:24:27 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV GOSU_VERSION=1.17
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_VERSION=4.1.5
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_SHA512=9b76bcba188c34de0bec7327adb5d4d571df7ac485788e577974f361422c229df17d90925eff20d97090581c01756bc7a7fc8b8f01f99297c90276240e27ebeb
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 20 May 2024 14:24:27 GMT
VOLUME [/var/lib/cassandra]
# Mon, 20 May 2024 14:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 20 May 2024 14:24:27 GMT
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
	-	`sha256:6d4dbb8ab7ebb70bbdbb49ab2085d99ae87968ea251f304e9fa059e7155f13e5`  
		Last Modified: Sat, 17 Aug 2024 01:35:00 GMT  
		Size: 45.6 MB (45557024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed86303b2ff16bd4b17f7c739a9055711b72b99e566885505d9258cd44e26c`  
		Last Modified: Sat, 17 Aug 2024 01:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a39144a3e0f2aebca5cbfc033c449426203033eec38601341a0e8b3ab494ce9`  
		Last Modified: Sat, 17 Aug 2024 01:34:55 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf032317ce36bc62ec8fa4e023c6c58db26838342356f4afcc6e6557db1803f7`  
		Last Modified: Sat, 17 Aug 2024 05:45:13 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc3f5f0c0d48495a4ef6e8c6eaa322be8ccc4126d54958d0ef84323ce462a36`  
		Last Modified: Sat, 17 Aug 2024 05:45:14 GMT  
		Size: 12.4 MB (12379918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6858a6d4f7815fe29fde2f36c57a880e9b54abe152f31aec3963a9c4b5b089b`  
		Last Modified: Sat, 17 Aug 2024 05:45:14 GMT  
		Size: 1.0 MB (1029713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615898e50997634eeef991ccc208e0f0f9c0a996bdf0875b9b76bc64d2c22fcd`  
		Last Modified: Sat, 17 Aug 2024 05:45:15 GMT  
		Size: 50.5 MB (50542141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5ec0e56ca513461227cd6b91838761372d2567fe43a8bc4ceebf523c4c24a2`  
		Last Modified: Sat, 17 Aug 2024 05:45:15 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:cddc084c2e48df0bcc5f900aa914b822c42a5c3c0a238bcfc5f62a5ad439b3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60de12e838d6d44eb8b992ebe30055e5390eac02b12f45638d95244cb40fb1b`

```dockerfile
```

-	Layers:
	-	`sha256:8fd329d584dbe54077fbdb7ea3f59faf9b34bfa2b8b30a606ab18cef51203e2b`  
		Last Modified: Sat, 17 Aug 2024 05:45:13 GMT  
		Size: 4.2 MB (4191475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a1836aefd8801b6e5e2c84179c96df7d3cf624460a39a09e5a7a861879b67b7`  
		Last Modified: Sat, 17 Aug 2024 05:45:13 GMT  
		Size: 36.2 KB (36203 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-jammy` - linux; ppc64le

```console
$ docker pull cassandra@sha256:5e46bbeb9751ee58fa6916aefd79590c820019eac392cb3ecc2430afacb7603c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156727211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5f994269bdaae1abaacb4da90d0c60d40099c12252f2ca3bfdf8085ae410ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 20 May 2024 14:24:27 GMT
ARG RELEASE
# Mon, 20 May 2024 14:24:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 May 2024 14:24:27 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 20 May 2024 14:24:27 GMT
CMD ["/bin/bash"]
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 May 2024 14:24:27 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV GOSU_VERSION=1.17
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_VERSION=4.1.5
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_SHA512=9b76bcba188c34de0bec7327adb5d4d571df7ac485788e577974f361422c229df17d90925eff20d97090581c01756bc7a7fc8b8f01f99297c90276240e27ebeb
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 20 May 2024 14:24:27 GMT
VOLUME [/var/lib/cassandra]
# Mon, 20 May 2024 14:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 20 May 2024 14:24:27 GMT
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
	-	`sha256:f4b50c4b0fab19a16a502b1681ff9177a05eed203d81aa04a49df18907898c34`  
		Last Modified: Sat, 17 Aug 2024 01:01:26 GMT  
		Size: 42.7 MB (42652048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338034862f9398ecf41f81f3eb5a9837d4cbe84271d6141f09462837e4a51105`  
		Last Modified: Sat, 17 Aug 2024 01:01:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3246224783f599f6a4153370a399e93e155ed12e7ec6a1628c035d5f16a802bc`  
		Last Modified: Sat, 17 Aug 2024 01:01:19 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98359b2a5f420e39731bea38638f901c75c70eb9c66983b03adc7e721677f26e`  
		Last Modified: Sat, 17 Aug 2024 04:12:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d115064b5698208c6b1ea0f745f89e18d272fa0cce80c0c413de8029e7249cc8`  
		Last Modified: Sat, 17 Aug 2024 04:12:51 GMT  
		Size: 13.2 MB (13205927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e030a30754a196d88676fbbeafe3fed7cf7a742732b5e053199c6d7cb0a1d4`  
		Last Modified: Sat, 17 Aug 2024 04:12:50 GMT  
		Size: 1.0 MB (1018960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b8a02a1214a6d79d35d8d233a1fcdee952fcd4c81904c7a5b288d9c9ea393`  
		Last Modified: Sat, 17 Aug 2024 04:12:52 GMT  
		Size: 50.5 MB (50542574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a217f2fad19f65e0d8c998a09df7f858d53488184e9e33e95c03ae3160e0d3f`  
		Last Modified: Sat, 17 Aug 2024 04:12:51 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:e96164cd4d72843578b3eaef5205854b881aea4e3846655c552e3f3c5a22e0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4231848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1b7ce887dc749af101123d8fb35736c4318fbcbe2b4ace4cd1ebb981e69a50`

```dockerfile
```

-	Layers:
	-	`sha256:267b3504c7b5e9a84a5d2f874424d763528b21c4f3f8c0eb047aba2b0776bfb0`  
		Last Modified: Sat, 17 Aug 2024 04:12:50 GMT  
		Size: 4.2 MB (4195942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0356bb9e725834c0ac054641226fcf3a94cb31e4f9979e39efb6d3779e9e499d`  
		Last Modified: Sat, 17 Aug 2024 04:12:49 GMT  
		Size: 35.9 KB (35906 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-jammy` - linux; s390x

```console
$ docker pull cassandra@sha256:38de482eeaf802a886b539a2ce0ba57bf11ee69bfd77a29bdc697fb4c0ec3376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146206228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da58d8b805f4dbde4b3f1d7fc64bca417492c57b5d98c0b13b23c6d8f0ff8cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 20 May 2024 14:24:27 GMT
ARG RELEASE
# Mon, 20 May 2024 14:24:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 May 2024 14:24:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 May 2024 14:24:27 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Mon, 20 May 2024 14:24:27 GMT
CMD ["/bin/bash"]
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 May 2024 14:24:27 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV GOSU_VERSION=1.17
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Mon, 20 May 2024 14:24:27 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 May 2024 14:24:27 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_VERSION=4.1.5
# Mon, 20 May 2024 14:24:27 GMT
ENV CASSANDRA_SHA512=9b76bcba188c34de0bec7327adb5d4d571df7ac485788e577974f361422c229df17d90925eff20d97090581c01756bc7a7fc8b8f01f99297c90276240e27ebeb
# Mon, 20 May 2024 14:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Mon, 20 May 2024 14:24:27 GMT
VOLUME [/var/lib/cassandra]
# Mon, 20 May 2024 14:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 May 2024 14:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 May 2024 14:24:27 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Mon, 20 May 2024 14:24:27 GMT
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
	-	`sha256:d74526df9c0366d211932ec56c4d441e07aaf847b38fc0ff252ab750aa945325`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c439f75bd8f90e14da9f4a76fcc816fcf82999ae2144b2e2d37075fbdfc170ad`  
		Last Modified: Sat, 17 Aug 2024 04:08:35 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407b149cb02689e3991a8873c0b90254c6f8df99136ec8a5088801c381b79f33`  
		Last Modified: Sat, 17 Aug 2024 04:08:36 GMT  
		Size: 12.2 MB (12184032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a830aa0252efc0dcf1dbb4c5e4c6e97324fe8c8cb5412182d2e1d5d30be14cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:36 GMT  
		Size: 1.1 MB (1064202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ecfb7f5ea52547f529f8458cfc7d49c862703854bbe9144ec727a84cf40b86`  
		Last Modified: Sat, 17 Aug 2024 04:08:37 GMT  
		Size: 50.5 MB (50542196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6c7113823228363deadc78a41f7681ca6baea2c6cf27fac0052e3275147243`  
		Last Modified: Sat, 17 Aug 2024 04:08:36 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:0127aff12d430a6d26b82191f708074de1d37ca7a139f0c84c6f5a85e132e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0140fda5d9f66906f7de03d390a216543f3e1b710649ebfa026d02708b8f1c9a`

```dockerfile
```

-	Layers:
	-	`sha256:72d8c1fb52e81a446c767f18adadefbd8f2d9493986420a8cc36173883200a3a`  
		Last Modified: Sat, 17 Aug 2024 04:08:35 GMT  
		Size: 4.2 MB (4192139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cdff7f8f908a1ebe2d3f3dc6e5387f40a41f35d6386f8dfdb628362ef851cb0`  
		Last Modified: Sat, 17 Aug 2024 04:08:35 GMT  
		Size: 35.8 KB (35838 bytes)  
		MIME: application/vnd.in-toto+json
