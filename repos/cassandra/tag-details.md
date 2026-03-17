<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `cassandra`

-	[`cassandra:4`](#cassandra4)
-	[`cassandra:4-bookworm`](#cassandra4-bookworm)
-	[`cassandra:4.0`](#cassandra40)
-	[`cassandra:4.0-bookworm`](#cassandra40-bookworm)
-	[`cassandra:4.0.19`](#cassandra4019)
-	[`cassandra:4.0.19-bookworm`](#cassandra4019-bookworm)
-	[`cassandra:4.1`](#cassandra41)
-	[`cassandra:4.1-bookworm`](#cassandra41-bookworm)
-	[`cassandra:4.1.10`](#cassandra4110)
-	[`cassandra:4.1.10-bookworm`](#cassandra4110-bookworm)
-	[`cassandra:5`](#cassandra5)
-	[`cassandra:5-bookworm`](#cassandra5-bookworm)
-	[`cassandra:5.0`](#cassandra50)
-	[`cassandra:5.0-bookworm`](#cassandra50-bookworm)
-	[`cassandra:5.0.6`](#cassandra506)
-	[`cassandra:5.0.6-bookworm`](#cassandra506-bookworm)
-	[`cassandra:bookworm`](#cassandrabookworm)
-	[`cassandra:latest`](#cassandralatest)

## `cassandra:4`

```console
$ docker pull cassandra@sha256:5e620e10efaeaf936ae73963e594c98df88f0cd468582d7ceb324cbb864f0604
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

### `cassandra:4` - linux; amd64

```console
$ docker pull cassandra@sha256:54589570846dcb96b39186721893246c7e97584ea6fe4e0ae02cac261d0833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84025b614066c7356b7225de9d9b8e2fe5941629d0a99aac0c6c55a023aebe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc147edb2180a007f53a18e50d643052e6b7d656281b7c5ab3cf0d70f28a0940`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d670879c4857cef3fb10b38721fa158f588e4ddd85896eff28c242a0989df`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.1 MB (18149851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b923e722f511a50b6bff10ba3b92293274cd6413d772dda4a689c6bbe0c7a6`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04daf4a2aade34353992d9096263af2ef8fd11aeafdd5b73dedbb26ef8f9b9`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.3 MB (47295070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44524ed1b03fe00c98b2fbf50dbe6727807cfc0f18210d64c9f701cbf245bff`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a8489d07ae41ed9e2d6345a0c13e6034112415f26c487f3992a0f16cb1499`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 52.9 MB (52914394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0abca5db3e631dd5135204bd9a6bc8d73612f4f80a6bdae493f43c439ac92`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:2d23bb7bcefda8d9274d396b12fbd83ddc56057015c6dca70b14a85cebf69e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc84b3792ade99a4755b76df1dccf5cd5f54173164c57dfc7e76a9e6610941b`

```dockerfile
```

-	Layers:
	-	`sha256:110edf9777d29d3f663616de421dec295c4cb30974ab58fb4125ebeade444a80`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5f100b6de7a3a1047993df533e2fbab334a1aa46a279d53870a1c01feb0f48`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:024f89d5c5131ffd64f2cd879a463046786d584139b4ecf67e95a40a291e379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139713787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a392bb249cde12480a26c56f793ebe209efbf7b2794c6d420f96535c5bdc2ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d1c799df811c08290bdbbcf494a179577f307a9102358ba6233490f8dc869`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678ee1b5b5ab49ae78fde02726ed843258da79044760e0644c8004906d475e05`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 16.2 MB (16209314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862025c91bde921b5cbc7345a2ace01654d8563870616a5ad60305da39e0a1`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.2 MB (1232648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4f13334e150c465bb2a85a4cf7c1b6f8cb3eb112bb98b7cdee3ed7b9928be`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 45.4 MB (45413511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3bf184cc7184732ad3551c915100fdac47df4e8d0bbc403340bbb61ef83f8e`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662617661e0afde65f790710b7bc09ebc4a41f8a331b01f474a53e531930d88`  
		Last Modified: Tue, 17 Mar 2026 02:49:44 GMT  
		Size: 52.9 MB (52914512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e3d16726bac9043b08884dd54073770b70e21c1adac99f556d2ec78c0c9b3f`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:630dc769d37bf584cf595776073b772707a78cd76e5418c2155c7e9c030e683b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f66e9f1c73ded8a88e09ee918c043bd04e5bcb19bf6ef00d32440ad2daad72`

```dockerfile
```

-	Layers:
	-	`sha256:de8104fcc429251fb1fda9ed26bd0aca4b09c7552f033abdbde199c35c3c757e`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6fc66ca6b8d54f7bfaf8dfc95c10b0dbdad4913cb0c4d850254ab3cc365de7`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:ada7dcfbd6cd0e8fe614285f90be65f2b609850c6447fb9d34d49af0071721d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081c9417c8f5c18e12b951d84e4faac1d96f3a233d3970ffb7607ad802fda4be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:49 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df339bed319fdd8de6f4208b5f9d4c55dff7d6048859b27073939d45ca9993a3`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be127bac61685f5e5c9c08d6d8dc2fdded5d51f05879f079878c790fa4ed21`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 17.9 MB (17888514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a10a35f57460bf17e201ca809b66febd1b0ad9c4eb2ce18eb86fb217f007963`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 1.2 MB (1220054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c00ad6d00bfaab00e033f6ea96dd01a532ac6fb496f20c6f03e708afbe080`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 45.6 MB (45617060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4000f376411bd7a134155344d5d0973f6572fea39089439e1346a89a154c50f7`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab142b63d3d02bdbe0c588f513d60a7165cb69fd41decfa7f7dc95be45f70713`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 52.9 MB (52914363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812da46cd96e726eb6b3268a352d8a66118b3b26f09483823d3379e7a428a939`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:79c9891cd92bccc8bcc390e203f0a3937eeb6677c87476510af40d3f53cf642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05f52e0f266413f489f6fcaa908ee03b8ce88100258d45d82f89ef18ab672f`

```dockerfile
```

-	Layers:
	-	`sha256:acb60ded2b756e0e9e3724926123424cbf0c8a18dec94d2e281af07ede67f08a`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd93984ef667b433881565357fb7b4f33d68039364e7e6cfe7f3ede4fd5a8d`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6eb375e1e70b4d0c1043560740cf35e1c092a57c789a1b5ab3b73e4712573369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148456276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78eb4cceb4186629456b4d85662ceb85552043b42815b0040686a900cdfae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 18:03:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:04 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:04 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e9ab86808875414f35ec4d4f6e5fb738e11e915034dccd7bd2d0fc20b6641`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 52.9 MB (52914659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a95eebf8bcf16c01a7abb0f6de19b873d1cb1b6c6ba8cfa0ef40832a2ecfc`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:a654bf8943c1706a9014e08dacbba0394522abda99a17523b8190c63c6d3f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9333b30d3b9b096019f8c876371b3e66308a7f84db7a9ac0f0a8be473315a`

```dockerfile
```

-	Layers:
	-	`sha256:6316c32cb26befe75f4a43768136066f477a297cfddeb850898cbddcfb7636f6`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f89cc1f6410a780d2a4da15aab47082e308d9d59afe5ab5c6299fb90275e9d`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 36.4 KB (36397 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; s390x

```console
$ docker pull cassandra@sha256:fc8eeff22bd21e4deae972ca136b304d95bdcb68733a82b5c043000454dced00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563513928131e9a28cfa9c225b98313c49336f68b0957cc23e9c353603bb4a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 11:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:30 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26393507fa42481ea67f620f43fb8c66f3130fc06d9bdbf849439834a274b08`  
		Last Modified: Tue, 17 Mar 2026 11:25:28 GMT  
		Size: 52.9 MB (52915323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c03bd184e759fde5abc9fdcb16f46c8fbad84289541eb9beffcfbb98ccabdbd`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:fda4630ac60a4304b85bf07516b53fe7adceacc53946912744b05eb5c51ec207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e4f376d1e28a2f1b92ab6288da8668d4954bf485dd1b570979c3e4df45588c`

```dockerfile
```

-	Layers:
	-	`sha256:ebc54e94368edbce6a1ae499c26da64270991b6db7da6e7dfc96523713ae303e`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cfa8490820696b7f33a860d5db0c9c958202ec9211f478a486dba079714d9`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4-bookworm`

```console
$ docker pull cassandra@sha256:5e620e10efaeaf936ae73963e594c98df88f0cd468582d7ceb324cbb864f0604
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

### `cassandra:4-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:54589570846dcb96b39186721893246c7e97584ea6fe4e0ae02cac261d0833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84025b614066c7356b7225de9d9b8e2fe5941629d0a99aac0c6c55a023aebe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc147edb2180a007f53a18e50d643052e6b7d656281b7c5ab3cf0d70f28a0940`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d670879c4857cef3fb10b38721fa158f588e4ddd85896eff28c242a0989df`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.1 MB (18149851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b923e722f511a50b6bff10ba3b92293274cd6413d772dda4a689c6bbe0c7a6`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04daf4a2aade34353992d9096263af2ef8fd11aeafdd5b73dedbb26ef8f9b9`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.3 MB (47295070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44524ed1b03fe00c98b2fbf50dbe6727807cfc0f18210d64c9f701cbf245bff`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a8489d07ae41ed9e2d6345a0c13e6034112415f26c487f3992a0f16cb1499`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 52.9 MB (52914394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0abca5db3e631dd5135204bd9a6bc8d73612f4f80a6bdae493f43c439ac92`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:2d23bb7bcefda8d9274d396b12fbd83ddc56057015c6dca70b14a85cebf69e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc84b3792ade99a4755b76df1dccf5cd5f54173164c57dfc7e76a9e6610941b`

```dockerfile
```

-	Layers:
	-	`sha256:110edf9777d29d3f663616de421dec295c4cb30974ab58fb4125ebeade444a80`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5f100b6de7a3a1047993df533e2fbab334a1aa46a279d53870a1c01feb0f48`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:024f89d5c5131ffd64f2cd879a463046786d584139b4ecf67e95a40a291e379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139713787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a392bb249cde12480a26c56f793ebe209efbf7b2794c6d420f96535c5bdc2ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d1c799df811c08290bdbbcf494a179577f307a9102358ba6233490f8dc869`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678ee1b5b5ab49ae78fde02726ed843258da79044760e0644c8004906d475e05`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 16.2 MB (16209314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862025c91bde921b5cbc7345a2ace01654d8563870616a5ad60305da39e0a1`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.2 MB (1232648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4f13334e150c465bb2a85a4cf7c1b6f8cb3eb112bb98b7cdee3ed7b9928be`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 45.4 MB (45413511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3bf184cc7184732ad3551c915100fdac47df4e8d0bbc403340bbb61ef83f8e`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662617661e0afde65f790710b7bc09ebc4a41f8a331b01f474a53e531930d88`  
		Last Modified: Tue, 17 Mar 2026 02:49:44 GMT  
		Size: 52.9 MB (52914512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e3d16726bac9043b08884dd54073770b70e21c1adac99f556d2ec78c0c9b3f`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:630dc769d37bf584cf595776073b772707a78cd76e5418c2155c7e9c030e683b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f66e9f1c73ded8a88e09ee918c043bd04e5bcb19bf6ef00d32440ad2daad72`

```dockerfile
```

-	Layers:
	-	`sha256:de8104fcc429251fb1fda9ed26bd0aca4b09c7552f033abdbde199c35c3c757e`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6fc66ca6b8d54f7bfaf8dfc95c10b0dbdad4913cb0c4d850254ab3cc365de7`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:ada7dcfbd6cd0e8fe614285f90be65f2b609850c6447fb9d34d49af0071721d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081c9417c8f5c18e12b951d84e4faac1d96f3a233d3970ffb7607ad802fda4be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:49 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df339bed319fdd8de6f4208b5f9d4c55dff7d6048859b27073939d45ca9993a3`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be127bac61685f5e5c9c08d6d8dc2fdded5d51f05879f079878c790fa4ed21`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 17.9 MB (17888514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a10a35f57460bf17e201ca809b66febd1b0ad9c4eb2ce18eb86fb217f007963`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 1.2 MB (1220054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c00ad6d00bfaab00e033f6ea96dd01a532ac6fb496f20c6f03e708afbe080`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 45.6 MB (45617060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4000f376411bd7a134155344d5d0973f6572fea39089439e1346a89a154c50f7`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab142b63d3d02bdbe0c588f513d60a7165cb69fd41decfa7f7dc95be45f70713`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 52.9 MB (52914363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812da46cd96e726eb6b3268a352d8a66118b3b26f09483823d3379e7a428a939`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:79c9891cd92bccc8bcc390e203f0a3937eeb6677c87476510af40d3f53cf642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05f52e0f266413f489f6fcaa908ee03b8ce88100258d45d82f89ef18ab672f`

```dockerfile
```

-	Layers:
	-	`sha256:acb60ded2b756e0e9e3724926123424cbf0c8a18dec94d2e281af07ede67f08a`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd93984ef667b433881565357fb7b4f33d68039364e7e6cfe7f3ede4fd5a8d`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6eb375e1e70b4d0c1043560740cf35e1c092a57c789a1b5ab3b73e4712573369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148456276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78eb4cceb4186629456b4d85662ceb85552043b42815b0040686a900cdfae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 18:03:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:04 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:04 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e9ab86808875414f35ec4d4f6e5fb738e11e915034dccd7bd2d0fc20b6641`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 52.9 MB (52914659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a95eebf8bcf16c01a7abb0f6de19b873d1cb1b6c6ba8cfa0ef40832a2ecfc`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a654bf8943c1706a9014e08dacbba0394522abda99a17523b8190c63c6d3f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9333b30d3b9b096019f8c876371b3e66308a7f84db7a9ac0f0a8be473315a`

```dockerfile
```

-	Layers:
	-	`sha256:6316c32cb26befe75f4a43768136066f477a297cfddeb850898cbddcfb7636f6`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f89cc1f6410a780d2a4da15aab47082e308d9d59afe5ab5c6299fb90275e9d`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 36.4 KB (36397 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:fc8eeff22bd21e4deae972ca136b304d95bdcb68733a82b5c043000454dced00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563513928131e9a28cfa9c225b98313c49336f68b0957cc23e9c353603bb4a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 11:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:30 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26393507fa42481ea67f620f43fb8c66f3130fc06d9bdbf849439834a274b08`  
		Last Modified: Tue, 17 Mar 2026 11:25:28 GMT  
		Size: 52.9 MB (52915323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c03bd184e759fde5abc9fdcb16f46c8fbad84289541eb9beffcfbb98ccabdbd`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:fda4630ac60a4304b85bf07516b53fe7adceacc53946912744b05eb5c51ec207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e4f376d1e28a2f1b92ab6288da8668d4954bf485dd1b570979c3e4df45588c`

```dockerfile
```

-	Layers:
	-	`sha256:ebc54e94368edbce6a1ae499c26da64270991b6db7da6e7dfc96523713ae303e`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cfa8490820696b7f33a860d5db0c9c958202ec9211f478a486dba079714d9`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0`

```console
$ docker pull cassandra@sha256:1fa3204f4be6ca223886d763c1dd7083bbf19fe678cb8dce25420ae09c7db354
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

### `cassandra:4.0` - linux; amd64

```console
$ docker pull cassandra@sha256:f42f1244e962ee3c2ccf20393950d161c57863b599634b4bc3c44e5d3018130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bc5a2f811ce824bb4ade64907d8ddc05a15f3350ce9f95ee288ff8b517da8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:18 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:55:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d836223b9c9f5cc73a05206fb58837ffb326baf90a60a3ddaf5852d4744bf9`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96abcf7decece82c84be1fdcfe2961a210de883e443b69f490682b077039cf1b`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 18.2 MB (18150047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9c0e50cc5660757aaa73da587aecdfc8cbbed4d5bf80bd633e29ede25d869`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.3 MB (1266589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106b4f5f45a273a5076ebb591bfe22e18c445e9c4870a4ab5696020f68addf58`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 47.3 MB (47295078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ce6a5606c87fdfb7692b2ead75fd33061fdd82d31c4a5d80c4c6d0b5064856`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20e88120a30c7c368f5ba7be4a4fa03521a5cbcda7924776bd460d5c5349ffe`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffa86e8f62a386ae9915d19e94a84f2f2dd979304f7b6ef10080a3d4a44d284`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:a795374db9aeb9cb06a6037c5daef7e1779628d61b3c3c567a2c3abd3c1238b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451ba2f333c122664b8457cbc4dab1a59493dafe83eb3891cf11b4f291f8f083`

```dockerfile
```

-	Layers:
	-	`sha256:ca825978cdbc0feeb26d176810dce5f3d1f821a238eae06959be351921535b52`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8c2bde62a4784489d66372b381c052d77c8db1207feac5e2206f05c42f9b2`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:48664a8fd3f8b057e54f6edf16dc3c81cd998704b3d863c8ca16131007eb8e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138649625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379aa63781c7bd7556f5e2164a4024a5f1900f06b3405426708fdd50a6e5facb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:49:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:50:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:50:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:50:00 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:50:00 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e26d2e5b846c0018ca5716e7ab1885536ce6061bbf55078537c32237c02810a`  
		Last Modified: Tue, 17 Mar 2026 02:50:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a420464ef66e9189f40162f178906aeebf526b465b9552d433169ff47a1a63d7`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 16.2 MB (16209341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fac858a648e2b39225b0919dc0da840751c2c51206754742afa2635380b4c0`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 1.2 MB (1232649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009eddd1df2329310836e8f73dfb1f2bab7f3da034d0fd6faccd3754f038db7d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 45.4 MB (45413532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3200f84dc1855a59e3bb582b7cffea6809c2ff36a52bae827fb6035c7c4081d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1b08e39d081c4018d8af0b5848027a44da8bd2f81a14246d1cbdb65d6ad64`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 51.9 MB (51850302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee2595071a0f1b3aef0703dd6389d26171b6d582322d68ba6e5380baac8cbe`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:4a29c5dbb5b11ae8ee50fa13aa8d0a596f5692966631f5054e448ebdf65b9f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcfb00eae63e5bcd83f363e02efb3c276f7f7c0edcfebe741cc2d44ea73f5b`

```dockerfile
```

-	Layers:
	-	`sha256:2a5711f80750486859ad5eb585fe80d384969bd4fe9a7c43c4d3fc57f6ed5a0c`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4008e40688626eab0f2f667e152913fbc9710f44684c4ab2ea59016e64e7b9`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8f6331cc9c23d403eb91ba1d6d9ebef3622afa91fc2eac771ea000a0148c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b069908f79ca262c3880aef700648141b0be4ad322970cb7cbafcfdaa57eb76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:59:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:58 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:58 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726d3ccf94ff715cb4621afa3cf3aa87bf187f3f78bc7192b7877c2dc38dcf72`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73010b268b1d9251d56551ab7d6e259a68454fd0df0a70b680defde0d213b347`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 17.9 MB (17888400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fe3eb5309c7fb7b0d56a82be47d9e0cffcd728ce536571445f54b08c1be7`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.2 MB (1220130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e519473f08d8fd6893168d3b34414ff92ea39ea32819a72d89b722c736c494`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 45.6 MB (45617061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc899eaee09f8f99b88c217e10a58d78bd93969d5d7dadb3f9f00ed6f6dc2b`  
		Last Modified: Tue, 17 Mar 2026 03:00:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a6105692a3b0090a172e554a66ef36dcde16ef19300983e1ffa1985a60d015`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 51.9 MB (51850219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f08bb352cd249f42a5d437a9a92df6140d43bb7c010c00357c2e3e4c0ca0a`  
		Last Modified: Tue, 17 Mar 2026 03:00:14 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:d4fbade90fb359024aeea96233d0cfc5ba75dd0a36674738f031085f299aebbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbe063fc98fd1c2f4bd2212f06fcabe796fdd82d308988dfdd4be7e29eaefcf`

```dockerfile
```

-	Layers:
	-	`sha256:c4fc34a893084fb72196fce4ff2d94c83076754ab7abb0b2380a5caf1fd4cdec`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f041e1db81650ac166e8c53f7fc7cef443889a3f71afb41ce2c23827897186`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 35.9 KB (35909 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6a33d01c0223819c8d598de9a7e871afc3fd3ee2cad5e72388b462ea853f7faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147392166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c9547738ef6af564d6a7deeda756c9f243c4af155a193f621592e22ccd866`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 18:04:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:04:24 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:04:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:04:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c726bf2a78a1fc122da0840b9eba047db3fbb5e7e55726649c8f2b584e46b5`  
		Last Modified: Tue, 17 Mar 2026 18:04:50 GMT  
		Size: 51.9 MB (51850548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ae18580784cb7240e0b50e089c5c44801decce49fea47203c9731f77643963`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:b2bfe96db1360650e7d4fc110c88b779f6a451b4cecebe85274fbfde91a986d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f1e55e19a689263f393367b327b5eaaf0a42a3a4bb7cbeae0d1df7a59e085`

```dockerfile
```

-	Layers:
	-	`sha256:b338c4935b96aa7cee5982eefac402ce6f2be3780db1bca9c95429553e362651`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad003619e0820f1c011feee14f3162c5399870bd80cc7fc3c08ebb0302c12d9`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 35.8 KB (35780 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; s390x

```console
$ docker pull cassandra@sha256:51ba24a9bf69549e51813086b6c201c57d1f65a4ed11ed1613aa17fad0fa28c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138744006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9520d2ee6ca372587046d3c60a72aecd683ef7cd06c3081ac6e42b3cdc8108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 11:24:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:31 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04611d3add83f47830619dddc831f3a5d99d42ac6c4c79c3a6738bdd50f1ec78`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 51.9 MB (51851116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc341591840c1d84d6ad1b86aa148730228db0dd1e6c7cefa570fbb0df4440`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:9604ae75321349de3433b70d768aa77192d9da7cbc3526b6109c4e47f362f3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738ae175d1b9477594547b6cd001b3d27f83aaf97d33d4f92473e5527ed49970`

```dockerfile
```

-	Layers:
	-	`sha256:4adb1eb4916c4fdb9ee029b303f4d87a22a89f3e340e0f71009529dd2f1eceb3`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1aaddc9291f94f41049deb7cee887920e5a8470da29651c749d0698d7482f7f`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0-bookworm`

```console
$ docker pull cassandra@sha256:1fa3204f4be6ca223886d763c1dd7083bbf19fe678cb8dce25420ae09c7db354
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

### `cassandra:4.0-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:f42f1244e962ee3c2ccf20393950d161c57863b599634b4bc3c44e5d3018130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bc5a2f811ce824bb4ade64907d8ddc05a15f3350ce9f95ee288ff8b517da8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:18 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:55:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d836223b9c9f5cc73a05206fb58837ffb326baf90a60a3ddaf5852d4744bf9`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96abcf7decece82c84be1fdcfe2961a210de883e443b69f490682b077039cf1b`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 18.2 MB (18150047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9c0e50cc5660757aaa73da587aecdfc8cbbed4d5bf80bd633e29ede25d869`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.3 MB (1266589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106b4f5f45a273a5076ebb591bfe22e18c445e9c4870a4ab5696020f68addf58`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 47.3 MB (47295078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ce6a5606c87fdfb7692b2ead75fd33061fdd82d31c4a5d80c4c6d0b5064856`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20e88120a30c7c368f5ba7be4a4fa03521a5cbcda7924776bd460d5c5349ffe`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffa86e8f62a386ae9915d19e94a84f2f2dd979304f7b6ef10080a3d4a44d284`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a795374db9aeb9cb06a6037c5daef7e1779628d61b3c3c567a2c3abd3c1238b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451ba2f333c122664b8457cbc4dab1a59493dafe83eb3891cf11b4f291f8f083`

```dockerfile
```

-	Layers:
	-	`sha256:ca825978cdbc0feeb26d176810dce5f3d1f821a238eae06959be351921535b52`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8c2bde62a4784489d66372b381c052d77c8db1207feac5e2206f05c42f9b2`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:48664a8fd3f8b057e54f6edf16dc3c81cd998704b3d863c8ca16131007eb8e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138649625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379aa63781c7bd7556f5e2164a4024a5f1900f06b3405426708fdd50a6e5facb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:49:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:50:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:50:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:50:00 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:50:00 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e26d2e5b846c0018ca5716e7ab1885536ce6061bbf55078537c32237c02810a`  
		Last Modified: Tue, 17 Mar 2026 02:50:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a420464ef66e9189f40162f178906aeebf526b465b9552d433169ff47a1a63d7`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 16.2 MB (16209341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fac858a648e2b39225b0919dc0da840751c2c51206754742afa2635380b4c0`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 1.2 MB (1232649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009eddd1df2329310836e8f73dfb1f2bab7f3da034d0fd6faccd3754f038db7d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 45.4 MB (45413532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3200f84dc1855a59e3bb582b7cffea6809c2ff36a52bae827fb6035c7c4081d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1b08e39d081c4018d8af0b5848027a44da8bd2f81a14246d1cbdb65d6ad64`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 51.9 MB (51850302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee2595071a0f1b3aef0703dd6389d26171b6d582322d68ba6e5380baac8cbe`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:4a29c5dbb5b11ae8ee50fa13aa8d0a596f5692966631f5054e448ebdf65b9f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcfb00eae63e5bcd83f363e02efb3c276f7f7c0edcfebe741cc2d44ea73f5b`

```dockerfile
```

-	Layers:
	-	`sha256:2a5711f80750486859ad5eb585fe80d384969bd4fe9a7c43c4d3fc57f6ed5a0c`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4008e40688626eab0f2f667e152913fbc9710f44684c4ab2ea59016e64e7b9`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8f6331cc9c23d403eb91ba1d6d9ebef3622afa91fc2eac771ea000a0148c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b069908f79ca262c3880aef700648141b0be4ad322970cb7cbafcfdaa57eb76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:59:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:58 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:58 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726d3ccf94ff715cb4621afa3cf3aa87bf187f3f78bc7192b7877c2dc38dcf72`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73010b268b1d9251d56551ab7d6e259a68454fd0df0a70b680defde0d213b347`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 17.9 MB (17888400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fe3eb5309c7fb7b0d56a82be47d9e0cffcd728ce536571445f54b08c1be7`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.2 MB (1220130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e519473f08d8fd6893168d3b34414ff92ea39ea32819a72d89b722c736c494`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 45.6 MB (45617061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc899eaee09f8f99b88c217e10a58d78bd93969d5d7dadb3f9f00ed6f6dc2b`  
		Last Modified: Tue, 17 Mar 2026 03:00:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a6105692a3b0090a172e554a66ef36dcde16ef19300983e1ffa1985a60d015`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 51.9 MB (51850219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f08bb352cd249f42a5d437a9a92df6140d43bb7c010c00357c2e3e4c0ca0a`  
		Last Modified: Tue, 17 Mar 2026 03:00:14 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:d4fbade90fb359024aeea96233d0cfc5ba75dd0a36674738f031085f299aebbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbe063fc98fd1c2f4bd2212f06fcabe796fdd82d308988dfdd4be7e29eaefcf`

```dockerfile
```

-	Layers:
	-	`sha256:c4fc34a893084fb72196fce4ff2d94c83076754ab7abb0b2380a5caf1fd4cdec`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f041e1db81650ac166e8c53f7fc7cef443889a3f71afb41ce2c23827897186`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 35.9 KB (35909 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6a33d01c0223819c8d598de9a7e871afc3fd3ee2cad5e72388b462ea853f7faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147392166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c9547738ef6af564d6a7deeda756c9f243c4af155a193f621592e22ccd866`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 18:04:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:04:24 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:04:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:04:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c726bf2a78a1fc122da0840b9eba047db3fbb5e7e55726649c8f2b584e46b5`  
		Last Modified: Tue, 17 Mar 2026 18:04:50 GMT  
		Size: 51.9 MB (51850548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ae18580784cb7240e0b50e089c5c44801decce49fea47203c9731f77643963`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b2bfe96db1360650e7d4fc110c88b779f6a451b4cecebe85274fbfde91a986d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f1e55e19a689263f393367b327b5eaaf0a42a3a4bb7cbeae0d1df7a59e085`

```dockerfile
```

-	Layers:
	-	`sha256:b338c4935b96aa7cee5982eefac402ce6f2be3780db1bca9c95429553e362651`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad003619e0820f1c011feee14f3162c5399870bd80cc7fc3c08ebb0302c12d9`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 35.8 KB (35780 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:51ba24a9bf69549e51813086b6c201c57d1f65a4ed11ed1613aa17fad0fa28c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138744006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9520d2ee6ca372587046d3c60a72aecd683ef7cd06c3081ac6e42b3cdc8108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 11:24:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:31 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04611d3add83f47830619dddc831f3a5d99d42ac6c4c79c3a6738bdd50f1ec78`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 51.9 MB (51851116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc341591840c1d84d6ad1b86aa148730228db0dd1e6c7cefa570fbb0df4440`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:9604ae75321349de3433b70d768aa77192d9da7cbc3526b6109c4e47f362f3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738ae175d1b9477594547b6cd001b3d27f83aaf97d33d4f92473e5527ed49970`

```dockerfile
```

-	Layers:
	-	`sha256:4adb1eb4916c4fdb9ee029b303f4d87a22a89f3e340e0f71009529dd2f1eceb3`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1aaddc9291f94f41049deb7cee887920e5a8470da29651c749d0698d7482f7f`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0.19`

```console
$ docker pull cassandra@sha256:1fa3204f4be6ca223886d763c1dd7083bbf19fe678cb8dce25420ae09c7db354
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

### `cassandra:4.0.19` - linux; amd64

```console
$ docker pull cassandra@sha256:f42f1244e962ee3c2ccf20393950d161c57863b599634b4bc3c44e5d3018130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bc5a2f811ce824bb4ade64907d8ddc05a15f3350ce9f95ee288ff8b517da8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:18 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:55:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d836223b9c9f5cc73a05206fb58837ffb326baf90a60a3ddaf5852d4744bf9`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96abcf7decece82c84be1fdcfe2961a210de883e443b69f490682b077039cf1b`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 18.2 MB (18150047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9c0e50cc5660757aaa73da587aecdfc8cbbed4d5bf80bd633e29ede25d869`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.3 MB (1266589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106b4f5f45a273a5076ebb591bfe22e18c445e9c4870a4ab5696020f68addf58`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 47.3 MB (47295078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ce6a5606c87fdfb7692b2ead75fd33061fdd82d31c4a5d80c4c6d0b5064856`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20e88120a30c7c368f5ba7be4a4fa03521a5cbcda7924776bd460d5c5349ffe`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffa86e8f62a386ae9915d19e94a84f2f2dd979304f7b6ef10080a3d4a44d284`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:a795374db9aeb9cb06a6037c5daef7e1779628d61b3c3c567a2c3abd3c1238b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451ba2f333c122664b8457cbc4dab1a59493dafe83eb3891cf11b4f291f8f083`

```dockerfile
```

-	Layers:
	-	`sha256:ca825978cdbc0feeb26d176810dce5f3d1f821a238eae06959be351921535b52`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8c2bde62a4784489d66372b381c052d77c8db1207feac5e2206f05c42f9b2`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:48664a8fd3f8b057e54f6edf16dc3c81cd998704b3d863c8ca16131007eb8e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138649625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379aa63781c7bd7556f5e2164a4024a5f1900f06b3405426708fdd50a6e5facb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:49:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:50:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:50:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:50:00 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:50:00 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e26d2e5b846c0018ca5716e7ab1885536ce6061bbf55078537c32237c02810a`  
		Last Modified: Tue, 17 Mar 2026 02:50:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a420464ef66e9189f40162f178906aeebf526b465b9552d433169ff47a1a63d7`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 16.2 MB (16209341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fac858a648e2b39225b0919dc0da840751c2c51206754742afa2635380b4c0`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 1.2 MB (1232649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009eddd1df2329310836e8f73dfb1f2bab7f3da034d0fd6faccd3754f038db7d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 45.4 MB (45413532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3200f84dc1855a59e3bb582b7cffea6809c2ff36a52bae827fb6035c7c4081d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1b08e39d081c4018d8af0b5848027a44da8bd2f81a14246d1cbdb65d6ad64`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 51.9 MB (51850302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee2595071a0f1b3aef0703dd6389d26171b6d582322d68ba6e5380baac8cbe`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:4a29c5dbb5b11ae8ee50fa13aa8d0a596f5692966631f5054e448ebdf65b9f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcfb00eae63e5bcd83f363e02efb3c276f7f7c0edcfebe741cc2d44ea73f5b`

```dockerfile
```

-	Layers:
	-	`sha256:2a5711f80750486859ad5eb585fe80d384969bd4fe9a7c43c4d3fc57f6ed5a0c`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4008e40688626eab0f2f667e152913fbc9710f44684c4ab2ea59016e64e7b9`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8f6331cc9c23d403eb91ba1d6d9ebef3622afa91fc2eac771ea000a0148c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b069908f79ca262c3880aef700648141b0be4ad322970cb7cbafcfdaa57eb76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:59:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:58 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:58 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726d3ccf94ff715cb4621afa3cf3aa87bf187f3f78bc7192b7877c2dc38dcf72`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73010b268b1d9251d56551ab7d6e259a68454fd0df0a70b680defde0d213b347`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 17.9 MB (17888400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fe3eb5309c7fb7b0d56a82be47d9e0cffcd728ce536571445f54b08c1be7`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.2 MB (1220130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e519473f08d8fd6893168d3b34414ff92ea39ea32819a72d89b722c736c494`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 45.6 MB (45617061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc899eaee09f8f99b88c217e10a58d78bd93969d5d7dadb3f9f00ed6f6dc2b`  
		Last Modified: Tue, 17 Mar 2026 03:00:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a6105692a3b0090a172e554a66ef36dcde16ef19300983e1ffa1985a60d015`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 51.9 MB (51850219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f08bb352cd249f42a5d437a9a92df6140d43bb7c010c00357c2e3e4c0ca0a`  
		Last Modified: Tue, 17 Mar 2026 03:00:14 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:d4fbade90fb359024aeea96233d0cfc5ba75dd0a36674738f031085f299aebbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbe063fc98fd1c2f4bd2212f06fcabe796fdd82d308988dfdd4be7e29eaefcf`

```dockerfile
```

-	Layers:
	-	`sha256:c4fc34a893084fb72196fce4ff2d94c83076754ab7abb0b2380a5caf1fd4cdec`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f041e1db81650ac166e8c53f7fc7cef443889a3f71afb41ce2c23827897186`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 35.9 KB (35909 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6a33d01c0223819c8d598de9a7e871afc3fd3ee2cad5e72388b462ea853f7faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147392166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c9547738ef6af564d6a7deeda756c9f243c4af155a193f621592e22ccd866`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 18:04:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:04:24 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:04:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:04:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c726bf2a78a1fc122da0840b9eba047db3fbb5e7e55726649c8f2b584e46b5`  
		Last Modified: Tue, 17 Mar 2026 18:04:50 GMT  
		Size: 51.9 MB (51850548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ae18580784cb7240e0b50e089c5c44801decce49fea47203c9731f77643963`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:b2bfe96db1360650e7d4fc110c88b779f6a451b4cecebe85274fbfde91a986d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f1e55e19a689263f393367b327b5eaaf0a42a3a4bb7cbeae0d1df7a59e085`

```dockerfile
```

-	Layers:
	-	`sha256:b338c4935b96aa7cee5982eefac402ce6f2be3780db1bca9c95429553e362651`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad003619e0820f1c011feee14f3162c5399870bd80cc7fc3c08ebb0302c12d9`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 35.8 KB (35780 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; s390x

```console
$ docker pull cassandra@sha256:51ba24a9bf69549e51813086b6c201c57d1f65a4ed11ed1613aa17fad0fa28c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138744006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9520d2ee6ca372587046d3c60a72aecd683ef7cd06c3081ac6e42b3cdc8108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 11:24:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:31 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04611d3add83f47830619dddc831f3a5d99d42ac6c4c79c3a6738bdd50f1ec78`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 51.9 MB (51851116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc341591840c1d84d6ad1b86aa148730228db0dd1e6c7cefa570fbb0df4440`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:9604ae75321349de3433b70d768aa77192d9da7cbc3526b6109c4e47f362f3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738ae175d1b9477594547b6cd001b3d27f83aaf97d33d4f92473e5527ed49970`

```dockerfile
```

-	Layers:
	-	`sha256:4adb1eb4916c4fdb9ee029b303f4d87a22a89f3e340e0f71009529dd2f1eceb3`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1aaddc9291f94f41049deb7cee887920e5a8470da29651c749d0698d7482f7f`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0.19-bookworm`

```console
$ docker pull cassandra@sha256:1fa3204f4be6ca223886d763c1dd7083bbf19fe678cb8dce25420ae09c7db354
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

### `cassandra:4.0.19-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:f42f1244e962ee3c2ccf20393950d161c57863b599634b4bc3c44e5d3018130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bc5a2f811ce824bb4ade64907d8ddc05a15f3350ce9f95ee288ff8b517da8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:18 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:32 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:55:32 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:55:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d836223b9c9f5cc73a05206fb58837ffb326baf90a60a3ddaf5852d4744bf9`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96abcf7decece82c84be1fdcfe2961a210de883e443b69f490682b077039cf1b`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 18.2 MB (18150047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9c0e50cc5660757aaa73da587aecdfc8cbbed4d5bf80bd633e29ede25d869`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 1.3 MB (1266589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106b4f5f45a273a5076ebb591bfe22e18c445e9c4870a4ab5696020f68addf58`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 47.3 MB (47295078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ce6a5606c87fdfb7692b2ead75fd33061fdd82d31c4a5d80c4c6d0b5064856`  
		Last Modified: Tue, 17 Mar 2026 02:56:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20e88120a30c7c368f5ba7be4a4fa03521a5cbcda7924776bd460d5c5349ffe`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffa86e8f62a386ae9915d19e94a84f2f2dd979304f7b6ef10080a3d4a44d284`  
		Last Modified: Tue, 17 Mar 2026 02:56:01 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a795374db9aeb9cb06a6037c5daef7e1779628d61b3c3c567a2c3abd3c1238b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451ba2f333c122664b8457cbc4dab1a59493dafe83eb3891cf11b4f291f8f083`

```dockerfile
```

-	Layers:
	-	`sha256:ca825978cdbc0feeb26d176810dce5f3d1f821a238eae06959be351921535b52`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8c2bde62a4784489d66372b381c052d77c8db1207feac5e2206f05c42f9b2`  
		Last Modified: Tue, 17 Mar 2026 02:55:59 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:48664a8fd3f8b057e54f6edf16dc3c81cd998704b3d863c8ca16131007eb8e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138649625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379aa63781c7bd7556f5e2164a4024a5f1900f06b3405426708fdd50a6e5facb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:49:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:49:39 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:50:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:50:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:50:00 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:50:00 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e26d2e5b846c0018ca5716e7ab1885536ce6061bbf55078537c32237c02810a`  
		Last Modified: Tue, 17 Mar 2026 02:50:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a420464ef66e9189f40162f178906aeebf526b465b9552d433169ff47a1a63d7`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 16.2 MB (16209341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fac858a648e2b39225b0919dc0da840751c2c51206754742afa2635380b4c0`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 1.2 MB (1232649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009eddd1df2329310836e8f73dfb1f2bab7f3da034d0fd6faccd3754f038db7d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 45.4 MB (45413532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3200f84dc1855a59e3bb582b7cffea6809c2ff36a52bae827fb6035c7c4081d`  
		Last Modified: Tue, 17 Mar 2026 02:50:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1b08e39d081c4018d8af0b5848027a44da8bd2f81a14246d1cbdb65d6ad64`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 51.9 MB (51850302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee2595071a0f1b3aef0703dd6389d26171b6d582322d68ba6e5380baac8cbe`  
		Last Modified: Tue, 17 Mar 2026 02:50:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:4a29c5dbb5b11ae8ee50fa13aa8d0a596f5692966631f5054e448ebdf65b9f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcfb00eae63e5bcd83f363e02efb3c276f7f7c0edcfebe741cc2d44ea73f5b`

```dockerfile
```

-	Layers:
	-	`sha256:2a5711f80750486859ad5eb585fe80d384969bd4fe9a7c43c4d3fc57f6ed5a0c`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4008e40688626eab0f2f667e152913fbc9710f44684c4ab2ea59016e64e7b9`  
		Last Modified: Tue, 17 Mar 2026 02:50:12 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8f6331cc9c23d403eb91ba1d6d9ebef3622afa91fc2eac771ea000a0148c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b069908f79ca262c3880aef700648141b0be4ad322970cb7cbafcfdaa57eb76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:42 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 02:59:42 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 02:59:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:58 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:58 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726d3ccf94ff715cb4621afa3cf3aa87bf187f3f78bc7192b7877c2dc38dcf72`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73010b268b1d9251d56551ab7d6e259a68454fd0df0a70b680defde0d213b347`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 17.9 MB (17888400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fe3eb5309c7fb7b0d56a82be47d9e0cffcd728ce536571445f54b08c1be7`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 1.2 MB (1220130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e519473f08d8fd6893168d3b34414ff92ea39ea32819a72d89b722c736c494`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 45.6 MB (45617061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc899eaee09f8f99b88c217e10a58d78bd93969d5d7dadb3f9f00ed6f6dc2b`  
		Last Modified: Tue, 17 Mar 2026 03:00:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a6105692a3b0090a172e554a66ef36dcde16ef19300983e1ffa1985a60d015`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 51.9 MB (51850219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f08bb352cd249f42a5d437a9a92df6140d43bb7c010c00357c2e3e4c0ca0a`  
		Last Modified: Tue, 17 Mar 2026 03:00:14 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:d4fbade90fb359024aeea96233d0cfc5ba75dd0a36674738f031085f299aebbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbe063fc98fd1c2f4bd2212f06fcabe796fdd82d308988dfdd4be7e29eaefcf`

```dockerfile
```

-	Layers:
	-	`sha256:c4fc34a893084fb72196fce4ff2d94c83076754ab7abb0b2380a5caf1fd4cdec`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f041e1db81650ac166e8c53f7fc7cef443889a3f71afb41ce2c23827897186`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 35.9 KB (35909 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6a33d01c0223819c8d598de9a7e871afc3fd3ee2cad5e72388b462ea853f7faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147392166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c9547738ef6af564d6a7deeda756c9f243c4af155a193f621592e22ccd866`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 18:04:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:04:24 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:04:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:04:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c726bf2a78a1fc122da0840b9eba047db3fbb5e7e55726649c8f2b584e46b5`  
		Last Modified: Tue, 17 Mar 2026 18:04:50 GMT  
		Size: 51.9 MB (51850548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ae18580784cb7240e0b50e089c5c44801decce49fea47203c9731f77643963`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b2bfe96db1360650e7d4fc110c88b779f6a451b4cecebe85274fbfde91a986d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f1e55e19a689263f393367b327b5eaaf0a42a3a4bb7cbeae0d1df7a59e085`

```dockerfile
```

-	Layers:
	-	`sha256:b338c4935b96aa7cee5982eefac402ce6f2be3780db1bca9c95429553e362651`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad003619e0820f1c011feee14f3162c5399870bd80cc7fc3c08ebb0302c12d9`  
		Last Modified: Tue, 17 Mar 2026 18:04:48 GMT  
		Size: 35.8 KB (35780 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:51ba24a9bf69549e51813086b6c201c57d1f65a4ed11ed1613aa17fad0fa28c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138744006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9520d2ee6ca372587046d3c60a72aecd683ef7cd06c3081ac6e42b3cdc8108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Mar 2026 11:24:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:31 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04611d3add83f47830619dddc831f3a5d99d42ac6c4c79c3a6738bdd50f1ec78`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 51.9 MB (51851116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc341591840c1d84d6ad1b86aa148730228db0dd1e6c7cefa570fbb0df4440`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:9604ae75321349de3433b70d768aa77192d9da7cbc3526b6109c4e47f362f3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738ae175d1b9477594547b6cd001b3d27f83aaf97d33d4f92473e5527ed49970`

```dockerfile
```

-	Layers:
	-	`sha256:4adb1eb4916c4fdb9ee029b303f4d87a22a89f3e340e0f71009529dd2f1eceb3`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1aaddc9291f94f41049deb7cee887920e5a8470da29651c749d0698d7482f7f`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1`

```console
$ docker pull cassandra@sha256:5e620e10efaeaf936ae73963e594c98df88f0cd468582d7ceb324cbb864f0604
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

### `cassandra:4.1` - linux; amd64

```console
$ docker pull cassandra@sha256:54589570846dcb96b39186721893246c7e97584ea6fe4e0ae02cac261d0833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84025b614066c7356b7225de9d9b8e2fe5941629d0a99aac0c6c55a023aebe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc147edb2180a007f53a18e50d643052e6b7d656281b7c5ab3cf0d70f28a0940`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d670879c4857cef3fb10b38721fa158f588e4ddd85896eff28c242a0989df`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.1 MB (18149851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b923e722f511a50b6bff10ba3b92293274cd6413d772dda4a689c6bbe0c7a6`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04daf4a2aade34353992d9096263af2ef8fd11aeafdd5b73dedbb26ef8f9b9`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.3 MB (47295070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44524ed1b03fe00c98b2fbf50dbe6727807cfc0f18210d64c9f701cbf245bff`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a8489d07ae41ed9e2d6345a0c13e6034112415f26c487f3992a0f16cb1499`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 52.9 MB (52914394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0abca5db3e631dd5135204bd9a6bc8d73612f4f80a6bdae493f43c439ac92`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:2d23bb7bcefda8d9274d396b12fbd83ddc56057015c6dca70b14a85cebf69e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc84b3792ade99a4755b76df1dccf5cd5f54173164c57dfc7e76a9e6610941b`

```dockerfile
```

-	Layers:
	-	`sha256:110edf9777d29d3f663616de421dec295c4cb30974ab58fb4125ebeade444a80`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5f100b6de7a3a1047993df533e2fbab334a1aa46a279d53870a1c01feb0f48`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:024f89d5c5131ffd64f2cd879a463046786d584139b4ecf67e95a40a291e379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139713787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a392bb249cde12480a26c56f793ebe209efbf7b2794c6d420f96535c5bdc2ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d1c799df811c08290bdbbcf494a179577f307a9102358ba6233490f8dc869`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678ee1b5b5ab49ae78fde02726ed843258da79044760e0644c8004906d475e05`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 16.2 MB (16209314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862025c91bde921b5cbc7345a2ace01654d8563870616a5ad60305da39e0a1`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.2 MB (1232648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4f13334e150c465bb2a85a4cf7c1b6f8cb3eb112bb98b7cdee3ed7b9928be`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 45.4 MB (45413511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3bf184cc7184732ad3551c915100fdac47df4e8d0bbc403340bbb61ef83f8e`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662617661e0afde65f790710b7bc09ebc4a41f8a331b01f474a53e531930d88`  
		Last Modified: Tue, 17 Mar 2026 02:49:44 GMT  
		Size: 52.9 MB (52914512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e3d16726bac9043b08884dd54073770b70e21c1adac99f556d2ec78c0c9b3f`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:630dc769d37bf584cf595776073b772707a78cd76e5418c2155c7e9c030e683b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f66e9f1c73ded8a88e09ee918c043bd04e5bcb19bf6ef00d32440ad2daad72`

```dockerfile
```

-	Layers:
	-	`sha256:de8104fcc429251fb1fda9ed26bd0aca4b09c7552f033abdbde199c35c3c757e`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6fc66ca6b8d54f7bfaf8dfc95c10b0dbdad4913cb0c4d850254ab3cc365de7`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:ada7dcfbd6cd0e8fe614285f90be65f2b609850c6447fb9d34d49af0071721d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081c9417c8f5c18e12b951d84e4faac1d96f3a233d3970ffb7607ad802fda4be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:49 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df339bed319fdd8de6f4208b5f9d4c55dff7d6048859b27073939d45ca9993a3`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be127bac61685f5e5c9c08d6d8dc2fdded5d51f05879f079878c790fa4ed21`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 17.9 MB (17888514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a10a35f57460bf17e201ca809b66febd1b0ad9c4eb2ce18eb86fb217f007963`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 1.2 MB (1220054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c00ad6d00bfaab00e033f6ea96dd01a532ac6fb496f20c6f03e708afbe080`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 45.6 MB (45617060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4000f376411bd7a134155344d5d0973f6572fea39089439e1346a89a154c50f7`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab142b63d3d02bdbe0c588f513d60a7165cb69fd41decfa7f7dc95be45f70713`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 52.9 MB (52914363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812da46cd96e726eb6b3268a352d8a66118b3b26f09483823d3379e7a428a939`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:79c9891cd92bccc8bcc390e203f0a3937eeb6677c87476510af40d3f53cf642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05f52e0f266413f489f6fcaa908ee03b8ce88100258d45d82f89ef18ab672f`

```dockerfile
```

-	Layers:
	-	`sha256:acb60ded2b756e0e9e3724926123424cbf0c8a18dec94d2e281af07ede67f08a`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd93984ef667b433881565357fb7b4f33d68039364e7e6cfe7f3ede4fd5a8d`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6eb375e1e70b4d0c1043560740cf35e1c092a57c789a1b5ab3b73e4712573369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148456276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78eb4cceb4186629456b4d85662ceb85552043b42815b0040686a900cdfae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 18:03:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:04 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:04 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e9ab86808875414f35ec4d4f6e5fb738e11e915034dccd7bd2d0fc20b6641`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 52.9 MB (52914659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a95eebf8bcf16c01a7abb0f6de19b873d1cb1b6c6ba8cfa0ef40832a2ecfc`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:a654bf8943c1706a9014e08dacbba0394522abda99a17523b8190c63c6d3f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9333b30d3b9b096019f8c876371b3e66308a7f84db7a9ac0f0a8be473315a`

```dockerfile
```

-	Layers:
	-	`sha256:6316c32cb26befe75f4a43768136066f477a297cfddeb850898cbddcfb7636f6`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f89cc1f6410a780d2a4da15aab47082e308d9d59afe5ab5c6299fb90275e9d`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 36.4 KB (36397 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; s390x

```console
$ docker pull cassandra@sha256:fc8eeff22bd21e4deae972ca136b304d95bdcb68733a82b5c043000454dced00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563513928131e9a28cfa9c225b98313c49336f68b0957cc23e9c353603bb4a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 11:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:30 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26393507fa42481ea67f620f43fb8c66f3130fc06d9bdbf849439834a274b08`  
		Last Modified: Tue, 17 Mar 2026 11:25:28 GMT  
		Size: 52.9 MB (52915323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c03bd184e759fde5abc9fdcb16f46c8fbad84289541eb9beffcfbb98ccabdbd`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:fda4630ac60a4304b85bf07516b53fe7adceacc53946912744b05eb5c51ec207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e4f376d1e28a2f1b92ab6288da8668d4954bf485dd1b570979c3e4df45588c`

```dockerfile
```

-	Layers:
	-	`sha256:ebc54e94368edbce6a1ae499c26da64270991b6db7da6e7dfc96523713ae303e`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cfa8490820696b7f33a860d5db0c9c958202ec9211f478a486dba079714d9`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1-bookworm`

```console
$ docker pull cassandra@sha256:5e620e10efaeaf936ae73963e594c98df88f0cd468582d7ceb324cbb864f0604
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

### `cassandra:4.1-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:54589570846dcb96b39186721893246c7e97584ea6fe4e0ae02cac261d0833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84025b614066c7356b7225de9d9b8e2fe5941629d0a99aac0c6c55a023aebe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc147edb2180a007f53a18e50d643052e6b7d656281b7c5ab3cf0d70f28a0940`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d670879c4857cef3fb10b38721fa158f588e4ddd85896eff28c242a0989df`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.1 MB (18149851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b923e722f511a50b6bff10ba3b92293274cd6413d772dda4a689c6bbe0c7a6`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04daf4a2aade34353992d9096263af2ef8fd11aeafdd5b73dedbb26ef8f9b9`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.3 MB (47295070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44524ed1b03fe00c98b2fbf50dbe6727807cfc0f18210d64c9f701cbf245bff`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a8489d07ae41ed9e2d6345a0c13e6034112415f26c487f3992a0f16cb1499`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 52.9 MB (52914394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0abca5db3e631dd5135204bd9a6bc8d73612f4f80a6bdae493f43c439ac92`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:2d23bb7bcefda8d9274d396b12fbd83ddc56057015c6dca70b14a85cebf69e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc84b3792ade99a4755b76df1dccf5cd5f54173164c57dfc7e76a9e6610941b`

```dockerfile
```

-	Layers:
	-	`sha256:110edf9777d29d3f663616de421dec295c4cb30974ab58fb4125ebeade444a80`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5f100b6de7a3a1047993df533e2fbab334a1aa46a279d53870a1c01feb0f48`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:024f89d5c5131ffd64f2cd879a463046786d584139b4ecf67e95a40a291e379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139713787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a392bb249cde12480a26c56f793ebe209efbf7b2794c6d420f96535c5bdc2ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d1c799df811c08290bdbbcf494a179577f307a9102358ba6233490f8dc869`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678ee1b5b5ab49ae78fde02726ed843258da79044760e0644c8004906d475e05`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 16.2 MB (16209314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862025c91bde921b5cbc7345a2ace01654d8563870616a5ad60305da39e0a1`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.2 MB (1232648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4f13334e150c465bb2a85a4cf7c1b6f8cb3eb112bb98b7cdee3ed7b9928be`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 45.4 MB (45413511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3bf184cc7184732ad3551c915100fdac47df4e8d0bbc403340bbb61ef83f8e`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662617661e0afde65f790710b7bc09ebc4a41f8a331b01f474a53e531930d88`  
		Last Modified: Tue, 17 Mar 2026 02:49:44 GMT  
		Size: 52.9 MB (52914512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e3d16726bac9043b08884dd54073770b70e21c1adac99f556d2ec78c0c9b3f`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:630dc769d37bf584cf595776073b772707a78cd76e5418c2155c7e9c030e683b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f66e9f1c73ded8a88e09ee918c043bd04e5bcb19bf6ef00d32440ad2daad72`

```dockerfile
```

-	Layers:
	-	`sha256:de8104fcc429251fb1fda9ed26bd0aca4b09c7552f033abdbde199c35c3c757e`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6fc66ca6b8d54f7bfaf8dfc95c10b0dbdad4913cb0c4d850254ab3cc365de7`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:ada7dcfbd6cd0e8fe614285f90be65f2b609850c6447fb9d34d49af0071721d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081c9417c8f5c18e12b951d84e4faac1d96f3a233d3970ffb7607ad802fda4be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:49 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df339bed319fdd8de6f4208b5f9d4c55dff7d6048859b27073939d45ca9993a3`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be127bac61685f5e5c9c08d6d8dc2fdded5d51f05879f079878c790fa4ed21`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 17.9 MB (17888514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a10a35f57460bf17e201ca809b66febd1b0ad9c4eb2ce18eb86fb217f007963`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 1.2 MB (1220054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c00ad6d00bfaab00e033f6ea96dd01a532ac6fb496f20c6f03e708afbe080`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 45.6 MB (45617060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4000f376411bd7a134155344d5d0973f6572fea39089439e1346a89a154c50f7`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab142b63d3d02bdbe0c588f513d60a7165cb69fd41decfa7f7dc95be45f70713`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 52.9 MB (52914363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812da46cd96e726eb6b3268a352d8a66118b3b26f09483823d3379e7a428a939`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:79c9891cd92bccc8bcc390e203f0a3937eeb6677c87476510af40d3f53cf642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05f52e0f266413f489f6fcaa908ee03b8ce88100258d45d82f89ef18ab672f`

```dockerfile
```

-	Layers:
	-	`sha256:acb60ded2b756e0e9e3724926123424cbf0c8a18dec94d2e281af07ede67f08a`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd93984ef667b433881565357fb7b4f33d68039364e7e6cfe7f3ede4fd5a8d`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6eb375e1e70b4d0c1043560740cf35e1c092a57c789a1b5ab3b73e4712573369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148456276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78eb4cceb4186629456b4d85662ceb85552043b42815b0040686a900cdfae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 18:03:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:04 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:04 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e9ab86808875414f35ec4d4f6e5fb738e11e915034dccd7bd2d0fc20b6641`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 52.9 MB (52914659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a95eebf8bcf16c01a7abb0f6de19b873d1cb1b6c6ba8cfa0ef40832a2ecfc`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a654bf8943c1706a9014e08dacbba0394522abda99a17523b8190c63c6d3f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9333b30d3b9b096019f8c876371b3e66308a7f84db7a9ac0f0a8be473315a`

```dockerfile
```

-	Layers:
	-	`sha256:6316c32cb26befe75f4a43768136066f477a297cfddeb850898cbddcfb7636f6`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f89cc1f6410a780d2a4da15aab47082e308d9d59afe5ab5c6299fb90275e9d`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 36.4 KB (36397 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:fc8eeff22bd21e4deae972ca136b304d95bdcb68733a82b5c043000454dced00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563513928131e9a28cfa9c225b98313c49336f68b0957cc23e9c353603bb4a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 11:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:30 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26393507fa42481ea67f620f43fb8c66f3130fc06d9bdbf849439834a274b08`  
		Last Modified: Tue, 17 Mar 2026 11:25:28 GMT  
		Size: 52.9 MB (52915323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c03bd184e759fde5abc9fdcb16f46c8fbad84289541eb9beffcfbb98ccabdbd`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:fda4630ac60a4304b85bf07516b53fe7adceacc53946912744b05eb5c51ec207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e4f376d1e28a2f1b92ab6288da8668d4954bf485dd1b570979c3e4df45588c`

```dockerfile
```

-	Layers:
	-	`sha256:ebc54e94368edbce6a1ae499c26da64270991b6db7da6e7dfc96523713ae303e`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cfa8490820696b7f33a860d5db0c9c958202ec9211f478a486dba079714d9`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1.10`

```console
$ docker pull cassandra@sha256:5e620e10efaeaf936ae73963e594c98df88f0cd468582d7ceb324cbb864f0604
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

### `cassandra:4.1.10` - linux; amd64

```console
$ docker pull cassandra@sha256:54589570846dcb96b39186721893246c7e97584ea6fe4e0ae02cac261d0833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84025b614066c7356b7225de9d9b8e2fe5941629d0a99aac0c6c55a023aebe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc147edb2180a007f53a18e50d643052e6b7d656281b7c5ab3cf0d70f28a0940`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d670879c4857cef3fb10b38721fa158f588e4ddd85896eff28c242a0989df`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.1 MB (18149851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b923e722f511a50b6bff10ba3b92293274cd6413d772dda4a689c6bbe0c7a6`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04daf4a2aade34353992d9096263af2ef8fd11aeafdd5b73dedbb26ef8f9b9`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.3 MB (47295070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44524ed1b03fe00c98b2fbf50dbe6727807cfc0f18210d64c9f701cbf245bff`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a8489d07ae41ed9e2d6345a0c13e6034112415f26c487f3992a0f16cb1499`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 52.9 MB (52914394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0abca5db3e631dd5135204bd9a6bc8d73612f4f80a6bdae493f43c439ac92`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:2d23bb7bcefda8d9274d396b12fbd83ddc56057015c6dca70b14a85cebf69e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc84b3792ade99a4755b76df1dccf5cd5f54173164c57dfc7e76a9e6610941b`

```dockerfile
```

-	Layers:
	-	`sha256:110edf9777d29d3f663616de421dec295c4cb30974ab58fb4125ebeade444a80`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5f100b6de7a3a1047993df533e2fbab334a1aa46a279d53870a1c01feb0f48`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:024f89d5c5131ffd64f2cd879a463046786d584139b4ecf67e95a40a291e379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139713787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a392bb249cde12480a26c56f793ebe209efbf7b2794c6d420f96535c5bdc2ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d1c799df811c08290bdbbcf494a179577f307a9102358ba6233490f8dc869`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678ee1b5b5ab49ae78fde02726ed843258da79044760e0644c8004906d475e05`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 16.2 MB (16209314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862025c91bde921b5cbc7345a2ace01654d8563870616a5ad60305da39e0a1`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.2 MB (1232648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4f13334e150c465bb2a85a4cf7c1b6f8cb3eb112bb98b7cdee3ed7b9928be`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 45.4 MB (45413511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3bf184cc7184732ad3551c915100fdac47df4e8d0bbc403340bbb61ef83f8e`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662617661e0afde65f790710b7bc09ebc4a41f8a331b01f474a53e531930d88`  
		Last Modified: Tue, 17 Mar 2026 02:49:44 GMT  
		Size: 52.9 MB (52914512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e3d16726bac9043b08884dd54073770b70e21c1adac99f556d2ec78c0c9b3f`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:630dc769d37bf584cf595776073b772707a78cd76e5418c2155c7e9c030e683b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f66e9f1c73ded8a88e09ee918c043bd04e5bcb19bf6ef00d32440ad2daad72`

```dockerfile
```

-	Layers:
	-	`sha256:de8104fcc429251fb1fda9ed26bd0aca4b09c7552f033abdbde199c35c3c757e`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6fc66ca6b8d54f7bfaf8dfc95c10b0dbdad4913cb0c4d850254ab3cc365de7`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:ada7dcfbd6cd0e8fe614285f90be65f2b609850c6447fb9d34d49af0071721d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081c9417c8f5c18e12b951d84e4faac1d96f3a233d3970ffb7607ad802fda4be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:49 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df339bed319fdd8de6f4208b5f9d4c55dff7d6048859b27073939d45ca9993a3`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be127bac61685f5e5c9c08d6d8dc2fdded5d51f05879f079878c790fa4ed21`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 17.9 MB (17888514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a10a35f57460bf17e201ca809b66febd1b0ad9c4eb2ce18eb86fb217f007963`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 1.2 MB (1220054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c00ad6d00bfaab00e033f6ea96dd01a532ac6fb496f20c6f03e708afbe080`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 45.6 MB (45617060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4000f376411bd7a134155344d5d0973f6572fea39089439e1346a89a154c50f7`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab142b63d3d02bdbe0c588f513d60a7165cb69fd41decfa7f7dc95be45f70713`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 52.9 MB (52914363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812da46cd96e726eb6b3268a352d8a66118b3b26f09483823d3379e7a428a939`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:79c9891cd92bccc8bcc390e203f0a3937eeb6677c87476510af40d3f53cf642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05f52e0f266413f489f6fcaa908ee03b8ce88100258d45d82f89ef18ab672f`

```dockerfile
```

-	Layers:
	-	`sha256:acb60ded2b756e0e9e3724926123424cbf0c8a18dec94d2e281af07ede67f08a`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd93984ef667b433881565357fb7b4f33d68039364e7e6cfe7f3ede4fd5a8d`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6eb375e1e70b4d0c1043560740cf35e1c092a57c789a1b5ab3b73e4712573369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148456276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78eb4cceb4186629456b4d85662ceb85552043b42815b0040686a900cdfae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 18:03:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:04 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:04 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e9ab86808875414f35ec4d4f6e5fb738e11e915034dccd7bd2d0fc20b6641`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 52.9 MB (52914659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a95eebf8bcf16c01a7abb0f6de19b873d1cb1b6c6ba8cfa0ef40832a2ecfc`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:a654bf8943c1706a9014e08dacbba0394522abda99a17523b8190c63c6d3f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9333b30d3b9b096019f8c876371b3e66308a7f84db7a9ac0f0a8be473315a`

```dockerfile
```

-	Layers:
	-	`sha256:6316c32cb26befe75f4a43768136066f477a297cfddeb850898cbddcfb7636f6`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f89cc1f6410a780d2a4da15aab47082e308d9d59afe5ab5c6299fb90275e9d`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 36.4 KB (36397 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; s390x

```console
$ docker pull cassandra@sha256:fc8eeff22bd21e4deae972ca136b304d95bdcb68733a82b5c043000454dced00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563513928131e9a28cfa9c225b98313c49336f68b0957cc23e9c353603bb4a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 11:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:30 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26393507fa42481ea67f620f43fb8c66f3130fc06d9bdbf849439834a274b08`  
		Last Modified: Tue, 17 Mar 2026 11:25:28 GMT  
		Size: 52.9 MB (52915323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c03bd184e759fde5abc9fdcb16f46c8fbad84289541eb9beffcfbb98ccabdbd`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:fda4630ac60a4304b85bf07516b53fe7adceacc53946912744b05eb5c51ec207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e4f376d1e28a2f1b92ab6288da8668d4954bf485dd1b570979c3e4df45588c`

```dockerfile
```

-	Layers:
	-	`sha256:ebc54e94368edbce6a1ae499c26da64270991b6db7da6e7dfc96523713ae303e`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cfa8490820696b7f33a860d5db0c9c958202ec9211f478a486dba079714d9`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1.10-bookworm`

```console
$ docker pull cassandra@sha256:5e620e10efaeaf936ae73963e594c98df88f0cd468582d7ceb324cbb864f0604
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

### `cassandra:4.1.10-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:54589570846dcb96b39186721893246c7e97584ea6fe4e0ae02cac261d0833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84025b614066c7356b7225de9d9b8e2fe5941629d0a99aac0c6c55a023aebe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:55:23 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc147edb2180a007f53a18e50d643052e6b7d656281b7c5ab3cf0d70f28a0940`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d670879c4857cef3fb10b38721fa158f588e4ddd85896eff28c242a0989df`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.1 MB (18149851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b923e722f511a50b6bff10ba3b92293274cd6413d772dda4a689c6bbe0c7a6`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04daf4a2aade34353992d9096263af2ef8fd11aeafdd5b73dedbb26ef8f9b9`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.3 MB (47295070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44524ed1b03fe00c98b2fbf50dbe6727807cfc0f18210d64c9f701cbf245bff`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a8489d07ae41ed9e2d6345a0c13e6034112415f26c487f3992a0f16cb1499`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 52.9 MB (52914394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0abca5db3e631dd5135204bd9a6bc8d73612f4f80a6bdae493f43c439ac92`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:2d23bb7bcefda8d9274d396b12fbd83ddc56057015c6dca70b14a85cebf69e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc84b3792ade99a4755b76df1dccf5cd5f54173164c57dfc7e76a9e6610941b`

```dockerfile
```

-	Layers:
	-	`sha256:110edf9777d29d3f663616de421dec295c4cb30974ab58fb4125ebeade444a80`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5f100b6de7a3a1047993df533e2fbab334a1aa46a279d53870a1c01feb0f48`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:024f89d5c5131ffd64f2cd879a463046786d584139b4ecf67e95a40a291e379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139713787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a392bb249cde12480a26c56f793ebe209efbf7b2794c6d420f96535c5bdc2ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:49:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:49:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:49:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:49:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:49:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:49:09 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:49:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d1c799df811c08290bdbbcf494a179577f307a9102358ba6233490f8dc869`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678ee1b5b5ab49ae78fde02726ed843258da79044760e0644c8004906d475e05`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 16.2 MB (16209314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862025c91bde921b5cbc7345a2ace01654d8563870616a5ad60305da39e0a1`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 1.2 MB (1232648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4f13334e150c465bb2a85a4cf7c1b6f8cb3eb112bb98b7cdee3ed7b9928be`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 45.4 MB (45413511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3bf184cc7184732ad3551c915100fdac47df4e8d0bbc403340bbb61ef83f8e`  
		Last Modified: Tue, 17 Mar 2026 02:49:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662617661e0afde65f790710b7bc09ebc4a41f8a331b01f474a53e531930d88`  
		Last Modified: Tue, 17 Mar 2026 02:49:44 GMT  
		Size: 52.9 MB (52914512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e3d16726bac9043b08884dd54073770b70e21c1adac99f556d2ec78c0c9b3f`  
		Last Modified: Tue, 17 Mar 2026 02:49:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:630dc769d37bf584cf595776073b772707a78cd76e5418c2155c7e9c030e683b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f66e9f1c73ded8a88e09ee918c043bd04e5bcb19bf6ef00d32440ad2daad72`

```dockerfile
```

-	Layers:
	-	`sha256:de8104fcc429251fb1fda9ed26bd0aca4b09c7552f033abdbde199c35c3c757e`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6fc66ca6b8d54f7bfaf8dfc95c10b0dbdad4913cb0c4d850254ab3cc365de7`  
		Last Modified: Tue, 17 Mar 2026 02:49:41 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:ada7dcfbd6cd0e8fe614285f90be65f2b609850c6447fb9d34d49af0071721d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081c9417c8f5c18e12b951d84e4faac1d96f3a233d3970ffb7607ad802fda4be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 02:59:34 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 02:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:49 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df339bed319fdd8de6f4208b5f9d4c55dff7d6048859b27073939d45ca9993a3`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be127bac61685f5e5c9c08d6d8dc2fdded5d51f05879f079878c790fa4ed21`  
		Last Modified: Tue, 17 Mar 2026 03:00:07 GMT  
		Size: 17.9 MB (17888514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a10a35f57460bf17e201ca809b66febd1b0ad9c4eb2ce18eb86fb217f007963`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 1.2 MB (1220054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c00ad6d00bfaab00e033f6ea96dd01a532ac6fb496f20c6f03e708afbe080`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 45.6 MB (45617060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4000f376411bd7a134155344d5d0973f6572fea39089439e1346a89a154c50f7`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab142b63d3d02bdbe0c588f513d60a7165cb69fd41decfa7f7dc95be45f70713`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 52.9 MB (52914363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812da46cd96e726eb6b3268a352d8a66118b3b26f09483823d3379e7a428a939`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:79c9891cd92bccc8bcc390e203f0a3937eeb6677c87476510af40d3f53cf642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05f52e0f266413f489f6fcaa908ee03b8ce88100258d45d82f89ef18ab672f`

```dockerfile
```

-	Layers:
	-	`sha256:acb60ded2b756e0e9e3724926123424cbf0c8a18dec94d2e281af07ede67f08a`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd93984ef667b433881565357fb7b4f33d68039364e7e6cfe7f3ede4fd5a8d`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:6eb375e1e70b4d0c1043560740cf35e1c092a57c789a1b5ab3b73e4712573369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148456276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78eb4cceb4186629456b4d85662ceb85552043b42815b0040686a900cdfae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 18:03:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:04 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:04 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0cbb4c4e20ebb33dd999528877033777abce6ac7ba4bcf491cefde83202487`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 42.7 MB (42742152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e9ab86808875414f35ec4d4f6e5fb738e11e915034dccd7bd2d0fc20b6641`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 52.9 MB (52914659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a95eebf8bcf16c01a7abb0f6de19b873d1cb1b6c6ba8cfa0ef40832a2ecfc`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a654bf8943c1706a9014e08dacbba0394522abda99a17523b8190c63c6d3f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9333b30d3b9b096019f8c876371b3e66308a7f84db7a9ac0f0a8be473315a`

```dockerfile
```

-	Layers:
	-	`sha256:6316c32cb26befe75f4a43768136066f477a297cfddeb850898cbddcfb7636f6`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f89cc1f6410a780d2a4da15aab47082e308d9d59afe5ab5c6299fb90275e9d`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 36.4 KB (36397 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:fc8eeff22bd21e4deae972ca136b304d95bdcb68733a82b5c043000454dced00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563513928131e9a28cfa9c225b98313c49336f68b0957cc23e9c353603bb4a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:20:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:22:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:22:44 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:22:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Mar 2026 11:22:44 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Mar 2026 11:24:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:24:30 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:24:32 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:24:32 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87fed72d1adc5a92a1bfaa546f1358af32e80a7b8c32fcd489d0dc2d671148`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bad9916e1a89973ba8f309662fad28d6e23251293eb5e722896dcb7a7bc05a`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 17.5 MB (17455212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4b63a9ebcbe21fbe9d25183d82e3181395968700ff5b552fbf3e4db58bdd16`  
		Last Modified: Tue, 17 Mar 2026 11:25:23 GMT  
		Size: 1.2 MB (1241086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1692ab4651125cff24f5e1210b8a4fe03e3390e3e096bef9dc024a225d1cc49`  
		Last Modified: Tue, 17 Mar 2026 11:25:25 GMT  
		Size: 41.3 MB (41302617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30bb2c4038bf70b0f367a7c602be681dbb55dd48744f041e9420eb35ee6745`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26393507fa42481ea67f620f43fb8c66f3130fc06d9bdbf849439834a274b08`  
		Last Modified: Tue, 17 Mar 2026 11:25:28 GMT  
		Size: 52.9 MB (52915323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c03bd184e759fde5abc9fdcb16f46c8fbad84289541eb9beffcfbb98ccabdbd`  
		Last Modified: Tue, 17 Mar 2026 11:25:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:fda4630ac60a4304b85bf07516b53fe7adceacc53946912744b05eb5c51ec207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e4f376d1e28a2f1b92ab6288da8668d4954bf485dd1b570979c3e4df45588c`

```dockerfile
```

-	Layers:
	-	`sha256:ebc54e94368edbce6a1ae499c26da64270991b6db7da6e7dfc96523713ae303e`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cfa8490820696b7f33a860d5db0c9c958202ec9211f478a486dba079714d9`  
		Last Modified: Tue, 17 Mar 2026 11:25:24 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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

### `cassandra:5` - linux; amd64

```console
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5-bookworm`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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

### `cassandra:5-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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

### `cassandra:5.0` - linux; amd64

```console
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0-bookworm`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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

### `cassandra:5.0-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0.6`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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

### `cassandra:5.0.6` - linux; amd64

```console
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0.6-bookworm`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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

### `cassandra:5.0.6-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:bookworm`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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

### `cassandra:bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:latest`

```console
$ docker pull cassandra@sha256:b494afb347bfd20765d80817d89d9e6e31ae77a339bfb34e82c6ea868a51c9c1
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
$ docker pull cassandra@sha256:a2ca8f048d531e9c1714c701cc3c8971f2c1627eaf8a762a0e7e3e83167880b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494de8b59dac2c966544193ed857b3bbd0b54c1f49f032dab1e808e20843225f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:55:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:55:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:55:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883331bfdbbf7822445798a1d5f9d874a34941d75b3b85ba7bd0bcc9c4e2f8d`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55097fdf8add3d84f9af8a061d3cdde10658950d32370de51629709bf69d0e0`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 18.2 MB (18150029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f0b6a6c31f95e46046eee41f00336d0a48a4a051e48aaecc3d389dfb78e43`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 1.3 MB (1266560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5c7d9e1c6eea8c27c903f93fe6271f79629f146c98da2e887bb93cebef796`  
		Last Modified: Tue, 17 Mar 2026 02:55:53 GMT  
		Size: 47.4 MB (47429832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dddef10ea497e9d656d6965cbe13ffb1ed3fa68e6d0008ef7cb7ac454e92bb`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5936ae2ca84403a21ed7aebc13f708f347dd32689a2e1a9ef37318f54866d7f8`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 73.2 MB (73245797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce294f2c05d34d649a0be35a9827953b1001c27dcad71258dfb423e96080f4`  
		Last Modified: Tue, 17 Mar 2026 02:55:54 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:1b2ca5e661f45e045f7fa8006f6e53c0bd779fc59c3db7f6c737ecf1ab680f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce049a0798145d45f0827ff301ca8f5b9fcebd2efbd55cc1818616329e2fdc63`

```dockerfile
```

-	Layers:
	-	`sha256:03772bf4d7b1651b0e349d38a37419bcc91e5526fcc2bfc707872e3022a24ca9`  
		Last Modified: Tue, 17 Mar 2026 02:55:52 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed48d995d71f111059e0fff49f43b3bccb16d0d0cef549361bf22a74c453991`  
		Last Modified: Tue, 17 Mar 2026 02:55:51 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:49065dac8c25634f169f7ca529d778fad6cafc2237d0befa1c8ce143c5614ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c339b323bdbac521a470557191d5a983c9da3e2a9c1853c7325dfe738c6af4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:48:33 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:48:53 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:48:53 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:48:53 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:49:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:49:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:49:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5c0697f7c5afacee34a4a0dfceccd8895923b53d5d5de07b0439be6a004b2`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8e03a307c0d751fd5ba8f41b2cbf1b5d0b51b36c553046b1a022804cf686`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 16.2 MB (16209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee42c4e88b43519a25a638ea3c0b7f446c2c47c4ba3bb71f99bf1733ed80e71`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 1.2 MB (1232651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca189295b37d21ff589a7a6e93985c4ae789b6c757dbc679d492c995590f02`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 45.0 MB (45037269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c3fcd7239fc162a4496896deed9bf3108eff7e6f9f53bb6c1d11b2515a8b7`  
		Last Modified: Tue, 17 Mar 2026 02:49:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92bdbb64f11cc2960dc9d1e8b153f88b634a79141604fa3e25791caabe8f8`  
		Last Modified: Tue, 17 Mar 2026 02:49:30 GMT  
		Size: 73.2 MB (73245885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037cdaba78837410d3c6cdc7180a952684e8422d5cb3d059e53d49128d94553`  
		Last Modified: Tue, 17 Mar 2026 02:49:29 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:bd2af614a8f62c560c38cca9220730d7ea0da07b9154847bf28eb5800a400d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e162dac28a0b380b219c628c15e2da031232ca7be5688e2f467c9767fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:d3564405156b9f7edd8e1b3c05827eccb85c4c367fd1e94b203079b6e7c17366`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9309567bbe908c9fab055cf409ebaf0bbcef804ca406c52af7e2f8b7850e127`  
		Last Modified: Tue, 17 Mar 2026 02:49:27 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:129e73530221a272805cd238ce3e5904df95f346133d0b8e02b9389a8d0de8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff038be5375f4ca20e40c4eedcc6ea6e48f7d454506161a28f1d63a7efda85bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 02:59:31 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:31 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 02:59:31 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 02:59:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 02:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:47 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 02:59:47 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f9be4d1342706275be7c0e4c515104c1129fe9b341d10b56e86ba36191efb`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb36c4ad1202838a34a7c6efd6a262625bd8201a9d50c8e04c4be051a09b5`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 17.9 MB (17888553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24823a583934dedf0ac17e60acf86b0f9fb179c881bc5d366acddaee1d529993`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf8f0afe95b663bd5ec2e6f65402e88d5a429ae6ca29afec15f8903ff13a8a`  
		Last Modified: Tue, 17 Mar 2026 03:00:03 GMT  
		Size: 46.9 MB (46910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6597b8bfd2f387bf8290c2ee78bbfaab3ff592927572713bd58a77634c8b2767`  
		Last Modified: Tue, 17 Mar 2026 03:00:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d8173fc874d06000d549c25a8b747df30d2e22a33a347b413817905135e29`  
		Last Modified: Tue, 17 Mar 2026 03:00:05 GMT  
		Size: 73.2 MB (73245728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5561028c6600b5daa64c64c8575c6b799e094b60a7a5cb64007e1e082553f73`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:a3b3504fa0d5106b9410f905e100fc9648a876c18322ab9269d67b18ee26bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4ca6b0fcf4d7916dd0dfc5bf012dfbbd33db63cfd2ded42029ba9ba15d612`

```dockerfile
```

-	Layers:
	-	`sha256:2ae5d781de5b5750e2d23aa527bef836942164664b241566915828deaaad69bd`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08223087bb2db23d350300aa08c4dcfd7422a36bad3a8a6032b859650bdb556`  
		Last Modified: Tue, 17 Mar 2026 03:00:01 GMT  
		Size: 37.2 KB (37165 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:63880b8122464c3fac8634d330f3d294cbf82dd34f52c2619968fa08e85c126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173373084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661655ab48669981ad3dbed3950bce0a401be12ee247022aa78d3fe6b20ebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:01:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 18:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:02:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:02:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 18:02:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:02:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 18:02:25 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 18:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 18:03:06 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 18:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:09 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 18:03:09 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56944593f159efe8ecc3218a9e0dda7554aea19baaea6b2eeddfb97809908d23`  
		Last Modified: Tue, 17 Mar 2026 18:03:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d511b53f266ab963a7523889602e6a11c78294e54a9494d290486c2a7590e65`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 19.5 MB (19493143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905f1fb03f7f777f578673b2b92134d02f965f04d9ce9395c3e0dfd9290259`  
		Last Modified: Tue, 17 Mar 2026 18:03:31 GMT  
		Size: 1.2 MB (1225498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37310a89abca1de58482620141151a3ad1f21e6f8f414f3ac00a46af52776d40`  
		Last Modified: Tue, 17 Mar 2026 18:03:36 GMT  
		Size: 47.3 MB (47327562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f8c9074834170161a8b016c87ec0971b98016e04d628660e008f4df031666`  
		Last Modified: Tue, 17 Mar 2026 18:03:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52976986c67159bdfd6580a76722683655300f0c27e4705151c02f18e1cbe516`  
		Last Modified: Tue, 17 Mar 2026 18:03:37 GMT  
		Size: 73.2 MB (73246055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968cb836853486d0975111ea9034f509b05a0d4cde263a02cdc3cea56ea9344`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:6200d6880dfbf7bb977e0711f623369dd954b05c6a8d8493c9b07ca3b8e70af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665d028b1761dfcf36b54c369b0df36b37f10eb6963857ddf1278e7da2db3cc`

```dockerfile
```

-	Layers:
	-	`sha256:f32c9897f5047fbf85d4893bbba86b57481bee5020e1574d5b756f183699f848`  
		Last Modified: Tue, 17 Mar 2026 18:03:34 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d07006ccdac0829193a9e8a48c8b58355e750a598a813e31146af96cdc31bb`  
		Last Modified: Tue, 17 Mar 2026 18:03:33 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; s390x

```console
$ docker pull cassandra@sha256:8fe2c65f81bf4430423984741c102af18df2a663cc3e06934bb52e5c662682ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163235562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c9f725aa42327f4c94d2d20f648c122cb72c32951545bccae48a2636221a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:19:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Mar 2026 11:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 11:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
RUN java --version # buildkit
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Mar 2026 11:23:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:23:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Mar 2026 11:23:06 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Mar 2026 11:25:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Mar 2026 11:25:13 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Mar 2026 11:25:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 11:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:25:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Mar 2026 11:25:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f9a2d43fbce9d2954bf4de90ede68e8b971b1482f4f17f7dfbed3ba61ea83`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a5d09017c3365748c473946d7cbdf032b40ec67632b2466d37843ddb906902`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 17.5 MB (17455113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12840f13db80cee5e6bb62fd5f05fcd97267cb0527eccd2652f2799b59192bc2`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 1.2 MB (1241073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415bf44ece2737d57f19d1556ca1348f65001ff448b9f61e694cce8137c2b196`  
		Last Modified: Tue, 17 Mar 2026 11:25:58 GMT  
		Size: 44.4 MB (44398532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda070f96950a2c63ee8a305a8a5f413cf67c0d916a543a0f1218d6863f3ee4b`  
		Last Modified: Tue, 17 Mar 2026 11:25:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2a9de7fbb8f622f5a405efc405902e401b4b030595ee282e861f29214a36d`  
		Last Modified: Tue, 17 Mar 2026 11:25:59 GMT  
		Size: 73.2 MB (73246866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df959837dd5bc46bb03dcc2adc7613e12b784828abe2acc06893ec4301373f8d`  
		Last Modified: Tue, 17 Mar 2026 11:25:57 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:f26f963fabf93fba12a70353a99b45221d62a4811a83b69ddc4667f54efb1291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646ed14cf5c87060b8da1ae41ce8e5d986bd6ccb64d77625f406edf6a51f095`

```dockerfile
```

-	Layers:
	-	`sha256:79edf9c5e268008950668ab1073ccbeb89e9331337871ae5d1aa9816d60a6729`  
		Last Modified: Tue, 17 Mar 2026 11:25:54 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e8a5c0759f1728a68702067970165c8e51b3e9b2a8eca8f598aad43c224c37`  
		Last Modified: Tue, 17 Mar 2026 11:25:53 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json
