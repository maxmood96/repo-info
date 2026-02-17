## `cassandra:latest`

```console
$ docker pull cassandra@sha256:8d2d96cbed769b2e9173d4e3522d5cb59ddbba26c636b900600af0e9ef1660b3
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
$ docker pull cassandra@sha256:ebcbeba10dd8fa832decb37e8ca05dd4422ec90ce49c9771e97ce1589fe944b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168323224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dcd41701c814c5bbb5746acc8d7072bfb40ee70fb741e1c8163bebce70d386`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:39:38 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:39:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:39:55 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:39:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:39:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:39:55 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:39:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:39:55 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:39:55 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:39:55 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:39:55 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 21:39:55 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 21:40:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:40:10 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:40:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:40:10 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:40:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93afc517788dc58b4c96164fced22cbc436c54ece0ee8cee4d6aca4fccd649ad`  
		Last Modified: Tue, 17 Feb 2026 21:40:24 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d6644578cf05e456ba3d6dc7a4fd817b68909e9d2a9e9d92a10c8b33c57693`  
		Last Modified: Tue, 17 Feb 2026 21:40:25 GMT  
		Size: 18.1 MB (18149891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e747f38727ca931be0b664b1a6bc9b4ee6c1fd44c57d26b04aede1aa1d34f1c`  
		Last Modified: Tue, 17 Feb 2026 21:40:24 GMT  
		Size: 1.3 MB (1266639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968557cbd4a4357a30a30812b5cb0562a1515853f615142709a2f221e8f73f1e`  
		Last Modified: Tue, 17 Feb 2026 21:40:26 GMT  
		Size: 47.4 MB (47429833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb884c5102dd28a51ad21e2cc13c37c525dcbd872e1f462ae505c62ea4c6a13b`  
		Last Modified: Tue, 17 Feb 2026 21:40:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d807ef6301abec8c43334e1d5263232ae65d2b53e15ce52be36b54ccb0abdaf`  
		Last Modified: Tue, 17 Feb 2026 21:40:27 GMT  
		Size: 73.2 MB (73245913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432bb378e3c32a9d8dcbf539d044182609679448b585e3fe402e012850af0f67`  
		Last Modified: Tue, 17 Feb 2026 21:40:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:07298e79cfb71222f2221e7807d946c445494d871a5b866ad200791f71a549a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d3cbc9ab09434fc4bd7b61f0fa6fac90bcd42597a9f568637186acde3e41df`

```dockerfile
```

-	Layers:
	-	`sha256:58f44538882c04e4ea9ca3a42556c9041c37bd3ddc65e96d01c8732635052469`  
		Last Modified: Tue, 17 Feb 2026 21:40:24 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4684065ca0cb7b52011a60753158ac4b74eea963e389fec9ece538fa30885a2a`  
		Last Modified: Tue, 17 Feb 2026 21:40:24 GMT  
		Size: 36.9 KB (36927 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:a03abf572560fa626d59a8c15f18d024c3f6322d2856614c5a1322da8c55a8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159661710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79420a0c7e585afd83e58896e640eb45fb39925120ba6022bb259d2f30d5aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:19:18 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:19:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:19:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:19:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:19:38 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:19:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:19:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:19:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:19:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:19:38 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 21:19:38 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 21:20:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:20:00 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:20:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:20:00 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:20:00 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29be9ef133c6e983c557d50c5b495503572814157079ea17f0e0221cff92f26`  
		Last Modified: Tue, 17 Feb 2026 21:20:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa859a9257eca8ee404e28c80de84b52e3ce4486cfad483be32095081e1b225`  
		Last Modified: Tue, 17 Feb 2026 21:20:12 GMT  
		Size: 16.2 MB (16209326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e8ae56b9d44fc86b2104418ac4374ab19b2c795ffc1010ab347a294c7854a9`  
		Last Modified: Tue, 17 Feb 2026 21:20:12 GMT  
		Size: 1.2 MB (1232640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7324b906d4ca5d67e89ea7f199e14244a78471c3b807d3fa5999969c65531d`  
		Last Modified: Tue, 17 Feb 2026 21:20:13 GMT  
		Size: 45.0 MB (45037249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279517d7759516062cd3d50fd5960a58c6458d5db767dae26a4af7a525f4bcd1`  
		Last Modified: Tue, 17 Feb 2026 21:20:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5929456ccd47a6fd06e56c0a037f3984ee8f53b586008ec84e574cd6455070c`  
		Last Modified: Tue, 17 Feb 2026 21:20:15 GMT  
		Size: 73.2 MB (73245941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e4cf3f129d53b9ee509fc6ae31d83333417d25d34564e21e2e102c4ddf55b2`  
		Last Modified: Tue, 17 Feb 2026 21:20:14 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:9dffc17cb1e28e790853dc6ee515e3f7e317fa7d05b79a6787a60b36faab96c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed6fd945cdc29d542b561228b10cf93aefa3265b34a2bded68b9cfd5437fbf`

```dockerfile
```

-	Layers:
	-	`sha256:06065d3a7c3cbc85000283bb111db414469c16a894d40cbcb14b910eefa3dfa8`  
		Last Modified: Tue, 17 Feb 2026 21:20:12 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ad752a4bc4c0d862f68d28b610377c4029786693f9729a3c8eaaa44f04fe75`  
		Last Modified: Tue, 17 Feb 2026 21:20:12 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:e96c8f4df05b945242851f0cd5b56b838afc7c665a17b69a739c11c89ea7117d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167374785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93dafcd6e3d2c30eb70fa10a6b3092bc2d5b9c99d55291e54a444092410ca6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:39:35 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:39:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:39:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:39:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:39:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:39:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:39:51 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:39:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:39:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:39:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:39:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:39:51 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 21:39:51 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 21:40:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:40:08 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:40:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:40:08 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:40:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203f4fdb48a27d91dd0e21291cbd1a8d6991fbd7042b2bef3794e8ee0037bb77`  
		Last Modified: Tue, 17 Feb 2026 21:40:22 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b9b7e288bc328b59312e4cde541c465851a43cf85c3d3acab0b8fd66c739fd`  
		Last Modified: Tue, 17 Feb 2026 21:40:22 GMT  
		Size: 17.9 MB (17888391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30799a949e56db61e6f5b244e5fb34247809440b58575a3ff897c29e3f44eb`  
		Last Modified: Tue, 17 Feb 2026 21:40:22 GMT  
		Size: 1.2 MB (1220080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaf9c8388941deed313dcb7fe2539f4ce5901619fd69021897e25036610d20e`  
		Last Modified: Tue, 17 Feb 2026 21:40:23 GMT  
		Size: 46.9 MB (46910204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7765c69b5afd9d953f9d20ad0b5713ac3935a2b8c4b2dc02293aab3541c677f`  
		Last Modified: Tue, 17 Feb 2026 21:40:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3464cc1f344c73064b3fa17e6499b796df9e73b90c8503a7cca8d255d60265`  
		Last Modified: Tue, 17 Feb 2026 21:40:25 GMT  
		Size: 73.2 MB (73245827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fe129f1a5beccfb8d723540d6823da73c19d0dfaa6c42b29720262ff24ffd0`  
		Last Modified: Tue, 17 Feb 2026 21:40:24 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:181291467cc1baa7f998d77f729367114ea6eaa53e9424534841c2a0d0c42d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7460da71e37105e33927eae54d49b669c6504f1fec3cfe85bca0b9d8eb76759`

```dockerfile
```

-	Layers:
	-	`sha256:b6843c7557970a17ae5dbb4cb9a98ffeaaff98a47d2aab74ade75dcb9229446a`  
		Last Modified: Tue, 17 Feb 2026 21:40:22 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e75d77bf15398d6c68ccdc36868545e4a44196eba469161cae00ae0ba84d9fa0`  
		Last Modified: Tue, 17 Feb 2026 21:40:21 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:d74d40a6b8ad71ac97e922976993a3125328346428b2fb03393cf247fbeb02cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5b77f5f34a57433b507ada98f459abbe37ebebcde9233fb141b8ef6af062d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:51:37 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 05 Feb 2026 23:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 05 Feb 2026 23:52:32 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 23:52:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 23:52:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:52:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:52:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:52:35 GMT
RUN java --version # buildkit
# Thu, 05 Feb 2026 23:52:35 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 05 Feb 2026 23:52:35 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 05 Feb 2026 23:52:35 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:52:35 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 05 Feb 2026 23:52:35 GMT
ENV CASSANDRA_VERSION=5.0.6
# Thu, 05 Feb 2026 23:52:35 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Thu, 05 Feb 2026 23:53:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 05 Feb 2026 23:53:16 GMT
VOLUME [/var/lib/cassandra]
# Thu, 05 Feb 2026 23:53:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 23:53:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 23:53:17 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 05 Feb 2026 23:53:17 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29b164197e65b0a4a2aa03bc1271d3171b833c3006c6b2bc0b44b775362c22a`  
		Last Modified: Thu, 05 Feb 2026 23:53:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a8f25d37b6332ce8a7ccbfbaff9d8fc7a3e2762064b0b78018a895bc3e4fc`  
		Last Modified: Thu, 05 Feb 2026 23:53:56 GMT  
		Size: 19.5 MB (19493281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1a41f85e431f559f8e9329db43fd6352d439d7c8366241e5352c41990f3ce9`  
		Last Modified: Thu, 05 Feb 2026 23:53:55 GMT  
		Size: 1.2 MB (1225510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cf2c239e64061d9e139e6287943df1814a8c5a2ee4bcb1823a8a8dce49b015`  
		Last Modified: Thu, 05 Feb 2026 23:54:01 GMT  
		Size: 47.3 MB (47327570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1edde3573505e25593e7e49bee16454aaa005043982e359be9a1b660429df4`  
		Last Modified: Thu, 05 Feb 2026 23:53:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb4895f90b4a359ae8f0fae7ec775ee564af931e5d18845ddecf89599632fdf`  
		Last Modified: Thu, 05 Feb 2026 23:54:02 GMT  
		Size: 73.2 MB (73246045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf544aa6e16bd7c4b3e0c72a5a5c6f41bf36effe56bf0c9302fef0f6b51934b8`  
		Last Modified: Thu, 05 Feb 2026 23:53:59 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:7fc0a33baeae3fe3aab76351267dc5c05f69a314862e233abf2d3e3adcd1968f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fe7c2673d664702571eb9ba4605ebdc21894dd1dd390a6a959c05432116321`

```dockerfile
```

-	Layers:
	-	`sha256:4b82519224ac2e4d0feeb670116647bee5470d634282bfd08e66ca54719910c0`  
		Last Modified: Thu, 05 Feb 2026 23:53:59 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:572c24e678901ae0a68fb3eed249fbacc1bdcbb2bef9a2f9e635a568e6dfaca2`  
		Last Modified: Thu, 05 Feb 2026 23:53:59 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; s390x

```console
$ docker pull cassandra@sha256:321683107faab3524e56f733fea1b055daf955bf057b823f85ab8451edcc82e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163226842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6da10cb30206d8e94e37be49432b12e19a7c89395ed4912e0d2acda11401d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:58:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:58:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:58:54 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:58:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:58:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:57 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:58:57 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:58:57 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:58:57 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:57 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:58:57 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 21:58:57 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 21:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:59:30 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:59:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:59:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:59:30 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:59:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f9ae3065bc6c290d56238776df4e1bc230044143d46eb2094b3b3a69f4c93c`  
		Last Modified: Tue, 17 Feb 2026 22:00:15 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94985232a2c8b2f470ce12acf7cd7fa974247e3c07ef9504c84184a524fedb66`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 17.5 MB (17454693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def17a1b8e565fa7c3277c91f18ffa6d97613ebab22cc69e8ac2d9995b13bbec`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 1.2 MB (1240669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecf11198d84c73d3bb12ec4fcdc2185ea051baba5b2bceb6aa031a2073faca`  
		Last Modified: Tue, 17 Feb 2026 22:00:19 GMT  
		Size: 44.4 MB (44398466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e1cd4d6d74ba9151275bb4500293ed750b9a9dd0fce14293c868f36ab8818`  
		Last Modified: Tue, 17 Feb 2026 22:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4be9ae0e5972c1e80ed8e9e92e09b973b643763afea5512c4cf7d9f47ac298`  
		Last Modified: Tue, 17 Feb 2026 22:00:20 GMT  
		Size: 73.2 MB (73246166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ad90b4c4e3edbe9bd5f59866400613c145d39e14f05ad19dc51091a439dbfc`  
		Last Modified: Tue, 17 Feb 2026 22:00:19 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:12d5f686fda32641f57cd61faf1c36cfde801bce888ec258acceeef45ae20f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce71544bcf8c4654b310bce410fd8d986b0748f3cf160f9e4b25137abe930e2`

```dockerfile
```

-	Layers:
	-	`sha256:1a5d4497b0d724ca8b23db4be28e16364d1fdd5acb1017ec1f399d624927ec0b`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 3.3 MB (3302298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a4493f64e6e6017451c17bbe03b41e5e32c674aaf7cf014dbf955dc2a563a5a`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json
