<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `cassandra`

-	[`cassandra:4`](#cassandra4)
-	[`cassandra:4-bookworm`](#cassandra4-bookworm)
-	[`cassandra:4.0`](#cassandra40)
-	[`cassandra:4.0-bookworm`](#cassandra40-bookworm)
-	[`cassandra:4.0.20`](#cassandra4020)
-	[`cassandra:4.0.20-bookworm`](#cassandra4020-bookworm)
-	[`cassandra:4.1`](#cassandra41)
-	[`cassandra:4.1-bookworm`](#cassandra41-bookworm)
-	[`cassandra:4.1.11`](#cassandra4111)
-	[`cassandra:4.1.11-bookworm`](#cassandra4111-bookworm)
-	[`cassandra:5`](#cassandra5)
-	[`cassandra:5-bookworm`](#cassandra5-bookworm)
-	[`cassandra:5.0`](#cassandra50)
-	[`cassandra:5.0-bookworm`](#cassandra50-bookworm)
-	[`cassandra:5.0.8`](#cassandra508)
-	[`cassandra:5.0.8-bookworm`](#cassandra508-bookworm)
-	[`cassandra:bookworm`](#cassandrabookworm)
-	[`cassandra:latest`](#cassandralatest)

## `cassandra:4`

```console
$ docker pull cassandra@sha256:0627dca3236196ff04f81a04aad228bc17fc1f7968663acd45ca3fcfee7ec46a
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
$ docker pull cassandra@sha256:342d5a5e47bbdb1724592d9aa37f9b01469c6cdcb22acf6cbfbb1b2522e2a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe10241b56df781c9275120397ee51345ad20d9238721b4f1f3373f57a317e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:13:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f814bf989589f826cb7ec95f464d2a5465aaa76d3492dc1d730093680307433`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3970b782aaffaa415ea804d87a1605481ceda218eb8f9635c9ca8a0c2363f6`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 18.1 MB (18149686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f530ff2ab57ddef5a7e1b253ee16eedfca90a338c0f6e4cb1bee37bdc381f1`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.3 MB (1266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5431da1949bab0780fd4087c723abbf7c6909d20d860953a31e83c4815851e`  
		Last Modified: Wed, 24 Jun 2026 02:14:09 GMT  
		Size: 47.3 MB (47335640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abca18f7c231fd110cf397cc70971e8b7348d440bcb6bbc6f313d2186a148f`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dc3a24f948dcf321f4346ac0e0d1b6b49694ee3e1cb2a3444dea67d462f8c`  
		Last Modified: Wed, 24 Jun 2026 02:14:11 GMT  
		Size: 54.2 MB (54194462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b69de202a9a11e6454e669fa8f18c7292da0dd8d9957fdc76c8deabf90e0`  
		Last Modified: Wed, 24 Jun 2026 02:14:10 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:14660d331d5d21fe0904e0ea1409cd70fdeb55c528d3b81457bfb47cfba276a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2803166b69ac2dc40a060fd2a772664f5bb25e04ce10fe58bcef48ade864c4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c569a636f1e9846931511c6a42bed5a0b0621630c4c8bff4f2cefa3f8ed752`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 3.3 MB (3281849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f62a189f88709431f7561a8517694f3c30a952d16eb1870c65d5cbfad1a504`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 36.5 KB (36479 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:5f13d0ca7fd3592daf3051adf47f6b0c0a2452bf7bebe12a54d20ad27e536fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141034460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820a7ee3bfecd10269c3448562f5bf8759e7eccb3d4aadf8318c58158dd9bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 03:36:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:53 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:53 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3198c52e95c21dc7ec4a327deb00b0d701e5da2b6911d9025fc7995a35b58b0`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d868e44b7c86f4a9623f4555ad3b0aac9d8b2a36ae58d4216079e9a8c3e303`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 16.2 MB (16215470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05d70349e8bf227b20a848eea191e5479fa45e2fae8323e022fb4634d8a06e`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 1.2 MB (1232627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce9f099f1ec9cd1f9087d883337e0f0caee3a078e54353320a182391d1d7ae`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 45.4 MB (45444950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb689aa6e5eb8ef6ebc6684f4824f2d53fe0cdf8adc02f4a4dda67ca09efca9`  
		Last Modified: Wed, 24 Jun 2026 03:37:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c4ec86321f2fb1951d28b8ea5e86ad07ee462b9473bb743cb1ff0278fdbe4`  
		Last Modified: Wed, 24 Jun 2026 03:37:08 GMT  
		Size: 54.2 MB (54194423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68f88d020fe545c298b5628c1760e82a279e766204ad6ea3cef07f9301e5b2`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:11dc148e7bed15d5eb0adf0584408261f744a489e73d255f6e2e6f2febd55620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8f3f2c4235e7ce15ebc601ac7b31febba855950a2202f9f4692848a3128e9d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b94a3942988f4f64760b52d44d9410d15f104ac9ce7c470de75c3990f75bcb`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 3.3 MB (3285579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d0c87117f407ad137d5c56735fad36bfa97b48978dfdc45f84924ca36c4c35`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 36.6 KB (36649 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:2edc3a1ba6d95224c4f2f9dae106dc69e3266c32fc5ee16a7e194fa11b2d25a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147095522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cdfbef19b45c706c1190bc889262ba03c07a1b547b8600b718f1d723c2caf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:20:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf2f0f719de3cfb5e257ee87e8bd34c9f95196219c1aefa7ef30020e6b5698`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811d9c8ed0969752862ca5a9c23f7b62e550a8deece9cf365a1488cdcf05704`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 17.9 MB (17902826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad904963e1479f3e64ca0ae9fccb80c9f61ded11a6689cb81af214b186d0f31`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.2 MB (1220114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3ace08c83ffcce9e15022a5dfad9d5ca5556b2478b06fc0a3133ae710047`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2077f3c118c61f8b7c7280e2df18d0204b86c5dd9d2705a6ee9667c1a5996cb8`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d35534d6526d4845ca93c22feee6982992f1e195b6ce7ef7794f78bdcefd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 54.2 MB (54194517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586a9dc12054e6e2208fc75024a2220a53369c1ce01d9c0ddbab422408f37fd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:4488f0b5de6ba9c811d4293f0dd0993e540af202d21b89851bca0821543810ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaccea88367d11af64d282015a2ac4f3a12df7c6b5d7073e906d7d64711c487f`

```dockerfile
```

-	Layers:
	-	`sha256:a5c4cdf76da33880cd2a042e18c23c5026e57c3b2f0ca8170cee3e0c817db3a5`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 3.3 MB (3282208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35261f221e69211e3944dd810a2604cc1b0cc4a7e7d51759c1176932d807497`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 36.7 KB (36693 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; ppc64le

```console
$ docker pull cassandra@sha256:1a1278953eb3ab9259b9cd391f4e74ebf92010ffca558f77d58b8dfd85d2616a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149800407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0674fc93d88050d7315897c8fad0b2adc52ed03b6ce2b1fe5b2a7ea88c379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 07:44:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:24 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df50698bd54dc04ad6d578f419f5f36a0c401f29a84bb87e7ea1767e1ec3dad`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 54.2 MB (54194650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e0b57aed13290ec341c3b8d96ccf9096203434c2570bb73219288c3a75701`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:77a293cf5054a5081cedb54271e02cc96184dc982a6c75451bba6e4002174311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef7e942b0024d19628f262ef5505bf7dc9e423b61f8efc614c36eed8ed720ac`

```dockerfile
```

-	Layers:
	-	`sha256:6bb48001caccaaa5525fe40798cdbf235e201e0eb20f2c5f9ac71845e1a63a20`  
		Last Modified: Wed, 24 Jun 2026 07:44:52 GMT  
		Size: 3.3 MB (3286109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462212774e36d284b2b8dc9c7cd6de84216ecca26dbb7dd54a9ac8be846cb459`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 36.6 KB (36553 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; s390x

```console
$ docker pull cassandra@sha256:0b25a4785f7703e6fc9324a43d67f871bba8a57d59176f1231e604e896911323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141132094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c5a2159086e3167b8e97765fe98c3e058c201857514326c499be1e37b566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 04:07:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:10 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5a38564b7ced68fc7e2f1cddb380cb6c238e8fbb476156c3b83d011f5f096`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555aaf2ffdd08dcfe4bfe1184660ab24772d8cc22555958c2de28bc256d8392f`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 54.2 MB (54194514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99755dbdc69b420f50d4ee908a99861a8efac62f7133d06ab96ec34ff37d3ff7`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:6acbe938193d59e328536396e23d3b61c1f161303af33c331c98b95d1ac959f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf87dd3d71d39fff9f5ff84477c10850a90911f316d947402462367947a8e444`

```dockerfile
```

-	Layers:
	-	`sha256:d423c7f079628aa07ca26ad67e9e9f8cb04dfc0ecf37b308f4477cc9b9da98f1`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 3.3 MB (3277991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f9ccb5535afab45f37780dfeeed2d54a227695c04db38914eebfc7b631c3de`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 36.5 KB (36478 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4-bookworm`

```console
$ docker pull cassandra@sha256:0627dca3236196ff04f81a04aad228bc17fc1f7968663acd45ca3fcfee7ec46a
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
$ docker pull cassandra@sha256:342d5a5e47bbdb1724592d9aa37f9b01469c6cdcb22acf6cbfbb1b2522e2a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe10241b56df781c9275120397ee51345ad20d9238721b4f1f3373f57a317e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:13:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f814bf989589f826cb7ec95f464d2a5465aaa76d3492dc1d730093680307433`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3970b782aaffaa415ea804d87a1605481ceda218eb8f9635c9ca8a0c2363f6`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 18.1 MB (18149686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f530ff2ab57ddef5a7e1b253ee16eedfca90a338c0f6e4cb1bee37bdc381f1`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.3 MB (1266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5431da1949bab0780fd4087c723abbf7c6909d20d860953a31e83c4815851e`  
		Last Modified: Wed, 24 Jun 2026 02:14:09 GMT  
		Size: 47.3 MB (47335640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abca18f7c231fd110cf397cc70971e8b7348d440bcb6bbc6f313d2186a148f`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dc3a24f948dcf321f4346ac0e0d1b6b49694ee3e1cb2a3444dea67d462f8c`  
		Last Modified: Wed, 24 Jun 2026 02:14:11 GMT  
		Size: 54.2 MB (54194462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b69de202a9a11e6454e669fa8f18c7292da0dd8d9957fdc76c8deabf90e0`  
		Last Modified: Wed, 24 Jun 2026 02:14:10 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:14660d331d5d21fe0904e0ea1409cd70fdeb55c528d3b81457bfb47cfba276a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2803166b69ac2dc40a060fd2a772664f5bb25e04ce10fe58bcef48ade864c4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c569a636f1e9846931511c6a42bed5a0b0621630c4c8bff4f2cefa3f8ed752`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 3.3 MB (3281849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f62a189f88709431f7561a8517694f3c30a952d16eb1870c65d5cbfad1a504`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 36.5 KB (36479 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:5f13d0ca7fd3592daf3051adf47f6b0c0a2452bf7bebe12a54d20ad27e536fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141034460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820a7ee3bfecd10269c3448562f5bf8759e7eccb3d4aadf8318c58158dd9bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 03:36:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:53 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:53 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3198c52e95c21dc7ec4a327deb00b0d701e5da2b6911d9025fc7995a35b58b0`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d868e44b7c86f4a9623f4555ad3b0aac9d8b2a36ae58d4216079e9a8c3e303`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 16.2 MB (16215470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05d70349e8bf227b20a848eea191e5479fa45e2fae8323e022fb4634d8a06e`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 1.2 MB (1232627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce9f099f1ec9cd1f9087d883337e0f0caee3a078e54353320a182391d1d7ae`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 45.4 MB (45444950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb689aa6e5eb8ef6ebc6684f4824f2d53fe0cdf8adc02f4a4dda67ca09efca9`  
		Last Modified: Wed, 24 Jun 2026 03:37:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c4ec86321f2fb1951d28b8ea5e86ad07ee462b9473bb743cb1ff0278fdbe4`  
		Last Modified: Wed, 24 Jun 2026 03:37:08 GMT  
		Size: 54.2 MB (54194423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68f88d020fe545c298b5628c1760e82a279e766204ad6ea3cef07f9301e5b2`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:11dc148e7bed15d5eb0adf0584408261f744a489e73d255f6e2e6f2febd55620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8f3f2c4235e7ce15ebc601ac7b31febba855950a2202f9f4692848a3128e9d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b94a3942988f4f64760b52d44d9410d15f104ac9ce7c470de75c3990f75bcb`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 3.3 MB (3285579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d0c87117f407ad137d5c56735fad36bfa97b48978dfdc45f84924ca36c4c35`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 36.6 KB (36649 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:2edc3a1ba6d95224c4f2f9dae106dc69e3266c32fc5ee16a7e194fa11b2d25a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147095522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cdfbef19b45c706c1190bc889262ba03c07a1b547b8600b718f1d723c2caf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:20:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf2f0f719de3cfb5e257ee87e8bd34c9f95196219c1aefa7ef30020e6b5698`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811d9c8ed0969752862ca5a9c23f7b62e550a8deece9cf365a1488cdcf05704`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 17.9 MB (17902826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad904963e1479f3e64ca0ae9fccb80c9f61ded11a6689cb81af214b186d0f31`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.2 MB (1220114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3ace08c83ffcce9e15022a5dfad9d5ca5556b2478b06fc0a3133ae710047`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2077f3c118c61f8b7c7280e2df18d0204b86c5dd9d2705a6ee9667c1a5996cb8`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d35534d6526d4845ca93c22feee6982992f1e195b6ce7ef7794f78bdcefd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 54.2 MB (54194517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586a9dc12054e6e2208fc75024a2220a53369c1ce01d9c0ddbab422408f37fd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:4488f0b5de6ba9c811d4293f0dd0993e540af202d21b89851bca0821543810ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaccea88367d11af64d282015a2ac4f3a12df7c6b5d7073e906d7d64711c487f`

```dockerfile
```

-	Layers:
	-	`sha256:a5c4cdf76da33880cd2a042e18c23c5026e57c3b2f0ca8170cee3e0c817db3a5`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 3.3 MB (3282208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35261f221e69211e3944dd810a2604cc1b0cc4a7e7d51759c1176932d807497`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 36.7 KB (36693 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:1a1278953eb3ab9259b9cd391f4e74ebf92010ffca558f77d58b8dfd85d2616a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149800407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0674fc93d88050d7315897c8fad0b2adc52ed03b6ce2b1fe5b2a7ea88c379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 07:44:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:24 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df50698bd54dc04ad6d578f419f5f36a0c401f29a84bb87e7ea1767e1ec3dad`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 54.2 MB (54194650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e0b57aed13290ec341c3b8d96ccf9096203434c2570bb73219288c3a75701`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:77a293cf5054a5081cedb54271e02cc96184dc982a6c75451bba6e4002174311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef7e942b0024d19628f262ef5505bf7dc9e423b61f8efc614c36eed8ed720ac`

```dockerfile
```

-	Layers:
	-	`sha256:6bb48001caccaaa5525fe40798cdbf235e201e0eb20f2c5f9ac71845e1a63a20`  
		Last Modified: Wed, 24 Jun 2026 07:44:52 GMT  
		Size: 3.3 MB (3286109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462212774e36d284b2b8dc9c7cd6de84216ecca26dbb7dd54a9ac8be846cb459`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 36.6 KB (36553 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:0b25a4785f7703e6fc9324a43d67f871bba8a57d59176f1231e604e896911323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141132094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c5a2159086e3167b8e97765fe98c3e058c201857514326c499be1e37b566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 04:07:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:10 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5a38564b7ced68fc7e2f1cddb380cb6c238e8fbb476156c3b83d011f5f096`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555aaf2ffdd08dcfe4bfe1184660ab24772d8cc22555958c2de28bc256d8392f`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 54.2 MB (54194514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99755dbdc69b420f50d4ee908a99861a8efac62f7133d06ab96ec34ff37d3ff7`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:6acbe938193d59e328536396e23d3b61c1f161303af33c331c98b95d1ac959f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf87dd3d71d39fff9f5ff84477c10850a90911f316d947402462367947a8e444`

```dockerfile
```

-	Layers:
	-	`sha256:d423c7f079628aa07ca26ad67e9e9f8cb04dfc0ecf37b308f4477cc9b9da98f1`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 3.3 MB (3277991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f9ccb5535afab45f37780dfeeed2d54a227695c04db38914eebfc7b631c3de`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 36.5 KB (36478 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0`

```console
$ docker pull cassandra@sha256:f9ef8845e54fde1d1e6f569c8ac53840680e8b3c4f9c6196a38026ee651d160b
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
$ docker pull cassandra@sha256:2337788fec695a1c821420c752aa62604a198e94ec9da2bd9700a9552900e6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147071005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd591d5e55e19a7f4d631e9888f4069314ecb42af753a1a728e4df584f28a91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:14:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:14:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:14:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:14:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475cf2e0bf4636b7cae87bce011b7ff9fafa9a9154069a31c7d94eb2f5a518bb`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b5c28c433f9c6cf8bcf5a4bd9b90460d8a197b830407f40e484aa8be1db85d`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 18.1 MB (18149641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299a4a4d4147618f4cae51007bfe057d6d025219d9ea16f0b632009134b6040a`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.3 MB (1266594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd899553f84f574280fee85ae51541d70b653834eb95b251d58732d54f32c7e9`  
		Last Modified: Wed, 24 Jun 2026 02:14:22 GMT  
		Size: 47.3 MB (47335644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d270d1ff259c58313615cd34189238d8765525ecd50ccee236d8d8dd01fb065`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399925fde521c0d9a2aa54502afccd38b593371b066776141784dd59ead428c`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 52.1 MB (52079029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f45090d153695bf3e19047a22fc573930bee1c0aae67571100d93277217d72`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:3de694bde18fa560b03a890d6699e7619bcfe450f8efe3aad2661fae6ef055de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe314dbd65b2d7dbc31b4b5c9c9ab49a0951496720425d1f050e8c089a84911`

```dockerfile
```

-	Layers:
	-	`sha256:20dd55afa0b121ac9a2d7b6e7e907819cbe15ec5da24d6b095b3adf8cc75cacf`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 3.3 MB (3274782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af2c9830d7347d1409f1b32cd75f3cbcb5c1e08c029b017ca0dfb29d9eb7e86d`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:e752bfad40a1f352991210701988254c0f30507c01d3c4de4e74e9acde256969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138919153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6437da8c4b12f8baaeaed274e54a02ef1279ab26ab362fa2ebf3029da47b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 03:36:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:59 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f629d19b19842dfda3c8795578d0f050e7b3136b2d43a23621ab929d211c897`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd4488d525108e531815e34644ee84a088115314e76d852389b5d75154ad4c`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 16.2 MB (16215516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0657eb04a6859ec6c6f6e0d1132644069f4b71a46c39d20834e802cfb589022f`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.2 MB (1232625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257d1bc62663c9756056db832daea598a853eaf9a99ab5df59b4ada277ef102`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 45.4 MB (45444980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc0f875b18a87a6e008ef594888b877239d70afac5f3e6930637e49f524bc4a`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddba6860e72882558ccccc9b9f5cd5b14fe5f7789b411ceb6e070790aedd39`  
		Last Modified: Wed, 24 Jun 2026 03:37:14 GMT  
		Size: 52.1 MB (52079041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356172dc812261f45e4828f02aab7e187ca02792e32e60d4c4636dadeb9e72b`  
		Last Modified: Wed, 24 Jun 2026 03:37:13 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:d2f75be5a87f63b1ed936f221dc0f3667ba628c13cff01a1577f604c7e682c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9745a363b9785a414226dc36561b59c950e4c7b9b2ed5af14c92ae58f6cf10`

```dockerfile
```

-	Layers:
	-	`sha256:d096c783201dfdce816ba1252ae6bef7d059f91d30d6c812d4b580089ad5bdfe`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 3.3 MB (3278496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9af313d41cd7ae79aaed01ecb3ccdaedd39a39ab4ef8e9418a68f8f93e88b289`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 36.0 KB (36025 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8baaba577a6bd7ebe254a2eebb8f87ff69e8a0dc32a15f63690cd3e65a2dd849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144979956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9236b7ccb0de347e1066c6dc5e3c40b6fba7cc0099e5027f5c9683749562cff2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:20:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:54 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:54 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2c74b8ca4cf80f6962b4d46cc0ff8c0163a70a711cbf58e088d4649eff629d`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc67c0cbed57b6e6a2468b3cc0f47070d25f60f8d3c184c6f9ad3d1120166bc`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 17.9 MB (17902795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653171bfa8ea6f87370f4fde2c3240d2f3842c81fbae5a83837e5556c5691aba`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 1.2 MB (1220099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31bcc4b214e3336acc7501ec5660c64efb9bdd71ba44a31c0ad02cd7a8b6a24`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0831307c9950eeb324261b2c7cb0f4af59f471d6bfb625dbe5ff70237bb6ce`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a59f9a1aa628aa0db643f9a5bc6ee6ecd8fc688024ec6cdc72c6b2fe712d1`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 52.1 MB (52078996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d68d98c5dc889d95306ffaa5600def1765bbcc828f5d801722e2267fe9e9e`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:f24bd5634005e094c005a0a4f12f61d19f64bea3a0ba105fa8e1f036276357f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3683c8db974d56f6934723427713d67683dbbe6f4af5f97000b0f5f7b76ade76`

```dockerfile
```

-	Layers:
	-	`sha256:13fdd03821697c8e6918e3b82b018f9d9c4df1b8ac7a782951b16f96695281cf`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 3.3 MB (3275117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd32e04188dd2b7778ca423fa374a493d9b6c52b375eb7d01aa042b489ec46f`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 36.1 KB (36063 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:58230657410dfc8b81ea02e9f818c4592c8d6d8c36162d3f24e1892653e5ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147684951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2f282eec33c5abc715da9b42e745da67b2f713644f1ce5ca6870eef967ada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 07:45:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:45:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:45:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:45:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d359824a320396abf09ffe7619cf8058537243da79998b1b54705cbbfdf9e89`  
		Last Modified: Wed, 24 Jun 2026 07:46:18 GMT  
		Size: 52.1 MB (52079195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2972b74fe6ef0b7864ca4d51fbf0fa7866d81b98f680cdda3c42025df49088`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4ee91f25e4c192a31e00a46406ca4ee0ace9446698d1e66d20a2fc44e0ecac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0508d5bbb89e3b907f3bd5aed5f1793543e1baa5271da2809ae894884b2ff169`

```dockerfile
```

-	Layers:
	-	`sha256:2ce6bf876979a3057985966c8556c94939595407ec532c5ac9c36fdef5ecd503`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 3.3 MB (3279030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9e21f7daaab37b5dd0c4c3ef41e5ac43aefafb0db97aa4d0ab143f48bd619c`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 35.9 KB (35935 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; s390x

```console
$ docker pull cassandra@sha256:1dfac52ac8688bd225c7c209648db4bb9060adef743a50ce9e4ac176d9689b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139016792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c1a0b12e9f2da5e03f6c8ea5aed8a141515358a78bcbb2e253293e430a65a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:07:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 04:08:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:08:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:08:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:08:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c183e8bef1e52157e4dc9f6bf97a56d34a556830139a4f3421b63ab7821c02f`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5fb8ce7211a52e87b1feb45b6b4041c7174412009d276f64f8b5854ac4efa4`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 17.4 MB (17447322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c743e994c52b8c798f5a6447cc843661a8ae2f4959ed74b39b8ec02beeb89209`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.2 MB (1240522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2c7f7ad4205cdc3c900a969be21ce54f3cea32eb436f220169ca0f985d00c5`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccc014190219e03a6237f92cb5f1d36bd48348647ed15dce37127cb175e8699`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0cb20d73e38b48f62bb5a49c2a80c103d7957c65433a4a20bf8742e7f31699`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 52.1 MB (52079151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deafb2904eb6a04dde717d9f3bfe28ae522ae330e96efd9f1649abb2af318b0`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:5e663c64b047c7df5d114cf5da96237df8cfeecae22bddda76c042ad7b7510cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fe65fb1edb557b79bdb55cff33a9081478235e71ce13f1670f6c6a26f5e3c7`

```dockerfile
```

-	Layers:
	-	`sha256:2183a2cef824bc2dd61304bae79b3ffd20fa3385f46affecaf06c36e8c0fc12b`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 3.3 MB (3270924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05b3612f35c6ed45c6f7e83035c1a756717d9bbc539511016b3e4b87f6c329a`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0-bookworm`

```console
$ docker pull cassandra@sha256:f9ef8845e54fde1d1e6f569c8ac53840680e8b3c4f9c6196a38026ee651d160b
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
$ docker pull cassandra@sha256:2337788fec695a1c821420c752aa62604a198e94ec9da2bd9700a9552900e6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147071005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd591d5e55e19a7f4d631e9888f4069314ecb42af753a1a728e4df584f28a91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:14:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:14:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:14:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:14:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475cf2e0bf4636b7cae87bce011b7ff9fafa9a9154069a31c7d94eb2f5a518bb`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b5c28c433f9c6cf8bcf5a4bd9b90460d8a197b830407f40e484aa8be1db85d`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 18.1 MB (18149641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299a4a4d4147618f4cae51007bfe057d6d025219d9ea16f0b632009134b6040a`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.3 MB (1266594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd899553f84f574280fee85ae51541d70b653834eb95b251d58732d54f32c7e9`  
		Last Modified: Wed, 24 Jun 2026 02:14:22 GMT  
		Size: 47.3 MB (47335644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d270d1ff259c58313615cd34189238d8765525ecd50ccee236d8d8dd01fb065`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399925fde521c0d9a2aa54502afccd38b593371b066776141784dd59ead428c`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 52.1 MB (52079029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f45090d153695bf3e19047a22fc573930bee1c0aae67571100d93277217d72`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:3de694bde18fa560b03a890d6699e7619bcfe450f8efe3aad2661fae6ef055de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe314dbd65b2d7dbc31b4b5c9c9ab49a0951496720425d1f050e8c089a84911`

```dockerfile
```

-	Layers:
	-	`sha256:20dd55afa0b121ac9a2d7b6e7e907819cbe15ec5da24d6b095b3adf8cc75cacf`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 3.3 MB (3274782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af2c9830d7347d1409f1b32cd75f3cbcb5c1e08c029b017ca0dfb29d9eb7e86d`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:e752bfad40a1f352991210701988254c0f30507c01d3c4de4e74e9acde256969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138919153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6437da8c4b12f8baaeaed274e54a02ef1279ab26ab362fa2ebf3029da47b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 03:36:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:59 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f629d19b19842dfda3c8795578d0f050e7b3136b2d43a23621ab929d211c897`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd4488d525108e531815e34644ee84a088115314e76d852389b5d75154ad4c`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 16.2 MB (16215516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0657eb04a6859ec6c6f6e0d1132644069f4b71a46c39d20834e802cfb589022f`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.2 MB (1232625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257d1bc62663c9756056db832daea598a853eaf9a99ab5df59b4ada277ef102`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 45.4 MB (45444980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc0f875b18a87a6e008ef594888b877239d70afac5f3e6930637e49f524bc4a`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddba6860e72882558ccccc9b9f5cd5b14fe5f7789b411ceb6e070790aedd39`  
		Last Modified: Wed, 24 Jun 2026 03:37:14 GMT  
		Size: 52.1 MB (52079041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356172dc812261f45e4828f02aab7e187ca02792e32e60d4c4636dadeb9e72b`  
		Last Modified: Wed, 24 Jun 2026 03:37:13 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:d2f75be5a87f63b1ed936f221dc0f3667ba628c13cff01a1577f604c7e682c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9745a363b9785a414226dc36561b59c950e4c7b9b2ed5af14c92ae58f6cf10`

```dockerfile
```

-	Layers:
	-	`sha256:d096c783201dfdce816ba1252ae6bef7d059f91d30d6c812d4b580089ad5bdfe`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 3.3 MB (3278496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9af313d41cd7ae79aaed01ecb3ccdaedd39a39ab4ef8e9418a68f8f93e88b289`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 36.0 KB (36025 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8baaba577a6bd7ebe254a2eebb8f87ff69e8a0dc32a15f63690cd3e65a2dd849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144979956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9236b7ccb0de347e1066c6dc5e3c40b6fba7cc0099e5027f5c9683749562cff2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:20:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:54 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:54 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2c74b8ca4cf80f6962b4d46cc0ff8c0163a70a711cbf58e088d4649eff629d`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc67c0cbed57b6e6a2468b3cc0f47070d25f60f8d3c184c6f9ad3d1120166bc`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 17.9 MB (17902795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653171bfa8ea6f87370f4fde2c3240d2f3842c81fbae5a83837e5556c5691aba`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 1.2 MB (1220099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31bcc4b214e3336acc7501ec5660c64efb9bdd71ba44a31c0ad02cd7a8b6a24`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0831307c9950eeb324261b2c7cb0f4af59f471d6bfb625dbe5ff70237bb6ce`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a59f9a1aa628aa0db643f9a5bc6ee6ecd8fc688024ec6cdc72c6b2fe712d1`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 52.1 MB (52078996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d68d98c5dc889d95306ffaa5600def1765bbcc828f5d801722e2267fe9e9e`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f24bd5634005e094c005a0a4f12f61d19f64bea3a0ba105fa8e1f036276357f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3683c8db974d56f6934723427713d67683dbbe6f4af5f97000b0f5f7b76ade76`

```dockerfile
```

-	Layers:
	-	`sha256:13fdd03821697c8e6918e3b82b018f9d9c4df1b8ac7a782951b16f96695281cf`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 3.3 MB (3275117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd32e04188dd2b7778ca423fa374a493d9b6c52b375eb7d01aa042b489ec46f`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 36.1 KB (36063 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:58230657410dfc8b81ea02e9f818c4592c8d6d8c36162d3f24e1892653e5ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147684951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2f282eec33c5abc715da9b42e745da67b2f713644f1ce5ca6870eef967ada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 07:45:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:45:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:45:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:45:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d359824a320396abf09ffe7619cf8058537243da79998b1b54705cbbfdf9e89`  
		Last Modified: Wed, 24 Jun 2026 07:46:18 GMT  
		Size: 52.1 MB (52079195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2972b74fe6ef0b7864ca4d51fbf0fa7866d81b98f680cdda3c42025df49088`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4ee91f25e4c192a31e00a46406ca4ee0ace9446698d1e66d20a2fc44e0ecac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0508d5bbb89e3b907f3bd5aed5f1793543e1baa5271da2809ae894884b2ff169`

```dockerfile
```

-	Layers:
	-	`sha256:2ce6bf876979a3057985966c8556c94939595407ec532c5ac9c36fdef5ecd503`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 3.3 MB (3279030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9e21f7daaab37b5dd0c4c3ef41e5ac43aefafb0db97aa4d0ab143f48bd619c`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 35.9 KB (35935 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:1dfac52ac8688bd225c7c209648db4bb9060adef743a50ce9e4ac176d9689b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139016792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c1a0b12e9f2da5e03f6c8ea5aed8a141515358a78bcbb2e253293e430a65a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:07:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 04:08:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:08:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:08:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:08:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c183e8bef1e52157e4dc9f6bf97a56d34a556830139a4f3421b63ab7821c02f`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5fb8ce7211a52e87b1feb45b6b4041c7174412009d276f64f8b5854ac4efa4`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 17.4 MB (17447322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c743e994c52b8c798f5a6447cc843661a8ae2f4959ed74b39b8ec02beeb89209`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.2 MB (1240522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2c7f7ad4205cdc3c900a969be21ce54f3cea32eb436f220169ca0f985d00c5`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccc014190219e03a6237f92cb5f1d36bd48348647ed15dce37127cb175e8699`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0cb20d73e38b48f62bb5a49c2a80c103d7957c65433a4a20bf8742e7f31699`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 52.1 MB (52079151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deafb2904eb6a04dde717d9f3bfe28ae522ae330e96efd9f1649abb2af318b0`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:5e663c64b047c7df5d114cf5da96237df8cfeecae22bddda76c042ad7b7510cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fe65fb1edb557b79bdb55cff33a9081478235e71ce13f1670f6c6a26f5e3c7`

```dockerfile
```

-	Layers:
	-	`sha256:2183a2cef824bc2dd61304bae79b3ffd20fa3385f46affecaf06c36e8c0fc12b`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 3.3 MB (3270924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05b3612f35c6ed45c6f7e83035c1a756717d9bbc539511016b3e4b87f6c329a`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0.20`

```console
$ docker pull cassandra@sha256:f9ef8845e54fde1d1e6f569c8ac53840680e8b3c4f9c6196a38026ee651d160b
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

### `cassandra:4.0.20` - linux; amd64

```console
$ docker pull cassandra@sha256:2337788fec695a1c821420c752aa62604a198e94ec9da2bd9700a9552900e6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147071005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd591d5e55e19a7f4d631e9888f4069314ecb42af753a1a728e4df584f28a91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:14:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:14:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:14:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:14:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475cf2e0bf4636b7cae87bce011b7ff9fafa9a9154069a31c7d94eb2f5a518bb`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b5c28c433f9c6cf8bcf5a4bd9b90460d8a197b830407f40e484aa8be1db85d`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 18.1 MB (18149641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299a4a4d4147618f4cae51007bfe057d6d025219d9ea16f0b632009134b6040a`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.3 MB (1266594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd899553f84f574280fee85ae51541d70b653834eb95b251d58732d54f32c7e9`  
		Last Modified: Wed, 24 Jun 2026 02:14:22 GMT  
		Size: 47.3 MB (47335644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d270d1ff259c58313615cd34189238d8765525ecd50ccee236d8d8dd01fb065`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399925fde521c0d9a2aa54502afccd38b593371b066776141784dd59ead428c`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 52.1 MB (52079029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f45090d153695bf3e19047a22fc573930bee1c0aae67571100d93277217d72`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20` - unknown; unknown

```console
$ docker pull cassandra@sha256:3de694bde18fa560b03a890d6699e7619bcfe450f8efe3aad2661fae6ef055de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe314dbd65b2d7dbc31b4b5c9c9ab49a0951496720425d1f050e8c089a84911`

```dockerfile
```

-	Layers:
	-	`sha256:20dd55afa0b121ac9a2d7b6e7e907819cbe15ec5da24d6b095b3adf8cc75cacf`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 3.3 MB (3274782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af2c9830d7347d1409f1b32cd75f3cbcb5c1e08c029b017ca0dfb29d9eb7e86d`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:e752bfad40a1f352991210701988254c0f30507c01d3c4de4e74e9acde256969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138919153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6437da8c4b12f8baaeaed274e54a02ef1279ab26ab362fa2ebf3029da47b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 03:36:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:59 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f629d19b19842dfda3c8795578d0f050e7b3136b2d43a23621ab929d211c897`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd4488d525108e531815e34644ee84a088115314e76d852389b5d75154ad4c`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 16.2 MB (16215516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0657eb04a6859ec6c6f6e0d1132644069f4b71a46c39d20834e802cfb589022f`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.2 MB (1232625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257d1bc62663c9756056db832daea598a853eaf9a99ab5df59b4ada277ef102`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 45.4 MB (45444980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc0f875b18a87a6e008ef594888b877239d70afac5f3e6930637e49f524bc4a`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddba6860e72882558ccccc9b9f5cd5b14fe5f7789b411ceb6e070790aedd39`  
		Last Modified: Wed, 24 Jun 2026 03:37:14 GMT  
		Size: 52.1 MB (52079041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356172dc812261f45e4828f02aab7e187ca02792e32e60d4c4636dadeb9e72b`  
		Last Modified: Wed, 24 Jun 2026 03:37:13 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20` - unknown; unknown

```console
$ docker pull cassandra@sha256:d2f75be5a87f63b1ed936f221dc0f3667ba628c13cff01a1577f604c7e682c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9745a363b9785a414226dc36561b59c950e4c7b9b2ed5af14c92ae58f6cf10`

```dockerfile
```

-	Layers:
	-	`sha256:d096c783201dfdce816ba1252ae6bef7d059f91d30d6c812d4b580089ad5bdfe`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 3.3 MB (3278496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9af313d41cd7ae79aaed01ecb3ccdaedd39a39ab4ef8e9418a68f8f93e88b289`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 36.0 KB (36025 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8baaba577a6bd7ebe254a2eebb8f87ff69e8a0dc32a15f63690cd3e65a2dd849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144979956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9236b7ccb0de347e1066c6dc5e3c40b6fba7cc0099e5027f5c9683749562cff2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:20:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:54 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:54 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2c74b8ca4cf80f6962b4d46cc0ff8c0163a70a711cbf58e088d4649eff629d`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc67c0cbed57b6e6a2468b3cc0f47070d25f60f8d3c184c6f9ad3d1120166bc`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 17.9 MB (17902795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653171bfa8ea6f87370f4fde2c3240d2f3842c81fbae5a83837e5556c5691aba`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 1.2 MB (1220099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31bcc4b214e3336acc7501ec5660c64efb9bdd71ba44a31c0ad02cd7a8b6a24`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0831307c9950eeb324261b2c7cb0f4af59f471d6bfb625dbe5ff70237bb6ce`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a59f9a1aa628aa0db643f9a5bc6ee6ecd8fc688024ec6cdc72c6b2fe712d1`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 52.1 MB (52078996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d68d98c5dc889d95306ffaa5600def1765bbcc828f5d801722e2267fe9e9e`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20` - unknown; unknown

```console
$ docker pull cassandra@sha256:f24bd5634005e094c005a0a4f12f61d19f64bea3a0ba105fa8e1f036276357f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3683c8db974d56f6934723427713d67683dbbe6f4af5f97000b0f5f7b76ade76`

```dockerfile
```

-	Layers:
	-	`sha256:13fdd03821697c8e6918e3b82b018f9d9c4df1b8ac7a782951b16f96695281cf`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 3.3 MB (3275117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd32e04188dd2b7778ca423fa374a493d9b6c52b375eb7d01aa042b489ec46f`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 36.1 KB (36063 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20` - linux; ppc64le

```console
$ docker pull cassandra@sha256:58230657410dfc8b81ea02e9f818c4592c8d6d8c36162d3f24e1892653e5ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147684951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2f282eec33c5abc715da9b42e745da67b2f713644f1ce5ca6870eef967ada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 07:45:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:45:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:45:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:45:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d359824a320396abf09ffe7619cf8058537243da79998b1b54705cbbfdf9e89`  
		Last Modified: Wed, 24 Jun 2026 07:46:18 GMT  
		Size: 52.1 MB (52079195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2972b74fe6ef0b7864ca4d51fbf0fa7866d81b98f680cdda3c42025df49088`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4ee91f25e4c192a31e00a46406ca4ee0ace9446698d1e66d20a2fc44e0ecac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0508d5bbb89e3b907f3bd5aed5f1793543e1baa5271da2809ae894884b2ff169`

```dockerfile
```

-	Layers:
	-	`sha256:2ce6bf876979a3057985966c8556c94939595407ec532c5ac9c36fdef5ecd503`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 3.3 MB (3279030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9e21f7daaab37b5dd0c4c3ef41e5ac43aefafb0db97aa4d0ab143f48bd619c`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 35.9 KB (35935 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20` - linux; s390x

```console
$ docker pull cassandra@sha256:1dfac52ac8688bd225c7c209648db4bb9060adef743a50ce9e4ac176d9689b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139016792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c1a0b12e9f2da5e03f6c8ea5aed8a141515358a78bcbb2e253293e430a65a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:07:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 04:08:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:08:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:08:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:08:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c183e8bef1e52157e4dc9f6bf97a56d34a556830139a4f3421b63ab7821c02f`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5fb8ce7211a52e87b1feb45b6b4041c7174412009d276f64f8b5854ac4efa4`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 17.4 MB (17447322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c743e994c52b8c798f5a6447cc843661a8ae2f4959ed74b39b8ec02beeb89209`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.2 MB (1240522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2c7f7ad4205cdc3c900a969be21ce54f3cea32eb436f220169ca0f985d00c5`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccc014190219e03a6237f92cb5f1d36bd48348647ed15dce37127cb175e8699`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0cb20d73e38b48f62bb5a49c2a80c103d7957c65433a4a20bf8742e7f31699`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 52.1 MB (52079151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deafb2904eb6a04dde717d9f3bfe28ae522ae330e96efd9f1649abb2af318b0`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20` - unknown; unknown

```console
$ docker pull cassandra@sha256:5e663c64b047c7df5d114cf5da96237df8cfeecae22bddda76c042ad7b7510cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fe65fb1edb557b79bdb55cff33a9081478235e71ce13f1670f6c6a26f5e3c7`

```dockerfile
```

-	Layers:
	-	`sha256:2183a2cef824bc2dd61304bae79b3ffd20fa3385f46affecaf06c36e8c0fc12b`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 3.3 MB (3270924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05b3612f35c6ed45c6f7e83035c1a756717d9bbc539511016b3e4b87f6c329a`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0.20-bookworm`

```console
$ docker pull cassandra@sha256:f9ef8845e54fde1d1e6f569c8ac53840680e8b3c4f9c6196a38026ee651d160b
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

### `cassandra:4.0.20-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:2337788fec695a1c821420c752aa62604a198e94ec9da2bd9700a9552900e6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147071005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd591d5e55e19a7f4d631e9888f4069314ecb42af753a1a728e4df584f28a91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:34 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:13:50 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:14:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:14:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:14:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:14:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:14:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475cf2e0bf4636b7cae87bce011b7ff9fafa9a9154069a31c7d94eb2f5a518bb`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b5c28c433f9c6cf8bcf5a4bd9b90460d8a197b830407f40e484aa8be1db85d`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 18.1 MB (18149641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299a4a4d4147618f4cae51007bfe057d6d025219d9ea16f0b632009134b6040a`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 1.3 MB (1266594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd899553f84f574280fee85ae51541d70b653834eb95b251d58732d54f32c7e9`  
		Last Modified: Wed, 24 Jun 2026 02:14:22 GMT  
		Size: 47.3 MB (47335644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d270d1ff259c58313615cd34189238d8765525ecd50ccee236d8d8dd01fb065`  
		Last Modified: Wed, 24 Jun 2026 02:14:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399925fde521c0d9a2aa54502afccd38b593371b066776141784dd59ead428c`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 52.1 MB (52079029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f45090d153695bf3e19047a22fc573930bee1c0aae67571100d93277217d72`  
		Last Modified: Wed, 24 Jun 2026 02:14:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:3de694bde18fa560b03a890d6699e7619bcfe450f8efe3aad2661fae6ef055de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe314dbd65b2d7dbc31b4b5c9c9ab49a0951496720425d1f050e8c089a84911`

```dockerfile
```

-	Layers:
	-	`sha256:20dd55afa0b121ac9a2d7b6e7e907819cbe15ec5da24d6b095b3adf8cc75cacf`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 3.3 MB (3274782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af2c9830d7347d1409f1b32cd75f3cbcb5c1e08c029b017ca0dfb29d9eb7e86d`  
		Last Modified: Wed, 24 Jun 2026 02:14:20 GMT  
		Size: 35.9 KB (35873 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:e752bfad40a1f352991210701988254c0f30507c01d3c4de4e74e9acde256969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138919153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6437da8c4b12f8baaeaed274e54a02ef1279ab26ab362fa2ebf3029da47b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 03:36:39 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 03:36:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:59 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f629d19b19842dfda3c8795578d0f050e7b3136b2d43a23621ab929d211c897`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd4488d525108e531815e34644ee84a088115314e76d852389b5d75154ad4c`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 16.2 MB (16215516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0657eb04a6859ec6c6f6e0d1132644069f4b71a46c39d20834e802cfb589022f`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 1.2 MB (1232625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257d1bc62663c9756056db832daea598a853eaf9a99ab5df59b4ada277ef102`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 45.4 MB (45444980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc0f875b18a87a6e008ef594888b877239d70afac5f3e6930637e49f524bc4a`  
		Last Modified: Wed, 24 Jun 2026 03:37:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddba6860e72882558ccccc9b9f5cd5b14fe5f7789b411ceb6e070790aedd39`  
		Last Modified: Wed, 24 Jun 2026 03:37:14 GMT  
		Size: 52.1 MB (52079041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356172dc812261f45e4828f02aab7e187ca02792e32e60d4c4636dadeb9e72b`  
		Last Modified: Wed, 24 Jun 2026 03:37:13 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:d2f75be5a87f63b1ed936f221dc0f3667ba628c13cff01a1577f604c7e682c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9745a363b9785a414226dc36561b59c950e4c7b9b2ed5af14c92ae58f6cf10`

```dockerfile
```

-	Layers:
	-	`sha256:d096c783201dfdce816ba1252ae6bef7d059f91d30d6c812d4b580089ad5bdfe`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 3.3 MB (3278496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9af313d41cd7ae79aaed01ecb3ccdaedd39a39ab4ef8e9418a68f8f93e88b289`  
		Last Modified: Wed, 24 Jun 2026 03:37:11 GMT  
		Size: 36.0 KB (36025 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:8baaba577a6bd7ebe254a2eebb8f87ff69e8a0dc32a15f63690cd3e65a2dd849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144979956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9236b7ccb0de347e1066c6dc5e3c40b6fba7cc0099e5027f5c9683749562cff2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 02:20:38 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 02:20:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:54 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:54 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2c74b8ca4cf80f6962b4d46cc0ff8c0163a70a711cbf58e088d4649eff629d`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc67c0cbed57b6e6a2468b3cc0f47070d25f60f8d3c184c6f9ad3d1120166bc`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 17.9 MB (17902795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653171bfa8ea6f87370f4fde2c3240d2f3842c81fbae5a83837e5556c5691aba`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 1.2 MB (1220099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31bcc4b214e3336acc7501ec5660c64efb9bdd71ba44a31c0ad02cd7a8b6a24`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0831307c9950eeb324261b2c7cb0f4af59f471d6bfb625dbe5ff70237bb6ce`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a59f9a1aa628aa0db643f9a5bc6ee6ecd8fc688024ec6cdc72c6b2fe712d1`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 52.1 MB (52078996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d68d98c5dc889d95306ffaa5600def1765bbcc828f5d801722e2267fe9e9e`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f24bd5634005e094c005a0a4f12f61d19f64bea3a0ba105fa8e1f036276357f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3683c8db974d56f6934723427713d67683dbbe6f4af5f97000b0f5f7b76ade76`

```dockerfile
```

-	Layers:
	-	`sha256:13fdd03821697c8e6918e3b82b018f9d9c4df1b8ac7a782951b16f96695281cf`  
		Last Modified: Wed, 24 Jun 2026 02:21:07 GMT  
		Size: 3.3 MB (3275117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd32e04188dd2b7778ca423fa374a493d9b6c52b375eb7d01aa042b489ec46f`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 36.1 KB (36063 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:58230657410dfc8b81ea02e9f818c4592c8d6d8c36162d3f24e1892653e5ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147684951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2f282eec33c5abc715da9b42e745da67b2f713644f1ce5ca6870eef967ada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 07:45:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:45:54 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:45:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:45:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d359824a320396abf09ffe7619cf8058537243da79998b1b54705cbbfdf9e89`  
		Last Modified: Wed, 24 Jun 2026 07:46:18 GMT  
		Size: 52.1 MB (52079195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2972b74fe6ef0b7864ca4d51fbf0fa7866d81b98f680cdda3c42025df49088`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4ee91f25e4c192a31e00a46406ca4ee0ace9446698d1e66d20a2fc44e0ecac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0508d5bbb89e3b907f3bd5aed5f1793543e1baa5271da2809ae894884b2ff169`

```dockerfile
```

-	Layers:
	-	`sha256:2ce6bf876979a3057985966c8556c94939595407ec532c5ac9c36fdef5ecd503`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 3.3 MB (3279030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9e21f7daaab37b5dd0c4c3ef41e5ac43aefafb0db97aa4d0ab143f48bd619c`  
		Last Modified: Wed, 24 Jun 2026 07:46:16 GMT  
		Size: 35.9 KB (35935 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.20-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:1dfac52ac8688bd225c7c209648db4bb9060adef743a50ce9e4ac176d9689b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139016792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c1a0b12e9f2da5e03f6c8ea5aed8a141515358a78bcbb2e253293e430a65a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:07:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:07:56 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:56 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_VERSION=4.0.20
# Wed, 24 Jun 2026 04:07:56 GMT
ENV CASSANDRA_SHA512=4abd74a1a488360d94ee3bca905c7095cac2e3328577e46622aa41144b1a612844af79ba5ec3e98b26d08fee168511fac128bc6ea2eb2026f981d72bfdeb9fdb
# Wed, 24 Jun 2026 04:08:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:08:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:08:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:08:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:08:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c183e8bef1e52157e4dc9f6bf97a56d34a556830139a4f3421b63ab7821c02f`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5fb8ce7211a52e87b1feb45b6b4041c7174412009d276f64f8b5854ac4efa4`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 17.4 MB (17447322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c743e994c52b8c798f5a6447cc843661a8ae2f4959ed74b39b8ec02beeb89209`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 1.2 MB (1240522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2c7f7ad4205cdc3c900a969be21ce54f3cea32eb436f220169ca0f985d00c5`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccc014190219e03a6237f92cb5f1d36bd48348647ed15dce37127cb175e8699`  
		Last Modified: Wed, 24 Jun 2026 04:08:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0cb20d73e38b48f62bb5a49c2a80c103d7957c65433a4a20bf8742e7f31699`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 52.1 MB (52079151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deafb2904eb6a04dde717d9f3bfe28ae522ae330e96efd9f1649abb2af318b0`  
		Last Modified: Wed, 24 Jun 2026 04:08:32 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.20-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:5e663c64b047c7df5d114cf5da96237df8cfeecae22bddda76c042ad7b7510cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fe65fb1edb557b79bdb55cff33a9081478235e71ce13f1670f6c6a26f5e3c7`

```dockerfile
```

-	Layers:
	-	`sha256:2183a2cef824bc2dd61304bae79b3ffd20fa3385f46affecaf06c36e8c0fc12b`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 3.3 MB (3270924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05b3612f35c6ed45c6f7e83035c1a756717d9bbc539511016b3e4b87f6c329a`  
		Last Modified: Wed, 24 Jun 2026 04:08:30 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1`

```console
$ docker pull cassandra@sha256:0627dca3236196ff04f81a04aad228bc17fc1f7968663acd45ca3fcfee7ec46a
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
$ docker pull cassandra@sha256:342d5a5e47bbdb1724592d9aa37f9b01469c6cdcb22acf6cbfbb1b2522e2a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe10241b56df781c9275120397ee51345ad20d9238721b4f1f3373f57a317e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:13:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f814bf989589f826cb7ec95f464d2a5465aaa76d3492dc1d730093680307433`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3970b782aaffaa415ea804d87a1605481ceda218eb8f9635c9ca8a0c2363f6`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 18.1 MB (18149686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f530ff2ab57ddef5a7e1b253ee16eedfca90a338c0f6e4cb1bee37bdc381f1`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.3 MB (1266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5431da1949bab0780fd4087c723abbf7c6909d20d860953a31e83c4815851e`  
		Last Modified: Wed, 24 Jun 2026 02:14:09 GMT  
		Size: 47.3 MB (47335640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abca18f7c231fd110cf397cc70971e8b7348d440bcb6bbc6f313d2186a148f`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dc3a24f948dcf321f4346ac0e0d1b6b49694ee3e1cb2a3444dea67d462f8c`  
		Last Modified: Wed, 24 Jun 2026 02:14:11 GMT  
		Size: 54.2 MB (54194462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b69de202a9a11e6454e669fa8f18c7292da0dd8d9957fdc76c8deabf90e0`  
		Last Modified: Wed, 24 Jun 2026 02:14:10 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:14660d331d5d21fe0904e0ea1409cd70fdeb55c528d3b81457bfb47cfba276a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2803166b69ac2dc40a060fd2a772664f5bb25e04ce10fe58bcef48ade864c4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c569a636f1e9846931511c6a42bed5a0b0621630c4c8bff4f2cefa3f8ed752`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 3.3 MB (3281849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f62a189f88709431f7561a8517694f3c30a952d16eb1870c65d5cbfad1a504`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 36.5 KB (36479 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:5f13d0ca7fd3592daf3051adf47f6b0c0a2452bf7bebe12a54d20ad27e536fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141034460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820a7ee3bfecd10269c3448562f5bf8759e7eccb3d4aadf8318c58158dd9bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 03:36:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:53 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:53 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3198c52e95c21dc7ec4a327deb00b0d701e5da2b6911d9025fc7995a35b58b0`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d868e44b7c86f4a9623f4555ad3b0aac9d8b2a36ae58d4216079e9a8c3e303`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 16.2 MB (16215470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05d70349e8bf227b20a848eea191e5479fa45e2fae8323e022fb4634d8a06e`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 1.2 MB (1232627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce9f099f1ec9cd1f9087d883337e0f0caee3a078e54353320a182391d1d7ae`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 45.4 MB (45444950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb689aa6e5eb8ef6ebc6684f4824f2d53fe0cdf8adc02f4a4dda67ca09efca9`  
		Last Modified: Wed, 24 Jun 2026 03:37:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c4ec86321f2fb1951d28b8ea5e86ad07ee462b9473bb743cb1ff0278fdbe4`  
		Last Modified: Wed, 24 Jun 2026 03:37:08 GMT  
		Size: 54.2 MB (54194423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68f88d020fe545c298b5628c1760e82a279e766204ad6ea3cef07f9301e5b2`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:11dc148e7bed15d5eb0adf0584408261f744a489e73d255f6e2e6f2febd55620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8f3f2c4235e7ce15ebc601ac7b31febba855950a2202f9f4692848a3128e9d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b94a3942988f4f64760b52d44d9410d15f104ac9ce7c470de75c3990f75bcb`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 3.3 MB (3285579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d0c87117f407ad137d5c56735fad36bfa97b48978dfdc45f84924ca36c4c35`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 36.6 KB (36649 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:2edc3a1ba6d95224c4f2f9dae106dc69e3266c32fc5ee16a7e194fa11b2d25a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147095522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cdfbef19b45c706c1190bc889262ba03c07a1b547b8600b718f1d723c2caf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:20:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf2f0f719de3cfb5e257ee87e8bd34c9f95196219c1aefa7ef30020e6b5698`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811d9c8ed0969752862ca5a9c23f7b62e550a8deece9cf365a1488cdcf05704`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 17.9 MB (17902826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad904963e1479f3e64ca0ae9fccb80c9f61ded11a6689cb81af214b186d0f31`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.2 MB (1220114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3ace08c83ffcce9e15022a5dfad9d5ca5556b2478b06fc0a3133ae710047`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2077f3c118c61f8b7c7280e2df18d0204b86c5dd9d2705a6ee9667c1a5996cb8`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d35534d6526d4845ca93c22feee6982992f1e195b6ce7ef7794f78bdcefd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 54.2 MB (54194517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586a9dc12054e6e2208fc75024a2220a53369c1ce01d9c0ddbab422408f37fd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:4488f0b5de6ba9c811d4293f0dd0993e540af202d21b89851bca0821543810ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaccea88367d11af64d282015a2ac4f3a12df7c6b5d7073e906d7d64711c487f`

```dockerfile
```

-	Layers:
	-	`sha256:a5c4cdf76da33880cd2a042e18c23c5026e57c3b2f0ca8170cee3e0c817db3a5`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 3.3 MB (3282208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35261f221e69211e3944dd810a2604cc1b0cc4a7e7d51759c1176932d807497`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 36.7 KB (36693 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; ppc64le

```console
$ docker pull cassandra@sha256:1a1278953eb3ab9259b9cd391f4e74ebf92010ffca558f77d58b8dfd85d2616a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149800407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0674fc93d88050d7315897c8fad0b2adc52ed03b6ce2b1fe5b2a7ea88c379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 07:44:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:24 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df50698bd54dc04ad6d578f419f5f36a0c401f29a84bb87e7ea1767e1ec3dad`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 54.2 MB (54194650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e0b57aed13290ec341c3b8d96ccf9096203434c2570bb73219288c3a75701`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:77a293cf5054a5081cedb54271e02cc96184dc982a6c75451bba6e4002174311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef7e942b0024d19628f262ef5505bf7dc9e423b61f8efc614c36eed8ed720ac`

```dockerfile
```

-	Layers:
	-	`sha256:6bb48001caccaaa5525fe40798cdbf235e201e0eb20f2c5f9ac71845e1a63a20`  
		Last Modified: Wed, 24 Jun 2026 07:44:52 GMT  
		Size: 3.3 MB (3286109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462212774e36d284b2b8dc9c7cd6de84216ecca26dbb7dd54a9ac8be846cb459`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 36.6 KB (36553 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; s390x

```console
$ docker pull cassandra@sha256:0b25a4785f7703e6fc9324a43d67f871bba8a57d59176f1231e604e896911323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141132094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c5a2159086e3167b8e97765fe98c3e058c201857514326c499be1e37b566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 04:07:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:10 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5a38564b7ced68fc7e2f1cddb380cb6c238e8fbb476156c3b83d011f5f096`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555aaf2ffdd08dcfe4bfe1184660ab24772d8cc22555958c2de28bc256d8392f`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 54.2 MB (54194514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99755dbdc69b420f50d4ee908a99861a8efac62f7133d06ab96ec34ff37d3ff7`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:6acbe938193d59e328536396e23d3b61c1f161303af33c331c98b95d1ac959f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf87dd3d71d39fff9f5ff84477c10850a90911f316d947402462367947a8e444`

```dockerfile
```

-	Layers:
	-	`sha256:d423c7f079628aa07ca26ad67e9e9f8cb04dfc0ecf37b308f4477cc9b9da98f1`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 3.3 MB (3277991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f9ccb5535afab45f37780dfeeed2d54a227695c04db38914eebfc7b631c3de`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 36.5 KB (36478 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1-bookworm`

```console
$ docker pull cassandra@sha256:0627dca3236196ff04f81a04aad228bc17fc1f7968663acd45ca3fcfee7ec46a
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
$ docker pull cassandra@sha256:342d5a5e47bbdb1724592d9aa37f9b01469c6cdcb22acf6cbfbb1b2522e2a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe10241b56df781c9275120397ee51345ad20d9238721b4f1f3373f57a317e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:13:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f814bf989589f826cb7ec95f464d2a5465aaa76d3492dc1d730093680307433`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3970b782aaffaa415ea804d87a1605481ceda218eb8f9635c9ca8a0c2363f6`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 18.1 MB (18149686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f530ff2ab57ddef5a7e1b253ee16eedfca90a338c0f6e4cb1bee37bdc381f1`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.3 MB (1266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5431da1949bab0780fd4087c723abbf7c6909d20d860953a31e83c4815851e`  
		Last Modified: Wed, 24 Jun 2026 02:14:09 GMT  
		Size: 47.3 MB (47335640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abca18f7c231fd110cf397cc70971e8b7348d440bcb6bbc6f313d2186a148f`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dc3a24f948dcf321f4346ac0e0d1b6b49694ee3e1cb2a3444dea67d462f8c`  
		Last Modified: Wed, 24 Jun 2026 02:14:11 GMT  
		Size: 54.2 MB (54194462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b69de202a9a11e6454e669fa8f18c7292da0dd8d9957fdc76c8deabf90e0`  
		Last Modified: Wed, 24 Jun 2026 02:14:10 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:14660d331d5d21fe0904e0ea1409cd70fdeb55c528d3b81457bfb47cfba276a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2803166b69ac2dc40a060fd2a772664f5bb25e04ce10fe58bcef48ade864c4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c569a636f1e9846931511c6a42bed5a0b0621630c4c8bff4f2cefa3f8ed752`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 3.3 MB (3281849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f62a189f88709431f7561a8517694f3c30a952d16eb1870c65d5cbfad1a504`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 36.5 KB (36479 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:5f13d0ca7fd3592daf3051adf47f6b0c0a2452bf7bebe12a54d20ad27e536fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141034460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820a7ee3bfecd10269c3448562f5bf8759e7eccb3d4aadf8318c58158dd9bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 03:36:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:53 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:53 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3198c52e95c21dc7ec4a327deb00b0d701e5da2b6911d9025fc7995a35b58b0`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d868e44b7c86f4a9623f4555ad3b0aac9d8b2a36ae58d4216079e9a8c3e303`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 16.2 MB (16215470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05d70349e8bf227b20a848eea191e5479fa45e2fae8323e022fb4634d8a06e`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 1.2 MB (1232627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce9f099f1ec9cd1f9087d883337e0f0caee3a078e54353320a182391d1d7ae`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 45.4 MB (45444950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb689aa6e5eb8ef6ebc6684f4824f2d53fe0cdf8adc02f4a4dda67ca09efca9`  
		Last Modified: Wed, 24 Jun 2026 03:37:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c4ec86321f2fb1951d28b8ea5e86ad07ee462b9473bb743cb1ff0278fdbe4`  
		Last Modified: Wed, 24 Jun 2026 03:37:08 GMT  
		Size: 54.2 MB (54194423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68f88d020fe545c298b5628c1760e82a279e766204ad6ea3cef07f9301e5b2`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:11dc148e7bed15d5eb0adf0584408261f744a489e73d255f6e2e6f2febd55620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8f3f2c4235e7ce15ebc601ac7b31febba855950a2202f9f4692848a3128e9d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b94a3942988f4f64760b52d44d9410d15f104ac9ce7c470de75c3990f75bcb`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 3.3 MB (3285579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d0c87117f407ad137d5c56735fad36bfa97b48978dfdc45f84924ca36c4c35`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 36.6 KB (36649 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:2edc3a1ba6d95224c4f2f9dae106dc69e3266c32fc5ee16a7e194fa11b2d25a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147095522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cdfbef19b45c706c1190bc889262ba03c07a1b547b8600b718f1d723c2caf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:20:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf2f0f719de3cfb5e257ee87e8bd34c9f95196219c1aefa7ef30020e6b5698`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811d9c8ed0969752862ca5a9c23f7b62e550a8deece9cf365a1488cdcf05704`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 17.9 MB (17902826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad904963e1479f3e64ca0ae9fccb80c9f61ded11a6689cb81af214b186d0f31`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.2 MB (1220114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3ace08c83ffcce9e15022a5dfad9d5ca5556b2478b06fc0a3133ae710047`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2077f3c118c61f8b7c7280e2df18d0204b86c5dd9d2705a6ee9667c1a5996cb8`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d35534d6526d4845ca93c22feee6982992f1e195b6ce7ef7794f78bdcefd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 54.2 MB (54194517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586a9dc12054e6e2208fc75024a2220a53369c1ce01d9c0ddbab422408f37fd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:4488f0b5de6ba9c811d4293f0dd0993e540af202d21b89851bca0821543810ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaccea88367d11af64d282015a2ac4f3a12df7c6b5d7073e906d7d64711c487f`

```dockerfile
```

-	Layers:
	-	`sha256:a5c4cdf76da33880cd2a042e18c23c5026e57c3b2f0ca8170cee3e0c817db3a5`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 3.3 MB (3282208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35261f221e69211e3944dd810a2604cc1b0cc4a7e7d51759c1176932d807497`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 36.7 KB (36693 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:1a1278953eb3ab9259b9cd391f4e74ebf92010ffca558f77d58b8dfd85d2616a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149800407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0674fc93d88050d7315897c8fad0b2adc52ed03b6ce2b1fe5b2a7ea88c379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 07:44:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:24 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df50698bd54dc04ad6d578f419f5f36a0c401f29a84bb87e7ea1767e1ec3dad`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 54.2 MB (54194650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e0b57aed13290ec341c3b8d96ccf9096203434c2570bb73219288c3a75701`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:77a293cf5054a5081cedb54271e02cc96184dc982a6c75451bba6e4002174311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef7e942b0024d19628f262ef5505bf7dc9e423b61f8efc614c36eed8ed720ac`

```dockerfile
```

-	Layers:
	-	`sha256:6bb48001caccaaa5525fe40798cdbf235e201e0eb20f2c5f9ac71845e1a63a20`  
		Last Modified: Wed, 24 Jun 2026 07:44:52 GMT  
		Size: 3.3 MB (3286109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462212774e36d284b2b8dc9c7cd6de84216ecca26dbb7dd54a9ac8be846cb459`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 36.6 KB (36553 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:0b25a4785f7703e6fc9324a43d67f871bba8a57d59176f1231e604e896911323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141132094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c5a2159086e3167b8e97765fe98c3e058c201857514326c499be1e37b566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 04:07:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:10 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5a38564b7ced68fc7e2f1cddb380cb6c238e8fbb476156c3b83d011f5f096`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555aaf2ffdd08dcfe4bfe1184660ab24772d8cc22555958c2de28bc256d8392f`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 54.2 MB (54194514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99755dbdc69b420f50d4ee908a99861a8efac62f7133d06ab96ec34ff37d3ff7`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:6acbe938193d59e328536396e23d3b61c1f161303af33c331c98b95d1ac959f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf87dd3d71d39fff9f5ff84477c10850a90911f316d947402462367947a8e444`

```dockerfile
```

-	Layers:
	-	`sha256:d423c7f079628aa07ca26ad67e9e9f8cb04dfc0ecf37b308f4477cc9b9da98f1`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 3.3 MB (3277991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f9ccb5535afab45f37780dfeeed2d54a227695c04db38914eebfc7b631c3de`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 36.5 KB (36478 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1.11`

```console
$ docker pull cassandra@sha256:0627dca3236196ff04f81a04aad228bc17fc1f7968663acd45ca3fcfee7ec46a
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

### `cassandra:4.1.11` - linux; amd64

```console
$ docker pull cassandra@sha256:342d5a5e47bbdb1724592d9aa37f9b01469c6cdcb22acf6cbfbb1b2522e2a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe10241b56df781c9275120397ee51345ad20d9238721b4f1f3373f57a317e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:13:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f814bf989589f826cb7ec95f464d2a5465aaa76d3492dc1d730093680307433`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3970b782aaffaa415ea804d87a1605481ceda218eb8f9635c9ca8a0c2363f6`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 18.1 MB (18149686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f530ff2ab57ddef5a7e1b253ee16eedfca90a338c0f6e4cb1bee37bdc381f1`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.3 MB (1266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5431da1949bab0780fd4087c723abbf7c6909d20d860953a31e83c4815851e`  
		Last Modified: Wed, 24 Jun 2026 02:14:09 GMT  
		Size: 47.3 MB (47335640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abca18f7c231fd110cf397cc70971e8b7348d440bcb6bbc6f313d2186a148f`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dc3a24f948dcf321f4346ac0e0d1b6b49694ee3e1cb2a3444dea67d462f8c`  
		Last Modified: Wed, 24 Jun 2026 02:14:11 GMT  
		Size: 54.2 MB (54194462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b69de202a9a11e6454e669fa8f18c7292da0dd8d9957fdc76c8deabf90e0`  
		Last Modified: Wed, 24 Jun 2026 02:14:10 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11` - unknown; unknown

```console
$ docker pull cassandra@sha256:14660d331d5d21fe0904e0ea1409cd70fdeb55c528d3b81457bfb47cfba276a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2803166b69ac2dc40a060fd2a772664f5bb25e04ce10fe58bcef48ade864c4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c569a636f1e9846931511c6a42bed5a0b0621630c4c8bff4f2cefa3f8ed752`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 3.3 MB (3281849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f62a189f88709431f7561a8517694f3c30a952d16eb1870c65d5cbfad1a504`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 36.5 KB (36479 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:5f13d0ca7fd3592daf3051adf47f6b0c0a2452bf7bebe12a54d20ad27e536fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141034460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820a7ee3bfecd10269c3448562f5bf8759e7eccb3d4aadf8318c58158dd9bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 03:36:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:53 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:53 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3198c52e95c21dc7ec4a327deb00b0d701e5da2b6911d9025fc7995a35b58b0`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d868e44b7c86f4a9623f4555ad3b0aac9d8b2a36ae58d4216079e9a8c3e303`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 16.2 MB (16215470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05d70349e8bf227b20a848eea191e5479fa45e2fae8323e022fb4634d8a06e`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 1.2 MB (1232627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce9f099f1ec9cd1f9087d883337e0f0caee3a078e54353320a182391d1d7ae`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 45.4 MB (45444950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb689aa6e5eb8ef6ebc6684f4824f2d53fe0cdf8adc02f4a4dda67ca09efca9`  
		Last Modified: Wed, 24 Jun 2026 03:37:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c4ec86321f2fb1951d28b8ea5e86ad07ee462b9473bb743cb1ff0278fdbe4`  
		Last Modified: Wed, 24 Jun 2026 03:37:08 GMT  
		Size: 54.2 MB (54194423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68f88d020fe545c298b5628c1760e82a279e766204ad6ea3cef07f9301e5b2`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11` - unknown; unknown

```console
$ docker pull cassandra@sha256:11dc148e7bed15d5eb0adf0584408261f744a489e73d255f6e2e6f2febd55620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8f3f2c4235e7ce15ebc601ac7b31febba855950a2202f9f4692848a3128e9d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b94a3942988f4f64760b52d44d9410d15f104ac9ce7c470de75c3990f75bcb`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 3.3 MB (3285579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d0c87117f407ad137d5c56735fad36bfa97b48978dfdc45f84924ca36c4c35`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 36.6 KB (36649 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:2edc3a1ba6d95224c4f2f9dae106dc69e3266c32fc5ee16a7e194fa11b2d25a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147095522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cdfbef19b45c706c1190bc889262ba03c07a1b547b8600b718f1d723c2caf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:20:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf2f0f719de3cfb5e257ee87e8bd34c9f95196219c1aefa7ef30020e6b5698`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811d9c8ed0969752862ca5a9c23f7b62e550a8deece9cf365a1488cdcf05704`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 17.9 MB (17902826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad904963e1479f3e64ca0ae9fccb80c9f61ded11a6689cb81af214b186d0f31`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.2 MB (1220114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3ace08c83ffcce9e15022a5dfad9d5ca5556b2478b06fc0a3133ae710047`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2077f3c118c61f8b7c7280e2df18d0204b86c5dd9d2705a6ee9667c1a5996cb8`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d35534d6526d4845ca93c22feee6982992f1e195b6ce7ef7794f78bdcefd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 54.2 MB (54194517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586a9dc12054e6e2208fc75024a2220a53369c1ce01d9c0ddbab422408f37fd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11` - unknown; unknown

```console
$ docker pull cassandra@sha256:4488f0b5de6ba9c811d4293f0dd0993e540af202d21b89851bca0821543810ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaccea88367d11af64d282015a2ac4f3a12df7c6b5d7073e906d7d64711c487f`

```dockerfile
```

-	Layers:
	-	`sha256:a5c4cdf76da33880cd2a042e18c23c5026e57c3b2f0ca8170cee3e0c817db3a5`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 3.3 MB (3282208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35261f221e69211e3944dd810a2604cc1b0cc4a7e7d51759c1176932d807497`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 36.7 KB (36693 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11` - linux; ppc64le

```console
$ docker pull cassandra@sha256:1a1278953eb3ab9259b9cd391f4e74ebf92010ffca558f77d58b8dfd85d2616a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149800407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0674fc93d88050d7315897c8fad0b2adc52ed03b6ce2b1fe5b2a7ea88c379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 07:44:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:24 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df50698bd54dc04ad6d578f419f5f36a0c401f29a84bb87e7ea1767e1ec3dad`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 54.2 MB (54194650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e0b57aed13290ec341c3b8d96ccf9096203434c2570bb73219288c3a75701`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11` - unknown; unknown

```console
$ docker pull cassandra@sha256:77a293cf5054a5081cedb54271e02cc96184dc982a6c75451bba6e4002174311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef7e942b0024d19628f262ef5505bf7dc9e423b61f8efc614c36eed8ed720ac`

```dockerfile
```

-	Layers:
	-	`sha256:6bb48001caccaaa5525fe40798cdbf235e201e0eb20f2c5f9ac71845e1a63a20`  
		Last Modified: Wed, 24 Jun 2026 07:44:52 GMT  
		Size: 3.3 MB (3286109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462212774e36d284b2b8dc9c7cd6de84216ecca26dbb7dd54a9ac8be846cb459`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 36.6 KB (36553 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11` - linux; s390x

```console
$ docker pull cassandra@sha256:0b25a4785f7703e6fc9324a43d67f871bba8a57d59176f1231e604e896911323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141132094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c5a2159086e3167b8e97765fe98c3e058c201857514326c499be1e37b566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 04:07:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:10 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5a38564b7ced68fc7e2f1cddb380cb6c238e8fbb476156c3b83d011f5f096`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555aaf2ffdd08dcfe4bfe1184660ab24772d8cc22555958c2de28bc256d8392f`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 54.2 MB (54194514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99755dbdc69b420f50d4ee908a99861a8efac62f7133d06ab96ec34ff37d3ff7`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11` - unknown; unknown

```console
$ docker pull cassandra@sha256:6acbe938193d59e328536396e23d3b61c1f161303af33c331c98b95d1ac959f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf87dd3d71d39fff9f5ff84477c10850a90911f316d947402462367947a8e444`

```dockerfile
```

-	Layers:
	-	`sha256:d423c7f079628aa07ca26ad67e9e9f8cb04dfc0ecf37b308f4477cc9b9da98f1`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 3.3 MB (3277991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f9ccb5535afab45f37780dfeeed2d54a227695c04db38914eebfc7b631c3de`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 36.5 KB (36478 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1.11-bookworm`

```console
$ docker pull cassandra@sha256:0627dca3236196ff04f81a04aad228bc17fc1f7968663acd45ca3fcfee7ec46a
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

### `cassandra:4.1.11-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:342d5a5e47bbdb1724592d9aa37f9b01469c6cdcb22acf6cbfbb1b2522e2a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe10241b56df781c9275120397ee51345ad20d9238721b4f1f3373f57a317e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:13:37 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:13:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f814bf989589f826cb7ec95f464d2a5465aaa76d3492dc1d730093680307433`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3970b782aaffaa415ea804d87a1605481ceda218eb8f9635c9ca8a0c2363f6`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 18.1 MB (18149686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f530ff2ab57ddef5a7e1b253ee16eedfca90a338c0f6e4cb1bee37bdc381f1`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 1.3 MB (1266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5431da1949bab0780fd4087c723abbf7c6909d20d860953a31e83c4815851e`  
		Last Modified: Wed, 24 Jun 2026 02:14:09 GMT  
		Size: 47.3 MB (47335640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abca18f7c231fd110cf397cc70971e8b7348d440bcb6bbc6f313d2186a148f`  
		Last Modified: Wed, 24 Jun 2026 02:14:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dc3a24f948dcf321f4346ac0e0d1b6b49694ee3e1cb2a3444dea67d462f8c`  
		Last Modified: Wed, 24 Jun 2026 02:14:11 GMT  
		Size: 54.2 MB (54194462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b69de202a9a11e6454e669fa8f18c7292da0dd8d9957fdc76c8deabf90e0`  
		Last Modified: Wed, 24 Jun 2026 02:14:10 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:14660d331d5d21fe0904e0ea1409cd70fdeb55c528d3b81457bfb47cfba276a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2803166b69ac2dc40a060fd2a772664f5bb25e04ce10fe58bcef48ade864c4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c569a636f1e9846931511c6a42bed5a0b0621630c4c8bff4f2cefa3f8ed752`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 3.3 MB (3281849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f62a189f88709431f7561a8517694f3c30a952d16eb1870c65d5cbfad1a504`  
		Last Modified: Wed, 24 Jun 2026 02:14:07 GMT  
		Size: 36.5 KB (36479 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:5f13d0ca7fd3592daf3051adf47f6b0c0a2452bf7bebe12a54d20ad27e536fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141034460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820a7ee3bfecd10269c3448562f5bf8759e7eccb3d4aadf8318c58158dd9bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:36:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:34 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 03:36:34 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 03:36:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:53 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:53 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3198c52e95c21dc7ec4a327deb00b0d701e5da2b6911d9025fc7995a35b58b0`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d868e44b7c86f4a9623f4555ad3b0aac9d8b2a36ae58d4216079e9a8c3e303`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 16.2 MB (16215470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05d70349e8bf227b20a848eea191e5479fa45e2fae8323e022fb4634d8a06e`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 1.2 MB (1232627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce9f099f1ec9cd1f9087d883337e0f0caee3a078e54353320a182391d1d7ae`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 45.4 MB (45444950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb689aa6e5eb8ef6ebc6684f4824f2d53fe0cdf8adc02f4a4dda67ca09efca9`  
		Last Modified: Wed, 24 Jun 2026 03:37:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c4ec86321f2fb1951d28b8ea5e86ad07ee462b9473bb743cb1ff0278fdbe4`  
		Last Modified: Wed, 24 Jun 2026 03:37:08 GMT  
		Size: 54.2 MB (54194423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68f88d020fe545c298b5628c1760e82a279e766204ad6ea3cef07f9301e5b2`  
		Last Modified: Wed, 24 Jun 2026 03:37:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:11dc148e7bed15d5eb0adf0584408261f744a489e73d255f6e2e6f2febd55620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8f3f2c4235e7ce15ebc601ac7b31febba855950a2202f9f4692848a3128e9d`

```dockerfile
```

-	Layers:
	-	`sha256:c0b94a3942988f4f64760b52d44d9410d15f104ac9ce7c470de75c3990f75bcb`  
		Last Modified: Wed, 24 Jun 2026 03:37:05 GMT  
		Size: 3.3 MB (3285579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d0c87117f407ad137d5c56735fad36bfa97b48978dfdc45f84924ca36c4c35`  
		Last Modified: Wed, 24 Jun 2026 03:37:04 GMT  
		Size: 36.6 KB (36649 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:2edc3a1ba6d95224c4f2f9dae106dc69e3266c32fc5ee16a7e194fa11b2d25a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147095522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cdfbef19b45c706c1190bc889262ba03c07a1b547b8600b718f1d723c2caf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:20 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:39 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:39 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 02:20:39 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 02:20:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:55 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:55 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf2f0f719de3cfb5e257ee87e8bd34c9f95196219c1aefa7ef30020e6b5698`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811d9c8ed0969752862ca5a9c23f7b62e550a8deece9cf365a1488cdcf05704`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 17.9 MB (17902826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad904963e1479f3e64ca0ae9fccb80c9f61ded11a6689cb81af214b186d0f31`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 1.2 MB (1220114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be3ace08c83ffcce9e15022a5dfad9d5ca5556b2478b06fc0a3133ae710047`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 45.7 MB (45653188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2077f3c118c61f8b7c7280e2df18d0204b86c5dd9d2705a6ee9667c1a5996cb8`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d35534d6526d4845ca93c22feee6982992f1e195b6ce7ef7794f78bdcefd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 54.2 MB (54194517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586a9dc12054e6e2208fc75024a2220a53369c1ce01d9c0ddbab422408f37fd5`  
		Last Modified: Wed, 24 Jun 2026 02:21:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:4488f0b5de6ba9c811d4293f0dd0993e540af202d21b89851bca0821543810ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaccea88367d11af64d282015a2ac4f3a12df7c6b5d7073e906d7d64711c487f`

```dockerfile
```

-	Layers:
	-	`sha256:a5c4cdf76da33880cd2a042e18c23c5026e57c3b2f0ca8170cee3e0c817db3a5`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 3.3 MB (3282208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35261f221e69211e3944dd810a2604cc1b0cc4a7e7d51759c1176932d807497`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 36.7 KB (36693 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:1a1278953eb3ab9259b9cd391f4e74ebf92010ffca558f77d58b8dfd85d2616a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149800407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0674fc93d88050d7315897c8fad0b2adc52ed03b6ce2b1fe5b2a7ea88c379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 07:44:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:24 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:25 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e570b802ccebdb6015c8cead0bb5a5b3d17a51a2d74703bb5ce2b66d542252`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 42.8 MB (42801461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df50698bd54dc04ad6d578f419f5f36a0c401f29a84bb87e7ea1767e1ec3dad`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 54.2 MB (54194650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e0b57aed13290ec341c3b8d96ccf9096203434c2570bb73219288c3a75701`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:77a293cf5054a5081cedb54271e02cc96184dc982a6c75451bba6e4002174311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef7e942b0024d19628f262ef5505bf7dc9e423b61f8efc614c36eed8ed720ac`

```dockerfile
```

-	Layers:
	-	`sha256:6bb48001caccaaa5525fe40798cdbf235e201e0eb20f2c5f9ac71845e1a63a20`  
		Last Modified: Wed, 24 Jun 2026 07:44:52 GMT  
		Size: 3.3 MB (3286109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462212774e36d284b2b8dc9c7cd6de84216ecca26dbb7dd54a9ac8be846cb459`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 36.6 KB (36553 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.11-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:0b25a4785f7703e6fc9324a43d67f871bba8a57d59176f1231e604e896911323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141132094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c5a2159086e3167b8e97765fe98c3e058c201857514326c499be1e37b566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=4.1.11
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=c31ead4e137774964818b3acfc2a16c329cce412ebb003baf447c3d453800a590d970cbe98641bd81539fd7a7fb8a1b6b569e5072c93fc2e18f40eaa638225be
# Wed, 24 Jun 2026 04:07:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:10 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5a38564b7ced68fc7e2f1cddb380cb6c238e8fbb476156c3b83d011f5f096`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 41.4 MB (41353755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555aaf2ffdd08dcfe4bfe1184660ab24772d8cc22555958c2de28bc256d8392f`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 54.2 MB (54194514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99755dbdc69b420f50d4ee908a99861a8efac62f7133d06ab96ec34ff37d3ff7`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.11-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:6acbe938193d59e328536396e23d3b61c1f161303af33c331c98b95d1ac959f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf87dd3d71d39fff9f5ff84477c10850a90911f316d947402462367947a8e444`

```dockerfile
```

-	Layers:
	-	`sha256:d423c7f079628aa07ca26ad67e9e9f8cb04dfc0ecf37b308f4477cc9b9da98f1`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 3.3 MB (3277991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f9ccb5535afab45f37780dfeeed2d54a227695c04db38914eebfc7b631c3de`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 36.5 KB (36478 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5-bookworm`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0-bookworm`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0.8`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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

### `cassandra:5.0.8` - linux; amd64

```console
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5.0.8-bookworm`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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

### `cassandra:5.0.8-bookworm` - linux; amd64

```console
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.8-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.8-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:bookworm`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:latest`

```console
$ docker pull cassandra@sha256:22d9d71f530662daf26c43c458c9d3820e14930941e801dc5fbbf2ca7e5a8a77
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
$ docker pull cassandra@sha256:0deae0a18f6629cfdbf0539098147619ced96ed9491bb0487f6c207e9329dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169133594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c7bd7b45d593badc03fa2775d2dc26f7a20e42c1b68308bbfa242a93ae5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:10 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:13:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:13:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:13:26 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:13:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:13:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:45 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:13:45 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a13751f075a99083923866e6f61f8fc65a7455b2574dd04fc60b1b6d1c49ed`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b800bb4134a152a194dac651f467ffcac7709b7edb93497dd264cbbc46f99`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 18.1 MB (18149694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a43b88491e726285b419d66502578f05a5a23385f5cab54265662a6944661`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 1.3 MB (1266609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e347efbb13616a4e101ea054dd82c5c6c6fc67b54edabc5a123632c7d1e0fc`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 47.6 MB (47558136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2291151ee6cf0515c9b461c74929aaadb526fb048ff44d898d0f00a1b320c3e`  
		Last Modified: Wed, 24 Jun 2026 02:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dab1bd22dbf9737db386bd276216ee27892fd5790539d03f7912d27144b66a`  
		Last Modified: Wed, 24 Jun 2026 02:14:01 GMT  
		Size: 73.9 MB (73919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a6ab9598f31b861cc5fee7df0008f3e71c4cfde2dc54f7df737ef15209e11`  
		Last Modified: Wed, 24 Jun 2026 02:14:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:3668048eebbac1d7345c84b57393d22242878723da350f819d3f8f59112e8dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f3a2c702f9b50156e8156fb8fdf274b0cf6618e3b2db7c99039495a8418f8`

```dockerfile
```

-	Layers:
	-	`sha256:d41ff3dd240137e56d4bb801569f25b2b0f0d6cdd31508dd3e5eb70a5bc5f634`  
		Last Modified: Wed, 24 Jun 2026 02:13:58 GMT  
		Size: 3.3 MB (3306826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95bd8aff389714e21e6b5f16402ccf0cd85242fc490a18e7ed01edb390d494b`  
		Last Modified: Wed, 24 Jun 2026 02:13:57 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:25b4c85100a7e48455c38b473e8704124a9f5eb46b9f4c706304418da1a853cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160440344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9e0d9ecbf52efc269106f6913a3f938f25c9089322ce8f0529e1eb6a63c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:35:53 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 03:36:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:36:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 03:36:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 03:36:13 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:13 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 03:36:13 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 03:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 03:36:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:36:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:36:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 03:36:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c27221e3f3b9fe0777e26a9f7820444e49b2ac942ae848987053a7ad631438`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b345b449d89eb192f72fcd78c57832f9459be6223b1d687d58dcea5882434`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 16.2 MB (16215644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f617ec09950666bf7a7b49b2b26c999095af7f2b0506d36ae5e11a71c0020`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 1.2 MB (1232646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558511450beb75652b3f2967141428898bf39d93eccc3c6c1f6cd92187a696d`  
		Last Modified: Wed, 24 Jun 2026 03:36:49 GMT  
		Size: 45.1 MB (45125982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431082826887abbe9a0ffcdba43fcc4eb48c017623696d9daab46bfff9ce418`  
		Last Modified: Wed, 24 Jun 2026 03:36:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7edfffe154cb502a77f7b2a4d2bf4f1d7598af74b44f279b3d69cce90254a3e`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 73.9 MB (73919082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e956c1c62b4fd5e66cedc7c6d7b998448876604a3bd21531f83d2d88717e7`  
		Last Modified: Wed, 24 Jun 2026 03:36:50 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:f1c63fef50028b851eedf1f18c7f8458785185e342e64255af684112130ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eff26b28ace7950a1c368f73e944a4a6a6bc4e4ae87bd2ce678cd2af56049f`

```dockerfile
```

-	Layers:
	-	`sha256:605eeec062af760e7635577b9dc0a1da16ec64dec8f5aa343d740ad153c059eb`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 3.3 MB (3309309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795d1461156b5fb050ec3d62410d5fb82d4edc2f91b213decd946d3d59c44ac`  
		Last Modified: Wed, 24 Jun 2026 03:36:47 GMT  
		Size: 37.3 KB (37268 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:b293cb20d459934ac3935992917bb968073794f4faafebb1bed92a9851c50117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d08c6eabe84d2d815cbe7bf617c0ffaeb332985cab824403c6f587a6cdab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 02:20:22 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:22 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 02:20:22 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 02:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 02:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:20:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 02:20:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df1a652fda22f638a99ddc6b2d4da32ddaf5e0e6e06ecf2ba7132144643ec1`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299c9cba3c021ac2f6e819067cde395eaef757fd3ee84279a3f8764209605f0`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 17.9 MB (17902770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1452a8fd7325b1ad277f4a848331299711e4c35b49b1eef99b475b66f621a4`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 1.2 MB (1220084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce8213f473782350ea093724557bb58c049bf2d4505af7081564bc7ddb887d`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 47.0 MB (47041116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a51f6966268c46380d557f9c1abd1e0e84c84dc84c2e011737f1cd5e89f1e2`  
		Last Modified: Wed, 24 Jun 2026 02:20:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487c4760efd1dee998347cadb780f2450d1a7734306d61fb9bc993c595812f5`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 73.9 MB (73919028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0ed4fa9844df37f70353764a465bb5ae2ae774e8f8887f60534c0d2020463`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:493ab09afdde400f5f5920c2629cce545d48cad3e9155f5e702348fd89b2e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1040d5934d5ed0c446b8210b5b5347561fe736646d3912229e0350153ca51087`

```dockerfile
```

-	Layers:
	-	`sha256:05fd1d00387efc38df76c126867baf3933cf56423156c1f537cd66efe82602c7`  
		Last Modified: Wed, 24 Jun 2026 02:20:51 GMT  
		Size: 3.3 MB (3306591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b3776dcf46768b32cf499f1f9ff2bed00ef1641677ceeb406d63f4bff7120`  
		Last Modified: Wed, 24 Jun 2026 02:20:50 GMT  
		Size: 37.3 KB (37320 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:9e7526926a693888112f2b783eb8ecab7f3f9c95b70454c586653a7c6d0dcea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174204451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f230a669e54cf865ff8f55caa78105442e580441aea3d6702676ae5938e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:43:15 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 07:43:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 07:43:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 07:43:52 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:43:52 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 07:43:52 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 07:44:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 07:44:25 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 07:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 07:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 07:44:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 07:44:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d287a6148167db59fb8c77e9ef652c87c590cafdbb1196d6fe0e7084c25f1d`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19b6941d71fea8169b86daf0720e7824d7d098ab2ad8553ffb022d9cb431cf`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 19.5 MB (19494391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7804ccb29055eca981db1d4f56af166427f300b4dbbc3787e8a67a8d88f153ad`  
		Last Modified: Wed, 24 Jun 2026 07:44:51 GMT  
		Size: 1.2 MB (1225469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17c2f1e9decb6dfb85edfc5a3266f0be0c217a1e19603aa4973672ca44f18c`  
		Last Modified: Wed, 24 Jun 2026 07:44:56 GMT  
		Size: 47.5 MB (47480915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da02aad40af80bd8e15eb4acd3e0594241d2a05a4fec18ed92b2d50812df86`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e84be954b163ae8dadb7fb27331a89f2feda1d299691697f6d29808cbaa3e`  
		Last Modified: Wed, 24 Jun 2026 07:44:57 GMT  
		Size: 73.9 MB (73919241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211085086dbe7dc9b4f1efbda0eece698d4bf7863de3c0efbe00a6976061b05`  
		Last Modified: Wed, 24 Jun 2026 07:44:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:98324f8b8a05cf38a0ca97d3d0168430d61f3879a50d4df1b0075d26a772f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3348259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4655b082991fd80f07b1f1bc6fc0a41dc0ee4470fdfb72d0352b0f75e51eba`

```dockerfile
```

-	Layers:
	-	`sha256:ad469f1abeb33ab1a3466907d5f9d9994d61b014a35e9a035ee00a307ce0ea37`  
		Last Modified: Wed, 24 Jun 2026 07:44:54 GMT  
		Size: 3.3 MB (3311092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c190e49df590893049d18d717db165e2d699b3045525e4c11c4e55f7ad479c`  
		Last Modified: Wed, 24 Jun 2026 07:44:53 GMT  
		Size: 37.2 KB (37167 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; s390x

```console
$ docker pull cassandra@sha256:741993c327c0c7d4e451c07f4feee282581be82dbc0e8fb08739cb34541ac892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164031654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fa44e208e330072abe593f2d77e6134ca9be21a014c9fc0e61b7e0c95c40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:06:39 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 24 Jun 2026 04:06:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 04:06:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
RUN java --version # buildkit
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 24 Jun 2026 04:06:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:06:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_VERSION=5.0.8
# Wed, 24 Jun 2026 04:06:55 GMT
ENV CASSANDRA_SHA512=06b7af18c8f41dc13dbfdae186d565a5f91e71ea413c3c5373aec8a4e5074c6dee5632a0e5e98c21665f08f7291d7ca384f61a323c02610c6bca51e074b5a0c4
# Wed, 24 Jun 2026 04:07:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
VOLUME [/var/lib/cassandra]
# Wed, 24 Jun 2026 04:07:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 04:07:11 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 24 Jun 2026 04:07:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db179328614ebd4dd9091c198673125e305a9241e9cd42c76383f2caac98d2b`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c0d21980a44f272fb9f5c995c1fbf4d893ba4ef933fc2697c1687361f5d80`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 17.4 MB (17447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c83823edd5ec026fd1bab7156caa5c35fcb441bdc7e17ab97ae06e032f8a78`  
		Last Modified: Wed, 24 Jun 2026 04:07:29 GMT  
		Size: 1.2 MB (1240499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed24b0007713f852d8c8614fb3524fc9bc6b00bc99d15c7a37b5bebaaf2375`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 44.5 MB (44528757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17eee014000b39ad3ec9a2a4b266fb4110e5aafedb327cd2b685983ee0d04a`  
		Last Modified: Wed, 24 Jun 2026 04:07:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ee311c618354250a2908a7a12ba2dafa08ef75bca12029a0aa8e5458bd173`  
		Last Modified: Wed, 24 Jun 2026 04:07:33 GMT  
		Size: 73.9 MB (73919072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafeac6f868b14fb754815d05a504228f7c8072e9a649d6b0b8781fb2486d4f8`  
		Last Modified: Wed, 24 Jun 2026 04:07:32 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:b9786e60b9d4d7c88965168f4f79e75f8be606903c5615a1093bb24ba6edb427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3340044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defbb069f76f1d0f76c3cf39bef96c1708623dad3daf2a1fdc7fcb693afa2e9`

```dockerfile
```

-	Layers:
	-	`sha256:d2c27c21f5616cdcb97444fdf420c1834358e43821b2b51ef70ab63c5841347e`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 3.3 MB (3302962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4e0f4bf325448f8921e0aef4b4618951c0d4974e1ccc514742031d17883a9`  
		Last Modified: Wed, 24 Jun 2026 04:07:31 GMT  
		Size: 37.1 KB (37082 bytes)  
		MIME: application/vnd.in-toto+json
