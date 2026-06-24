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
