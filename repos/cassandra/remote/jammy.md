## `cassandra:jammy`

```console
$ docker pull cassandra@sha256:d5e0fd2c2c6c1bf6cb1a38a8a5cbfb6c413685f483c0d2f22e4750ace4f222f0
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

### `cassandra:jammy` - linux; amd64

```console
$ docker pull cassandra@sha256:b002c950ddf8110ae91a9c4997dd83d40203f97b19f8f77f41ebf564e953b6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154563310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51681a4211593482739031a2808f11bde671dc9ef56011c0d8a6b15df6e66c6`
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
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 20 Mar 2024 22:45:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
ENV CASSANDRA_VERSION=4.1.4
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=ddc9f4157a6e272b421850c7787b822bae36c72ab2dce711a91dc24fe18bf56f2cd91c61410243cdc0eeeb5f2a7e5419f8a531863116026996bd3f167c36a916
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
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dddff65ed2408fb8512cf4a5e475bc56396102dc76b9968c1f68a06414767b`  
		Last Modified: Tue, 16 Apr 2024 04:03:41 GMT  
		Size: 12.9 MB (12905145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb16e8676af14644501e507607834fdafbdbb7fdd8a69d8278885094b4e333`  
		Last Modified: Wed, 24 Apr 2024 19:12:16 GMT  
		Size: 47.2 MB (47186120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b2f5549f48e12a82bcad54aa3ac6004145f73ab3d487334955c2df04e5ff1`  
		Last Modified: Wed, 24 Apr 2024 19:12:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb531e0bfe578c0e91785e0e5dfba61461a5742e8f5a28819bba2ce1c2fce27`  
		Last Modified: Wed, 24 Apr 2024 19:12:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5eb10f5640e4d4ec82f77fe2dce2f9652c1421910c7c08d2ad8f5342a4ca8e`  
		Last Modified: Wed, 24 Apr 2024 19:57:21 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7e7e564dc7c66d1ddfc45ab8fdf7259ce12d27d6b4aa6494db847b9d494d9d`  
		Last Modified: Wed, 24 Apr 2024 19:57:21 GMT  
		Size: 12.4 MB (12399459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b60986b91e65b4b472b1230847dce1b182de29ffad3e0e7e3a4cf8e8a9e1c`  
		Last Modified: Wed, 24 Apr 2024 19:57:21 GMT  
		Size: 1.1 MB (1097654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4404963fbbe627017d026436eb08c6f98cfbc4c67e64bc5098cf361e335a0d`  
		Last Modified: Wed, 24 Apr 2024 19:57:22 GMT  
		Size: 50.5 MB (50531313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f14361411b5b44a5033953f6413b84d7ea3030964083a1d8b82de36b58df08`  
		Last Modified: Wed, 24 Apr 2024 19:57:22 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:2f8ebaf1c96b0efe19c8a062ed8d0c9aad4ef583415855f2d59d4b94bb8c72ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc54dac44abc757e41f36c99ee22928d6100dac5ac65481ca67cd0eb48e88ae`

```dockerfile
```

-	Layers:
	-	`sha256:c6ebd9c646e0784788fe3cd7d090fa9a74345f0126e02bebd3a5fd886ead9ba4`  
		Last Modified: Wed, 24 Apr 2024 19:57:21 GMT  
		Size: 4.1 MB (4149942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:267fb79e57c467fad122579dcae6f780a02ddc3edf61f8348e4799432b946045`  
		Last Modified: Wed, 24 Apr 2024 19:57:21 GMT  
		Size: 36.6 KB (36599 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:jammy` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:51924c16c85d56b37742f1269767326b48de24928159141840355d38ac83bc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148305318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f759ef35e5849801ad08f4b1f8335b826741abfce66b15abcfe1e0295ef975b`
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
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
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
ENV CASSANDRA_VERSION=4.1.4
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=ddc9f4157a6e272b421850c7787b822bae36c72ab2dce711a91dc24fe18bf56f2cd91c61410243cdc0eeeb5f2a7e5419f8a531863116026996bd3f167c36a916
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
	-	`sha256:8e34fc49fc731bf85ce0a83deec49456ee2c584bf1a5c472db447d8a9b9a06cb`  
		Last Modified: Fri, 12 Apr 2024 01:35:18 GMT  
		Size: 27.5 MB (27533083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fcdb6b302d1f197eacdca37c53a51b762670c261ce3f687c83be6f26ee6ab6`  
		Last Modified: Tue, 16 Apr 2024 01:53:36 GMT  
		Size: 12.5 MB (12492494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbb341e66aafffc3f937d1351ce6bb3b8daef649e4998c41a5a107aab823411`  
		Last Modified: Tue, 16 Apr 2024 01:55:26 GMT  
		Size: 45.2 MB (45209889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ce1bbe831cf0a5ba9d838937a4fbcc6821abde8224e758a6680ce2c2e3784`  
		Last Modified: Tue, 16 Apr 2024 01:55:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98720bbc4c6a507f4aabde967fd02e64fa6fb7e3250e25d3dee57f670d79c3a6`  
		Last Modified: Tue, 16 Apr 2024 01:55:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f4b5a7496f004229c99308b652a18113f11cc9f73d5a734558a8df6ff88c9`  
		Last Modified: Thu, 18 Apr 2024 18:49:45 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3268ec12d0590679ea7fc1dbd8b6c99e12fc04961ab8d3efbdf78d72ea6e49a0`  
		Last Modified: Thu, 18 Apr 2024 18:49:47 GMT  
		Size: 11.5 MB (11470238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc7484553a3629eda6fe4b1236b40073031f80f36c80fdabfd9f4998acf2a0`  
		Last Modified: Thu, 18 Apr 2024 18:49:47 GMT  
		Size: 1.1 MB (1064399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045db4faefa0c8466e6aa88594ab3d37c7692636c3da45cf12539be13f42572`  
		Last Modified: Thu, 18 Apr 2024 18:49:48 GMT  
		Size: 50.5 MB (50531380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f80bcbd0832555207ca3bf285fde49f0817228cd44c0fd4fc7da2b19ef54c`  
		Last Modified: Thu, 18 Apr 2024 18:49:48 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:06d851ee7c1e218c9eb922c7202d6b227f7ea1a5f7ea916a9d4806631ee66e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd8b3311be875bf7da0a665da3e8cb94353927d34e4936ac2284d5acbdb6d32`

```dockerfile
```

-	Layers:
	-	`sha256:48d45b23ba7bd9344f2be22e07a095ad0fe39f0bc2f6d64bb108f5309cb8b9ea`  
		Last Modified: Thu, 18 Apr 2024 18:49:46 GMT  
		Size: 4.2 MB (4151525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c118aa38180e25e78977d6a451330fc3cf7997f36089411372592963ca1af82c`  
		Last Modified: Thu, 18 Apr 2024 18:49:45 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:jammy` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8e63ccb99f71012002e1c0fdfa5b4904b243218cd5bb9087003a41a23c6068f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150588899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae1a6d39d352019ae28fc74648f6348a560aa4934b636176eb3aad820f8c461`
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
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
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
ENV CASSANDRA_VERSION=4.1.4
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=ddc9f4157a6e272b421850c7787b822bae36c72ab2dce711a91dc24fe18bf56f2cd91c61410243cdc0eeeb5f2a7e5419f8a531863116026996bd3f167c36a916
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
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ca2228c6d0dc3ad64b1c9643c4b2474deef0087c8f2cd44c278f2cfdb9455a`  
		Last Modified: Tue, 16 Apr 2024 02:57:16 GMT  
		Size: 45.4 MB (45398152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a473335e30ec91c3965dd02d96860333da7b1e44cc5f614475d7c22fd8f1dbd`  
		Last Modified: Tue, 16 Apr 2024 02:57:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fa80fda4500056a196935fcda6e1405040ee8743a7e232229c1842621d3a2f`  
		Last Modified: Tue, 16 Apr 2024 02:57:11 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898dae04681793d0fbe33fd18bd2eada4f00783cc71664584928e9bc9368679`  
		Last Modified: Thu, 18 Apr 2024 18:53:29 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8acf350d646b6a969af61b76b4c0f5c654f37bf729c5cb096a7cc7b2a1564`  
		Last Modified: Thu, 18 Apr 2024 18:53:30 GMT  
		Size: 12.4 MB (12377589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25e85b8eb67803c520404014f1cb2305a3057d76a47240992559f853bd79355`  
		Last Modified: Thu, 18 Apr 2024 18:53:30 GMT  
		Size: 1.0 MB (1029976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90dd06c5a83f82fbbb7002fa922f973044bb06c336a5ce1f5059191f5866d03`  
		Last Modified: Thu, 18 Apr 2024 18:53:32 GMT  
		Size: 50.5 MB (50531943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45144964b9b59b717a7358ea5f7c81f28dbe00f3d159ea8a7d4176c6a80366a5`  
		Last Modified: Thu, 18 Apr 2024 18:53:31 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:818e6bf890ce73fa419fb8e3eece0f6b7ade2ce7b9ad82538d3a86d79e76c85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88945badce7ac34e72bd8c9b4593946b64c5f674e25f8fb2548cd0462992132f`

```dockerfile
```

-	Layers:
	-	`sha256:e9bcd76a590341d25a63f502bd1974e98a15ced69e841fd1c80fddcdeb7bdeba`  
		Last Modified: Thu, 18 Apr 2024 18:53:29 GMT  
		Size: 4.2 MB (4150256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727b810531b33a742dbcdf10a2b5109e1a619740934e595b8ff31ce877e0d7b5`  
		Last Modified: Thu, 18 Apr 2024 18:53:28 GMT  
		Size: 35.8 KB (35801 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:jammy` - linux; ppc64le

```console
$ docker pull cassandra@sha256:57c327ecf8f6451e533d414a677e515b0613955aa7f1664647d800e0e03eb993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156613579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e9f499e0e6a214a3c30d7ee785dfb0925d2d7d0e2ed10a549d9741e247b27c`
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
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
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
ENV CASSANDRA_VERSION=4.1.4
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=ddc9f4157a6e272b421850c7787b822bae36c72ab2dce711a91dc24fe18bf56f2cd91c61410243cdc0eeeb5f2a7e5419f8a531863116026996bd3f167c36a916
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
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27059a37dad5b2569dc7e52921098941cfcaf0d5cde7c56e3a893ad1e2f636f`  
		Last Modified: Tue, 16 Apr 2024 02:49:35 GMT  
		Size: 13.8 MB (13767192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6849f23a4f1434c16f795f92fb3da9479ce10d1430d7c596b18d90ee4214c2b`  
		Last Modified: Tue, 16 Apr 2024 02:51:44 GMT  
		Size: 42.5 MB (42495113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc00b9755d5e4e76beaf4e1163bc4e996e32943f3675ac85e8ceb6752565dcbc`  
		Last Modified: Tue, 16 Apr 2024 02:51:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534f801ae63411e03e2d0e382d7872e035bc223e769ca4cc8569f6d2f01a887c`  
		Last Modified: Tue, 16 Apr 2024 02:51:35 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19eded7d4b8b0bf0468e6541024fbeb0c9f01fed90ab436a5cfb7546c73d22f`  
		Last Modified: Thu, 18 Apr 2024 19:11:24 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e07e589a9c54b9f1ef1bd91b83e24188d813e72194c5939540535cfed1c7a52`  
		Last Modified: Thu, 18 Apr 2024 19:11:26 GMT  
		Size: 13.2 MB (13208882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ea969784cfb74f648882077018ff6a6cda2c69771bd60a1a833936a8b52e08`  
		Last Modified: Thu, 18 Apr 2024 19:11:26 GMT  
		Size: 1.0 MB (1019055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377babe32453cbc271b45b7c236d648443f71a6a93e63efcf0a4668a1754e338`  
		Last Modified: Thu, 18 Apr 2024 19:11:27 GMT  
		Size: 50.5 MB (50532243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76364c28af1f6eff9f116253d83273c99619fc20581036cb05beb559a062b7f`  
		Last Modified: Thu, 18 Apr 2024 19:11:27 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:4cc6acf1c527a20d357d7385ac8a6227e341ad7cd293933782b503d0c6c3de5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4190655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff9805d4846f4e0489cf24e90890147b84c295cb779e9d55c917d228ed4d97`

```dockerfile
```

-	Layers:
	-	`sha256:21eb4aaa32b7e2a8912bd9da72f54263f3b4a9b7d9f167c0baebea403f820840`  
		Last Modified: Thu, 18 Apr 2024 19:11:25 GMT  
		Size: 4.2 MB (4154808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650baad590d9a3da918ace502a776ed555922b2802929468cb2ab0136a61c5bd`  
		Last Modified: Thu, 18 Apr 2024 19:11:24 GMT  
		Size: 35.8 KB (35847 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:jammy` - linux; s390x

```console
$ docker pull cassandra@sha256:8e271fe01f0d4a276968e5a6c382bc73dabecd3da0a287c8a5a73a50af55c6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146173563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a41aee73fde95401b527a16ed253bcfcc12ed898cd9d435da443e84a1c6a132`
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
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 20 Mar 2024 22:45:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
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
ENV CASSANDRA_VERSION=4.1.4
# Wed, 20 Mar 2024 22:45:06 GMT
ENV CASSANDRA_SHA512=ddc9f4157a6e272b421850c7787b822bae36c72ab2dce711a91dc24fe18bf56f2cd91c61410243cdc0eeeb5f2a7e5419f8a531863116026996bd3f167c36a916
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
	-	`sha256:800aa7ed945a05dec0024b71aaef6a3ed35eb8fc8eef0982ff134513d2295713`  
		Last Modified: Tue, 16 Apr 2024 01:37:03 GMT  
		Size: 28.6 MB (28637157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8b881b4864a2e46e88ac5ec37c0b320ca30be290b791f04917dcc056809f3b`  
		Last Modified: Tue, 16 Apr 2024 01:50:44 GMT  
		Size: 13.0 MB (12986387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f41d0ade66ae0cbbac6954f7e6cb27ec29a3bedfdffeb9b235f5fd3925520`  
		Last Modified: Tue, 16 Apr 2024 01:51:19 GMT  
		Size: 40.8 MB (40766133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe4d7eb3f743d9e91fa6a779c0e996fbc86c104154c5070cde03b8840eceb7e`  
		Last Modified: Tue, 16 Apr 2024 01:51:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7aa937dc5864318cd995372e5d54863e03d67bedbe274df435a2a678380965`  
		Last Modified: Tue, 16 Apr 2024 01:51:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08a56076694145ed026659ee593606290bd9d23112f53677ffb6c0dc69ac9c1`  
		Last Modified: Tue, 16 Apr 2024 17:25:18 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31a7d156a747e1cbceca7a402b341c3ec81255fdf4f89e3b25fc220ce414272`  
		Last Modified: Tue, 16 Apr 2024 17:25:19 GMT  
		Size: 12.2 MB (12184224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b758be916ec389866416631e7f9c740f03c4fac5de2b7a36fd7c2668915873`  
		Last Modified: Tue, 16 Apr 2024 17:25:19 GMT  
		Size: 1.1 MB (1064218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba711c31a804835b3109b4b31d1dd6266590d37e946794b3154a41f48df607b`  
		Last Modified: Tue, 16 Apr 2024 17:25:21 GMT  
		Size: 50.5 MB (50531603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4f32d3da5f899d0fbac88ced485125c9898fffba7af24471a55b16f70172b0`  
		Last Modified: Tue, 16 Apr 2024 17:25:20 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:jammy` - unknown; unknown

```console
$ docker pull cassandra@sha256:aedb85bd4e858ee9be6717e9f8c20f59cfa2b37de8ec66118e437e61a281c412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4188653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ffe27010cff8186ed3aede77a02e395dd97073a4b1b68eb30b06cd3016fa63`

```dockerfile
```

-	Layers:
	-	`sha256:8d85ac40f7488912d462b7321da1b56b9246440065bf2c5efd151b90fd19f45a`  
		Last Modified: Tue, 16 Apr 2024 17:25:19 GMT  
		Size: 4.2 MB (4152057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa916b50886964edb9182a10c6add5867b4f1e7e94958e74165fd38427639f94`  
		Last Modified: Tue, 16 Apr 2024 17:25:18 GMT  
		Size: 36.6 KB (36596 bytes)  
		MIME: application/vnd.in-toto+json
