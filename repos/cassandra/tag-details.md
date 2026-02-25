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
$ docker pull cassandra@sha256:3b96901e62443e4c241952d0de88abea083b0fb98cdde4a5b52021c164cc95dd
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
$ docker pull cassandra@sha256:17dc669f7c9a1260816e8f908711d6c17deaed17742ae171416d1e3fb221b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ced33659ee23d14e1a0d5d957d9409047313c734d5bfc7983afdac8be3fe9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:08 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 19:51:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:43 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:43 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c451d7bd1bdd623e0e08ab6dff5e016bcbe8f36861aa9a030c62f323c8a0e0`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0924908ceb4159ebfa239a90b4c3b237f672fc7c5276a42cba6d52c5b1b40ed4`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 18.1 MB (18149822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284250caa4b9682a982bca8ca932f21122c0f5e4f76240aad7e58194aee8a2e`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 1.3 MB (1266583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2567053f78671b186f9dad73efbdf200b173a1bd2aec9d3f3c85b0f4af645`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 47.3 MB (47294889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4787c302506d4d556de5d633ad1e4ee205c26d30f37bdb299c2b5a21569fceb6`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb904ebfcf32042b33e0386e9bb0fc6d1dee70aa787df30eb3e2c17dfbac68a`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 52.9 MB (52914354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34cd45cc2b16685214894fda1ff13a9a39acc2d039aa4b274529dc30997118`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:1efc4518fc2df4d6816e8c3af0bfc89d18ced91ba57fafec2653242efec380fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea705d0c2b3dadf5eedd15c6017ae0ae6236dc0e07aa50c59ad1e6c75c4c858`

```dockerfile
```

-	Layers:
	-	`sha256:8ab1755e0b922fac453c7d7e8c3f02a04fc226e3209b9fc4fed00da9d05255a2`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c20d9b6468f2d2f9818b33012a128104a02580fbf1ded5fe254913e24ca113e`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:6c37b87490cb8d3573e30ee104f15f342abede27d2b2a01a07294bf55ee19052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1ec595db034761a62a17961e5ab30ce4c7725a026134405006132ce8b5790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:32 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 21:10:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:12 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:12 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc7063224ccd2d852c86ca2d3e9ba35718da1ff1487c0b99b3a32645e5c9e10`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13e196ef36b54bcb66d87ad4d4de07f63e79c2d522e3d213d84e89fbb279a9`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 16.2 MB (16209300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83637cdc95e7bb122906eee09ba9cd9eefd9c37b055ae9628eb8f7aaab276b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.2 MB (1232642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824a46883e448fd7a4022dbdd5340aaea423cbb18e302c7bfe47ef7482731beb`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 45.4 MB (45413860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbe148ec44193032e42de9b2b7334ae48dfc5a582b771f16b4f3a698c65dbe`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d7c1eedfe6c0fc1ca4aa0af78ebf527002fe812e9f4e28da7765d566cb79e`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 52.9 MB (52914505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6f221d4f32c84daffbc7f2df93d48ceb0a17e2544f30220d4f4092c43ec45`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4479cd4e3a0c13d73f1bcf5087adb3a2e96da176ba6e47a9d7cf323a7c61d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95514322c075a261e447ed962ab70d011cf7052cf35faf70c0e350acbf19c76`

```dockerfile
```

-	Layers:
	-	`sha256:138f65c798315d52ad9b7e22fd65208ea49dda746e2183ddd836bf26dd45b53b`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da383a9b628463bb5ae9005d4a307016fe050bcf71971021281f8f4b8d125db`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:e8555f52b54a31acba9f0bf10d6ced1426b09caa1c2a1a3642b28c7a2d911ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3906bfa310c774f020a5e76fed9c9e3c15e7205c183e160b641bfbc61e7891dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:31 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:08 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef79d776c2b52fe440faa84c52e71c6230a23a4ba30224c87cb1420baad085d`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c948817d15e429f907513f5421702f5049800cbd80d4fef6bfe47432ef0f7`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 17.9 MB (17888673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41730693b0a73838483aa3515f3ecf51ea817cda056d457bf38ae6ce1697bc68`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac89d9c702f85a7acb7578d5d6596d29a397e8328160b2b070bb461ebbb10d7`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 45.6 MB (45617132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4a6dd9827dac2a273a204977dc2366aec5e476c6b699155b5a5688dd9236e`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec0f2a506a5054efa6a0b65ba627944d264981867a580310084f82ae36dc0b`  
		Last Modified: Tue, 24 Feb 2026 20:02:24 GMT  
		Size: 52.9 MB (52914436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79bec185a2d3ced951cc759b4de25d2d5d719fe39d17f2e822ce3196426f92c`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:e62270f4072338ce6e88ec443891c88c11dd7a9fa6d988de617be08ef6e2bf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6093a2ab0ed44333db3ae568d889ed569187324385152acd5709fa9c41dccd4`

```dockerfile
```

-	Layers:
	-	`sha256:5dc81ead25e1d00e1b2b87619ecb927b8bf1e672120498ea42248219ae90f681`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d6b03010f966e94de1d7c6f1f0cf14b0907068b7a6bb5dd4b16ec8499b2d3`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; ppc64le

```console
$ docker pull cassandra@sha256:3c37654ffdc9ebfc42c9fd5b49c2e38f07d72b5e330843277a491f2511ea4d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148446597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e5b5640a3df560846af52408926e9b7413446a7dd346fc5c7a71a50a48798`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 23:25:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:05 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:07 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad00f890abc48b985889dd9a231206a616f5cf1142fdc34cf379e4e1919978`  
		Last Modified: Tue, 17 Feb 2026 23:25:37 GMT  
		Size: 52.9 MB (52914681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a66f595378cad72ae44f0d032e2027db2941617a80748f9dfa3017a603c6f`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:9df10ae3e45f48d92eb1e0ee7f99fa3033ee6fa616e3ce7bbe62c9a023e59be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62759e1f57179d440733fe70cdfd9f3f4c730e95ff0804d1be574ec2170bd61`

```dockerfile
```

-	Layers:
	-	`sha256:639da1b568fbcf17866e05bd424e64b49b5f82aa14419a34d3ab7651b8129592`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d55c1cb6b8039832a3af27eaebe0fd3ba0d90a034a4e5cead1099ec2901a54`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 36.4 KB (36399 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4` - linux; s390x

```console
$ docker pull cassandra@sha256:643c323fc6f76a60e642fb41f61ca911ad3bb425e1245f888f0ceb5bbe9d4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139800049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f93ff6d0cb01ca2f9fb0f6f579f1f8110dde06ddb5a9ca51ebc4e63001d014`
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
# Tue, 17 Feb 2026 21:58:58 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 21:59:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:59:34 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:59:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:59:35 GMT
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
	-	`sha256:0bd18c0204322ef5bbba2d083e811e3f75cf6f32c94cf27dc4de277cf388ae03`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 41.3 MB (41303100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e1cd4d6d74ba9151275bb4500293ed750b9a9dd0fce14293c868f36ab8818`  
		Last Modified: Tue, 17 Feb 2026 22:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c8d780a09144af0f6ac9227774c238d327d8208201fff0a443fd4b1b3d0ba`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 52.9 MB (52914739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a40fd716f56a8144e5164fcd4ec85fe9cccc266e207b3ecf321123b950256`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4` - unknown; unknown

```console
$ docker pull cassandra@sha256:195cb6b7b00c4cd94dafb56e962d11a3eea1a111465e6b66009c47536467c495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63c07a9788c1a3a386aff2204908f77414d3c09ccb386d30cfe4f1e843fe2c4`

```dockerfile
```

-	Layers:
	-	`sha256:15101ce78632fc025fdee03d4d0d7afb71594a1cc9c686ffaf90e9dd2c0af682`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92262922929100823e3cff817bf33a620e15b2781dbe40d738056ec8a7a46027`  
		Last Modified: Tue, 17 Feb 2026 22:00:15 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4-bookworm`

```console
$ docker pull cassandra@sha256:3b96901e62443e4c241952d0de88abea083b0fb98cdde4a5b52021c164cc95dd
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
$ docker pull cassandra@sha256:17dc669f7c9a1260816e8f908711d6c17deaed17742ae171416d1e3fb221b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ced33659ee23d14e1a0d5d957d9409047313c734d5bfc7983afdac8be3fe9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:08 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 19:51:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:43 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:43 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c451d7bd1bdd623e0e08ab6dff5e016bcbe8f36861aa9a030c62f323c8a0e0`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0924908ceb4159ebfa239a90b4c3b237f672fc7c5276a42cba6d52c5b1b40ed4`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 18.1 MB (18149822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284250caa4b9682a982bca8ca932f21122c0f5e4f76240aad7e58194aee8a2e`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 1.3 MB (1266583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2567053f78671b186f9dad73efbdf200b173a1bd2aec9d3f3c85b0f4af645`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 47.3 MB (47294889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4787c302506d4d556de5d633ad1e4ee205c26d30f37bdb299c2b5a21569fceb6`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb904ebfcf32042b33e0386e9bb0fc6d1dee70aa787df30eb3e2c17dfbac68a`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 52.9 MB (52914354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34cd45cc2b16685214894fda1ff13a9a39acc2d039aa4b274529dc30997118`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:1efc4518fc2df4d6816e8c3af0bfc89d18ced91ba57fafec2653242efec380fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea705d0c2b3dadf5eedd15c6017ae0ae6236dc0e07aa50c59ad1e6c75c4c858`

```dockerfile
```

-	Layers:
	-	`sha256:8ab1755e0b922fac453c7d7e8c3f02a04fc226e3209b9fc4fed00da9d05255a2`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c20d9b6468f2d2f9818b33012a128104a02580fbf1ded5fe254913e24ca113e`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:6c37b87490cb8d3573e30ee104f15f342abede27d2b2a01a07294bf55ee19052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1ec595db034761a62a17961e5ab30ce4c7725a026134405006132ce8b5790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:32 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 21:10:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:12 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:12 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc7063224ccd2d852c86ca2d3e9ba35718da1ff1487c0b99b3a32645e5c9e10`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13e196ef36b54bcb66d87ad4d4de07f63e79c2d522e3d213d84e89fbb279a9`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 16.2 MB (16209300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83637cdc95e7bb122906eee09ba9cd9eefd9c37b055ae9628eb8f7aaab276b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.2 MB (1232642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824a46883e448fd7a4022dbdd5340aaea423cbb18e302c7bfe47ef7482731beb`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 45.4 MB (45413860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbe148ec44193032e42de9b2b7334ae48dfc5a582b771f16b4f3a698c65dbe`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d7c1eedfe6c0fc1ca4aa0af78ebf527002fe812e9f4e28da7765d566cb79e`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 52.9 MB (52914505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6f221d4f32c84daffbc7f2df93d48ceb0a17e2544f30220d4f4092c43ec45`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4479cd4e3a0c13d73f1bcf5087adb3a2e96da176ba6e47a9d7cf323a7c61d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95514322c075a261e447ed962ab70d011cf7052cf35faf70c0e350acbf19c76`

```dockerfile
```

-	Layers:
	-	`sha256:138f65c798315d52ad9b7e22fd65208ea49dda746e2183ddd836bf26dd45b53b`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da383a9b628463bb5ae9005d4a307016fe050bcf71971021281f8f4b8d125db`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:e8555f52b54a31acba9f0bf10d6ced1426b09caa1c2a1a3642b28c7a2d911ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3906bfa310c774f020a5e76fed9c9e3c15e7205c183e160b641bfbc61e7891dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:31 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:08 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef79d776c2b52fe440faa84c52e71c6230a23a4ba30224c87cb1420baad085d`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c948817d15e429f907513f5421702f5049800cbd80d4fef6bfe47432ef0f7`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 17.9 MB (17888673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41730693b0a73838483aa3515f3ecf51ea817cda056d457bf38ae6ce1697bc68`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac89d9c702f85a7acb7578d5d6596d29a397e8328160b2b070bb461ebbb10d7`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 45.6 MB (45617132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4a6dd9827dac2a273a204977dc2366aec5e476c6b699155b5a5688dd9236e`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec0f2a506a5054efa6a0b65ba627944d264981867a580310084f82ae36dc0b`  
		Last Modified: Tue, 24 Feb 2026 20:02:24 GMT  
		Size: 52.9 MB (52914436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79bec185a2d3ced951cc759b4de25d2d5d719fe39d17f2e822ce3196426f92c`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:e62270f4072338ce6e88ec443891c88c11dd7a9fa6d988de617be08ef6e2bf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6093a2ab0ed44333db3ae568d889ed569187324385152acd5709fa9c41dccd4`

```dockerfile
```

-	Layers:
	-	`sha256:5dc81ead25e1d00e1b2b87619ecb927b8bf1e672120498ea42248219ae90f681`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d6b03010f966e94de1d7c6f1f0cf14b0907068b7a6bb5dd4b16ec8499b2d3`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:3c37654ffdc9ebfc42c9fd5b49c2e38f07d72b5e330843277a491f2511ea4d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148446597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e5b5640a3df560846af52408926e9b7413446a7dd346fc5c7a71a50a48798`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 23:25:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:05 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:07 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad00f890abc48b985889dd9a231206a616f5cf1142fdc34cf379e4e1919978`  
		Last Modified: Tue, 17 Feb 2026 23:25:37 GMT  
		Size: 52.9 MB (52914681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a66f595378cad72ae44f0d032e2027db2941617a80748f9dfa3017a603c6f`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:9df10ae3e45f48d92eb1e0ee7f99fa3033ee6fa616e3ce7bbe62c9a023e59be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62759e1f57179d440733fe70cdfd9f3f4c730e95ff0804d1be574ec2170bd61`

```dockerfile
```

-	Layers:
	-	`sha256:639da1b568fbcf17866e05bd424e64b49b5f82aa14419a34d3ab7651b8129592`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d55c1cb6b8039832a3af27eaebe0fd3ba0d90a034a4e5cead1099ec2901a54`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 36.4 KB (36399 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:643c323fc6f76a60e642fb41f61ca911ad3bb425e1245f888f0ceb5bbe9d4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139800049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f93ff6d0cb01ca2f9fb0f6f579f1f8110dde06ddb5a9ca51ebc4e63001d014`
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
# Tue, 17 Feb 2026 21:58:58 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 21:59:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:59:34 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:59:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:59:35 GMT
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
	-	`sha256:0bd18c0204322ef5bbba2d083e811e3f75cf6f32c94cf27dc4de277cf388ae03`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 41.3 MB (41303100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e1cd4d6d74ba9151275bb4500293ed750b9a9dd0fce14293c868f36ab8818`  
		Last Modified: Tue, 17 Feb 2026 22:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c8d780a09144af0f6ac9227774c238d327d8208201fff0a443fd4b1b3d0ba`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 52.9 MB (52914739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a40fd716f56a8144e5164fcd4ec85fe9cccc266e207b3ecf321123b950256`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:195cb6b7b00c4cd94dafb56e962d11a3eea1a111465e6b66009c47536467c495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63c07a9788c1a3a386aff2204908f77414d3c09ccb386d30cfe4f1e843fe2c4`

```dockerfile
```

-	Layers:
	-	`sha256:15101ce78632fc025fdee03d4d0d7afb71594a1cc9c686ffaf90e9dd2c0af682`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92262922929100823e3cff817bf33a620e15b2781dbe40d738056ec8a7a46027`  
		Last Modified: Tue, 17 Feb 2026 22:00:15 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0`

```console
$ docker pull cassandra@sha256:d4b062feb91ccbf1a16d8f31eda79c01d60ed143db970940cf0336b5d5d2654e
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
$ docker pull cassandra@sha256:5acfc1373a147771ac29ae59cc830c216b02afe01a9f058c22852eff23db344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be597501a681e5b47d92582a26ace6aaa6ac4835a977c1424b25ec50c2dc046d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 19:51:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:56 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:56 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa19148b1e5c95f0cecad947e969b1d8e8f6078ff46ad459ec0ba29898acc6`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb30cdce8ec678fade8303f156fb76735c6833c96b7a37863616268471bbe00`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 18.2 MB (18150147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de1e26862336f65aece4232489672fb873f0760c928f3ef7332a0a400ef6f3`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.3 MB (1266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45aa6f04cbee08fd5af7dea016dfd56ab4a4405614ad52d070b799d6e9481fa`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 47.3 MB (47294888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ebcf0ebc5c8fc0629715b7aae05f7fdc0782f82924fd085dc888386edd2905`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed444c976433cb5bad6ed75d6503184929f9dc8edd2fd75e94d355e00e1598c`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69945dd4ab329cf57c039a8bab01c57a90b57809f591497b530b4d414164b2`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:ae244994c3bf5346d85e4a839cf9ebafd0a7e233bd188b4b2fcafbe924a8f19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59885fa4b5cb256e594c6dd4f582bf97cf63e8b6a708c2f9c0020ddae9cc3e19`

```dockerfile
```

-	Layers:
	-	`sha256:5382812a7a4960c8f412359b7d0b874507dd701c4137698010c324d0a356db6e`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e342759cc5713ccf82d25aa43254e288907ce83418e9be0477f85c7c779169dd`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 35.7 KB (35718 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:12d9994dfdd7a47dd4c5387f64906051b8618c718858528c601fbb6e2ed7a720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138650079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3126dbc6f15b6521440bcf14eb5b29fdc3cf661eab9f4923d0e1e1122fa5fa8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:10:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:10:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:21 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:21 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a2ecc644aafa57ffb898ac2eedc38632bc38d42153e6f3b0af8a2aad70f31`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9923475f87c012d222361d32b3f217db6188fdeb8f3319a1b2a5a6ae3d417ff`  
		Last Modified: Tue, 24 Feb 2026 21:10:34 GMT  
		Size: 16.2 MB (16209321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b74e81c3d06a0e7ab4ad398c3a334f944c7cfe897d08a7343688233349225`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.2 MB (1232656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f7f4d60ba5590fb09668226c04f7afaeb759c27f52bc4d45aa8610004481c9`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 45.4 MB (45413842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918bc4a2db2972a07bd1d7f666f572e2edc6381c3ed0ebf2bef69e503ed5a22d`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3150c139e9a82e5752370652b2b076430a7ee2a13938dc4865dd3be238d5b4f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:36 GMT  
		Size: 51.9 MB (51850404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311f408c80e358d10a47e187941a8bc49c9cbc29a79390da8ab996f24fc35003`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:5fadb5681997e02662ae8053f74cd529dc69b2f2cd6f843a3c06b960aefcc1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47d986e9d110e786e67ba7c762c28b8bb68764bdfac6241fbbd298a0529a1c3`

```dockerfile
```

-	Layers:
	-	`sha256:aba92ea8202c851f5df74aa06d5c0d30c5d983c27b371129586b958d1acad9b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229b6829356babbbd8e08e8d795077636d4dadc9b34cd97c9ec1b096b9b1b374`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:43326ba726f615946af911fa218a19ccceb5d72544acb2f8ba8993af2006480b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81f81c8f608571e1332534e466cc4bce6a4d44be6237e18d6ab838e2c7bb005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:41 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 20:02:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776c6fcbca943e250cb7717026819146c2c3986621ea9125ca3523806734169`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15732dabcc36d4b5fd3115040b7c52d318009b923315b1b83b7f9e1cae4bdfcf`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 17.9 MB (17888534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c762f98953f3f3959fd5bc5d692820f4b3d73714419eb95f5a9a27f94d2f2`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.2 MB (1220132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cfad825ffb6e2adf83e44ffc31aa7f14ea00719aa6c677320e75df731692d`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 45.6 MB (45617125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f9f4004a5e1d681b965056eea11359ca257c4d32115dad9c6cd1be3f95879b`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f4e3fe70ce6ac131d0aa3f72ca5aa33da8d18906669501cbc0e14949f354c`  
		Last Modified: Tue, 24 Feb 2026 20:02:31 GMT  
		Size: 51.9 MB (51850347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bed2a99751bef806f11d9f7a4a7e87bb14ca14a1f0eb78349a532f982d4a40`  
		Last Modified: Tue, 24 Feb 2026 20:02:30 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:a07d210d5736829a5952c80dfdbb11939f36e828ef75a09b4507fe531a0231e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c268a290083c9f261a6e404b76edf8ac6ff1385c83d25f3bfcc3b9f12cd2f9a2`

```dockerfile
```

-	Layers:
	-	`sha256:2d6792d7a9be992bb0210c30bf69dbe47cf0778159c4b24625479cfb19687d59`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dba16b3be229d60309c9e0e64d4458b897dc5f886f85822d6688576cfb4c4c9`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 35.9 KB (35908 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:f549ce9e15bc974835f173aa2cc3c19d6f044b22947b0a954a9b0899608e6d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147382447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da15b83fd3eb3220c8f582c198dd0a50bf2831da718bd7e2809718887e1e`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 23:25:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:57 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:57 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60bf54c7c2f216842406367a2ab7f8c5f0891bb3592c811701c0947cc1a34e1`  
		Last Modified: Tue, 17 Feb 2026 23:26:17 GMT  
		Size: 51.9 MB (51850532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d9fbda36b1983477dd9702a7d58a21086e387721dc688bb2d54631ff4d1ab`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:5731200717490f3267f8b7ef2a72f2eb1f1ceb5f3b392dd70c5314a185b5ad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279f03ee79381858d2bb135ff991e5aaf0aa8ffaf744a753919912ddb09333c`

```dockerfile
```

-	Layers:
	-	`sha256:2282099bc0f31d58ef838ab6a17c0609606bfe892cc5ac4f1a5d0b4c899cfe4f`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f848c0809977295036c07c2b1f7e4825a956355a0b6fdbdaf1b49fbf77e902`  
		Last Modified: Tue, 17 Feb 2026 23:26:15 GMT  
		Size: 35.8 KB (35781 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0` - linux; s390x

```console
$ docker pull cassandra@sha256:8ad326fa7497c0118c03ba6624917718382996ac6bfcd0fc83059501b7f3edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138736174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3add3a4d7738e85685b5c08976da7e2ab6dbfe08a051f72fed26029d5ea8af0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:58:47 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:59:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 22:00:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 22:00:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:00:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 22:00:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c1d613eb90a63326ac47071d5fd3825317137acb4a94756ce9a04d2388496`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d84ab4976a7aa1013ab95c7c6cc3f6b9a11fa592233e14569df223ff1583b5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 17.5 MB (17454908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ae11a27e935ea0df1d1a506e31ebefa8cf04807ac3f7c30b95bf384852cf5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.2 MB (1240737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9886db6e61a662ba25a7faaef3af2630ba7f28983462b969ab6514c6d01e805`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 41.3 MB (41303109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c72d5ae6113f4c0b31330cdd50c0faa6bee4df7a036dd233a062a41d7236d7`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbd9b4a3a8eb40d1b01a1aae186bb9b7af51bd3a4b114fd3e3b9c9e2cd283e`  
		Last Modified: Tue, 17 Feb 2026 22:01:15 GMT  
		Size: 51.9 MB (51850573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387db55b22c8771f280c74d5cd2a4154a5b4dc3df08a7dee065ebd35f874574b`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:c8b6521ff9e158467284b2ad39208efc2f68405858b2a24df998f73d6a18233a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58caa7320ab4172c7d6d49e7adb4634a25c8a4d3b3db496c997a2d97d1b3007`

```dockerfile
```

-	Layers:
	-	`sha256:6040450fec81cbf0a29d5b821ec2dc6bd83a0021e69e2b307fc9808873f4c54a`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9c266e2a2da75cb7a6a16db61513d92825c6efe5aebb21906a6e4427b4865f`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0-bookworm`

```console
$ docker pull cassandra@sha256:d4b062feb91ccbf1a16d8f31eda79c01d60ed143db970940cf0336b5d5d2654e
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
$ docker pull cassandra@sha256:5acfc1373a147771ac29ae59cc830c216b02afe01a9f058c22852eff23db344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be597501a681e5b47d92582a26ace6aaa6ac4835a977c1424b25ec50c2dc046d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 19:51:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:56 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:56 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa19148b1e5c95f0cecad947e969b1d8e8f6078ff46ad459ec0ba29898acc6`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb30cdce8ec678fade8303f156fb76735c6833c96b7a37863616268471bbe00`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 18.2 MB (18150147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de1e26862336f65aece4232489672fb873f0760c928f3ef7332a0a400ef6f3`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.3 MB (1266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45aa6f04cbee08fd5af7dea016dfd56ab4a4405614ad52d070b799d6e9481fa`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 47.3 MB (47294888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ebcf0ebc5c8fc0629715b7aae05f7fdc0782f82924fd085dc888386edd2905`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed444c976433cb5bad6ed75d6503184929f9dc8edd2fd75e94d355e00e1598c`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69945dd4ab329cf57c039a8bab01c57a90b57809f591497b530b4d414164b2`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:ae244994c3bf5346d85e4a839cf9ebafd0a7e233bd188b4b2fcafbe924a8f19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59885fa4b5cb256e594c6dd4f582bf97cf63e8b6a708c2f9c0020ddae9cc3e19`

```dockerfile
```

-	Layers:
	-	`sha256:5382812a7a4960c8f412359b7d0b874507dd701c4137698010c324d0a356db6e`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e342759cc5713ccf82d25aa43254e288907ce83418e9be0477f85c7c779169dd`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 35.7 KB (35718 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:12d9994dfdd7a47dd4c5387f64906051b8618c718858528c601fbb6e2ed7a720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138650079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3126dbc6f15b6521440bcf14eb5b29fdc3cf661eab9f4923d0e1e1122fa5fa8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:10:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:10:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:21 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:21 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a2ecc644aafa57ffb898ac2eedc38632bc38d42153e6f3b0af8a2aad70f31`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9923475f87c012d222361d32b3f217db6188fdeb8f3319a1b2a5a6ae3d417ff`  
		Last Modified: Tue, 24 Feb 2026 21:10:34 GMT  
		Size: 16.2 MB (16209321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b74e81c3d06a0e7ab4ad398c3a334f944c7cfe897d08a7343688233349225`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.2 MB (1232656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f7f4d60ba5590fb09668226c04f7afaeb759c27f52bc4d45aa8610004481c9`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 45.4 MB (45413842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918bc4a2db2972a07bd1d7f666f572e2edc6381c3ed0ebf2bef69e503ed5a22d`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3150c139e9a82e5752370652b2b076430a7ee2a13938dc4865dd3be238d5b4f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:36 GMT  
		Size: 51.9 MB (51850404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311f408c80e358d10a47e187941a8bc49c9cbc29a79390da8ab996f24fc35003`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:5fadb5681997e02662ae8053f74cd529dc69b2f2cd6f843a3c06b960aefcc1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47d986e9d110e786e67ba7c762c28b8bb68764bdfac6241fbbd298a0529a1c3`

```dockerfile
```

-	Layers:
	-	`sha256:aba92ea8202c851f5df74aa06d5c0d30c5d983c27b371129586b958d1acad9b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229b6829356babbbd8e08e8d795077636d4dadc9b34cd97c9ec1b096b9b1b374`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:43326ba726f615946af911fa218a19ccceb5d72544acb2f8ba8993af2006480b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81f81c8f608571e1332534e466cc4bce6a4d44be6237e18d6ab838e2c7bb005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:41 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 20:02:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776c6fcbca943e250cb7717026819146c2c3986621ea9125ca3523806734169`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15732dabcc36d4b5fd3115040b7c52d318009b923315b1b83b7f9e1cae4bdfcf`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 17.9 MB (17888534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c762f98953f3f3959fd5bc5d692820f4b3d73714419eb95f5a9a27f94d2f2`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.2 MB (1220132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cfad825ffb6e2adf83e44ffc31aa7f14ea00719aa6c677320e75df731692d`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 45.6 MB (45617125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f9f4004a5e1d681b965056eea11359ca257c4d32115dad9c6cd1be3f95879b`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f4e3fe70ce6ac131d0aa3f72ca5aa33da8d18906669501cbc0e14949f354c`  
		Last Modified: Tue, 24 Feb 2026 20:02:31 GMT  
		Size: 51.9 MB (51850347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bed2a99751bef806f11d9f7a4a7e87bb14ca14a1f0eb78349a532f982d4a40`  
		Last Modified: Tue, 24 Feb 2026 20:02:30 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a07d210d5736829a5952c80dfdbb11939f36e828ef75a09b4507fe531a0231e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c268a290083c9f261a6e404b76edf8ac6ff1385c83d25f3bfcc3b9f12cd2f9a2`

```dockerfile
```

-	Layers:
	-	`sha256:2d6792d7a9be992bb0210c30bf69dbe47cf0778159c4b24625479cfb19687d59`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dba16b3be229d60309c9e0e64d4458b897dc5f886f85822d6688576cfb4c4c9`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 35.9 KB (35908 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:f549ce9e15bc974835f173aa2cc3c19d6f044b22947b0a954a9b0899608e6d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147382447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da15b83fd3eb3220c8f582c198dd0a50bf2831da718bd7e2809718887e1e`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 23:25:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:57 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:57 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60bf54c7c2f216842406367a2ab7f8c5f0891bb3592c811701c0947cc1a34e1`  
		Last Modified: Tue, 17 Feb 2026 23:26:17 GMT  
		Size: 51.9 MB (51850532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d9fbda36b1983477dd9702a7d58a21086e387721dc688bb2d54631ff4d1ab`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:5731200717490f3267f8b7ef2a72f2eb1f1ceb5f3b392dd70c5314a185b5ad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279f03ee79381858d2bb135ff991e5aaf0aa8ffaf744a753919912ddb09333c`

```dockerfile
```

-	Layers:
	-	`sha256:2282099bc0f31d58ef838ab6a17c0609606bfe892cc5ac4f1a5d0b4c899cfe4f`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f848c0809977295036c07c2b1f7e4825a956355a0b6fdbdaf1b49fbf77e902`  
		Last Modified: Tue, 17 Feb 2026 23:26:15 GMT  
		Size: 35.8 KB (35781 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:8ad326fa7497c0118c03ba6624917718382996ac6bfcd0fc83059501b7f3edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138736174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3add3a4d7738e85685b5c08976da7e2ab6dbfe08a051f72fed26029d5ea8af0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:58:47 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:59:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 22:00:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 22:00:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:00:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 22:00:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c1d613eb90a63326ac47071d5fd3825317137acb4a94756ce9a04d2388496`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d84ab4976a7aa1013ab95c7c6cc3f6b9a11fa592233e14569df223ff1583b5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 17.5 MB (17454908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ae11a27e935ea0df1d1a506e31ebefa8cf04807ac3f7c30b95bf384852cf5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.2 MB (1240737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9886db6e61a662ba25a7faaef3af2630ba7f28983462b969ab6514c6d01e805`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 41.3 MB (41303109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c72d5ae6113f4c0b31330cdd50c0faa6bee4df7a036dd233a062a41d7236d7`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbd9b4a3a8eb40d1b01a1aae186bb9b7af51bd3a4b114fd3e3b9c9e2cd283e`  
		Last Modified: Tue, 17 Feb 2026 22:01:15 GMT  
		Size: 51.9 MB (51850573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387db55b22c8771f280c74d5cd2a4154a5b4dc3df08a7dee065ebd35f874574b`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:c8b6521ff9e158467284b2ad39208efc2f68405858b2a24df998f73d6a18233a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58caa7320ab4172c7d6d49e7adb4634a25c8a4d3b3db496c997a2d97d1b3007`

```dockerfile
```

-	Layers:
	-	`sha256:6040450fec81cbf0a29d5b821ec2dc6bd83a0021e69e2b307fc9808873f4c54a`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9c266e2a2da75cb7a6a16db61513d92825c6efe5aebb21906a6e4427b4865f`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0.19`

```console
$ docker pull cassandra@sha256:d4b062feb91ccbf1a16d8f31eda79c01d60ed143db970940cf0336b5d5d2654e
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
$ docker pull cassandra@sha256:5acfc1373a147771ac29ae59cc830c216b02afe01a9f058c22852eff23db344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be597501a681e5b47d92582a26ace6aaa6ac4835a977c1424b25ec50c2dc046d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 19:51:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:56 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:56 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa19148b1e5c95f0cecad947e969b1d8e8f6078ff46ad459ec0ba29898acc6`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb30cdce8ec678fade8303f156fb76735c6833c96b7a37863616268471bbe00`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 18.2 MB (18150147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de1e26862336f65aece4232489672fb873f0760c928f3ef7332a0a400ef6f3`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.3 MB (1266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45aa6f04cbee08fd5af7dea016dfd56ab4a4405614ad52d070b799d6e9481fa`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 47.3 MB (47294888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ebcf0ebc5c8fc0629715b7aae05f7fdc0782f82924fd085dc888386edd2905`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed444c976433cb5bad6ed75d6503184929f9dc8edd2fd75e94d355e00e1598c`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69945dd4ab329cf57c039a8bab01c57a90b57809f591497b530b4d414164b2`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:ae244994c3bf5346d85e4a839cf9ebafd0a7e233bd188b4b2fcafbe924a8f19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59885fa4b5cb256e594c6dd4f582bf97cf63e8b6a708c2f9c0020ddae9cc3e19`

```dockerfile
```

-	Layers:
	-	`sha256:5382812a7a4960c8f412359b7d0b874507dd701c4137698010c324d0a356db6e`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e342759cc5713ccf82d25aa43254e288907ce83418e9be0477f85c7c779169dd`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 35.7 KB (35718 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:12d9994dfdd7a47dd4c5387f64906051b8618c718858528c601fbb6e2ed7a720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138650079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3126dbc6f15b6521440bcf14eb5b29fdc3cf661eab9f4923d0e1e1122fa5fa8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:10:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:10:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:21 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:21 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a2ecc644aafa57ffb898ac2eedc38632bc38d42153e6f3b0af8a2aad70f31`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9923475f87c012d222361d32b3f217db6188fdeb8f3319a1b2a5a6ae3d417ff`  
		Last Modified: Tue, 24 Feb 2026 21:10:34 GMT  
		Size: 16.2 MB (16209321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b74e81c3d06a0e7ab4ad398c3a334f944c7cfe897d08a7343688233349225`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.2 MB (1232656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f7f4d60ba5590fb09668226c04f7afaeb759c27f52bc4d45aa8610004481c9`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 45.4 MB (45413842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918bc4a2db2972a07bd1d7f666f572e2edc6381c3ed0ebf2bef69e503ed5a22d`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3150c139e9a82e5752370652b2b076430a7ee2a13938dc4865dd3be238d5b4f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:36 GMT  
		Size: 51.9 MB (51850404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311f408c80e358d10a47e187941a8bc49c9cbc29a79390da8ab996f24fc35003`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:5fadb5681997e02662ae8053f74cd529dc69b2f2cd6f843a3c06b960aefcc1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47d986e9d110e786e67ba7c762c28b8bb68764bdfac6241fbbd298a0529a1c3`

```dockerfile
```

-	Layers:
	-	`sha256:aba92ea8202c851f5df74aa06d5c0d30c5d983c27b371129586b958d1acad9b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229b6829356babbbd8e08e8d795077636d4dadc9b34cd97c9ec1b096b9b1b374`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:43326ba726f615946af911fa218a19ccceb5d72544acb2f8ba8993af2006480b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81f81c8f608571e1332534e466cc4bce6a4d44be6237e18d6ab838e2c7bb005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:41 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 20:02:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776c6fcbca943e250cb7717026819146c2c3986621ea9125ca3523806734169`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15732dabcc36d4b5fd3115040b7c52d318009b923315b1b83b7f9e1cae4bdfcf`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 17.9 MB (17888534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c762f98953f3f3959fd5bc5d692820f4b3d73714419eb95f5a9a27f94d2f2`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.2 MB (1220132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cfad825ffb6e2adf83e44ffc31aa7f14ea00719aa6c677320e75df731692d`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 45.6 MB (45617125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f9f4004a5e1d681b965056eea11359ca257c4d32115dad9c6cd1be3f95879b`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f4e3fe70ce6ac131d0aa3f72ca5aa33da8d18906669501cbc0e14949f354c`  
		Last Modified: Tue, 24 Feb 2026 20:02:31 GMT  
		Size: 51.9 MB (51850347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bed2a99751bef806f11d9f7a4a7e87bb14ca14a1f0eb78349a532f982d4a40`  
		Last Modified: Tue, 24 Feb 2026 20:02:30 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:a07d210d5736829a5952c80dfdbb11939f36e828ef75a09b4507fe531a0231e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c268a290083c9f261a6e404b76edf8ac6ff1385c83d25f3bfcc3b9f12cd2f9a2`

```dockerfile
```

-	Layers:
	-	`sha256:2d6792d7a9be992bb0210c30bf69dbe47cf0778159c4b24625479cfb19687d59`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dba16b3be229d60309c9e0e64d4458b897dc5f886f85822d6688576cfb4c4c9`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 35.9 KB (35908 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; ppc64le

```console
$ docker pull cassandra@sha256:f549ce9e15bc974835f173aa2cc3c19d6f044b22947b0a954a9b0899608e6d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147382447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da15b83fd3eb3220c8f582c198dd0a50bf2831da718bd7e2809718887e1e`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 23:25:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:57 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:57 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60bf54c7c2f216842406367a2ab7f8c5f0891bb3592c811701c0947cc1a34e1`  
		Last Modified: Tue, 17 Feb 2026 23:26:17 GMT  
		Size: 51.9 MB (51850532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d9fbda36b1983477dd9702a7d58a21086e387721dc688bb2d54631ff4d1ab`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:5731200717490f3267f8b7ef2a72f2eb1f1ceb5f3b392dd70c5314a185b5ad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279f03ee79381858d2bb135ff991e5aaf0aa8ffaf744a753919912ddb09333c`

```dockerfile
```

-	Layers:
	-	`sha256:2282099bc0f31d58ef838ab6a17c0609606bfe892cc5ac4f1a5d0b4c899cfe4f`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f848c0809977295036c07c2b1f7e4825a956355a0b6fdbdaf1b49fbf77e902`  
		Last Modified: Tue, 17 Feb 2026 23:26:15 GMT  
		Size: 35.8 KB (35781 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19` - linux; s390x

```console
$ docker pull cassandra@sha256:8ad326fa7497c0118c03ba6624917718382996ac6bfcd0fc83059501b7f3edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138736174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3add3a4d7738e85685b5c08976da7e2ab6dbfe08a051f72fed26029d5ea8af0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:58:47 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:59:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 22:00:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 22:00:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:00:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 22:00:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c1d613eb90a63326ac47071d5fd3825317137acb4a94756ce9a04d2388496`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d84ab4976a7aa1013ab95c7c6cc3f6b9a11fa592233e14569df223ff1583b5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 17.5 MB (17454908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ae11a27e935ea0df1d1a506e31ebefa8cf04807ac3f7c30b95bf384852cf5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.2 MB (1240737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9886db6e61a662ba25a7faaef3af2630ba7f28983462b969ab6514c6d01e805`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 41.3 MB (41303109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c72d5ae6113f4c0b31330cdd50c0faa6bee4df7a036dd233a062a41d7236d7`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbd9b4a3a8eb40d1b01a1aae186bb9b7af51bd3a4b114fd3e3b9c9e2cd283e`  
		Last Modified: Tue, 17 Feb 2026 22:01:15 GMT  
		Size: 51.9 MB (51850573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387db55b22c8771f280c74d5cd2a4154a5b4dc3df08a7dee065ebd35f874574b`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19` - unknown; unknown

```console
$ docker pull cassandra@sha256:c8b6521ff9e158467284b2ad39208efc2f68405858b2a24df998f73d6a18233a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58caa7320ab4172c7d6d49e7adb4634a25c8a4d3b3db496c997a2d97d1b3007`

```dockerfile
```

-	Layers:
	-	`sha256:6040450fec81cbf0a29d5b821ec2dc6bd83a0021e69e2b307fc9808873f4c54a`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9c266e2a2da75cb7a6a16db61513d92825c6efe5aebb21906a6e4427b4865f`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.0.19-bookworm`

```console
$ docker pull cassandra@sha256:d4b062feb91ccbf1a16d8f31eda79c01d60ed143db970940cf0336b5d5d2654e
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
$ docker pull cassandra@sha256:5acfc1373a147771ac29ae59cc830c216b02afe01a9f058c22852eff23db344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be597501a681e5b47d92582a26ace6aaa6ac4835a977c1424b25ec50c2dc046d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:21 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:38 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:38 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 19:51:38 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 19:51:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:56 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:56 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa19148b1e5c95f0cecad947e969b1d8e8f6078ff46ad459ec0ba29898acc6`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb30cdce8ec678fade8303f156fb76735c6833c96b7a37863616268471bbe00`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 18.2 MB (18150147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de1e26862336f65aece4232489672fb873f0760c928f3ef7332a0a400ef6f3`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 1.3 MB (1266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45aa6f04cbee08fd5af7dea016dfd56ab4a4405614ad52d070b799d6e9481fa`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 47.3 MB (47294888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ebcf0ebc5c8fc0629715b7aae05f7fdc0782f82924fd085dc888386edd2905`  
		Last Modified: Tue, 24 Feb 2026 19:52:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed444c976433cb5bad6ed75d6503184929f9dc8edd2fd75e94d355e00e1598c`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 51.9 MB (51850329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69945dd4ab329cf57c039a8bab01c57a90b57809f591497b530b4d414164b2`  
		Last Modified: Tue, 24 Feb 2026 19:52:11 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:ae244994c3bf5346d85e4a839cf9ebafd0a7e233bd188b4b2fcafbe924a8f19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59885fa4b5cb256e594c6dd4f582bf97cf63e8b6a708c2f9c0020ddae9cc3e19`

```dockerfile
```

-	Layers:
	-	`sha256:5382812a7a4960c8f412359b7d0b874507dd701c4137698010c324d0a356db6e`  
		Last Modified: Tue, 24 Feb 2026 19:52:09 GMT  
		Size: 3.3 MB (3274743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e342759cc5713ccf82d25aa43254e288907ce83418e9be0477f85c7c779169dd`  
		Last Modified: Tue, 24 Feb 2026 19:52:08 GMT  
		Size: 35.7 KB (35718 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:12d9994dfdd7a47dd4c5387f64906051b8618c718858528c601fbb6e2ed7a720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138650079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3126dbc6f15b6521440bcf14eb5b29fdc3cf661eab9f4923d0e1e1122fa5fa8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:10:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:10:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:10:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:10:01 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:01 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 21:10:01 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:21 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:21 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a2ecc644aafa57ffb898ac2eedc38632bc38d42153e6f3b0af8a2aad70f31`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9923475f87c012d222361d32b3f217db6188fdeb8f3319a1b2a5a6ae3d417ff`  
		Last Modified: Tue, 24 Feb 2026 21:10:34 GMT  
		Size: 16.2 MB (16209321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b74e81c3d06a0e7ab4ad398c3a334f944c7cfe897d08a7343688233349225`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 1.2 MB (1232656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f7f4d60ba5590fb09668226c04f7afaeb759c27f52bc4d45aa8610004481c9`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 45.4 MB (45413842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918bc4a2db2972a07bd1d7f666f572e2edc6381c3ed0ebf2bef69e503ed5a22d`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3150c139e9a82e5752370652b2b076430a7ee2a13938dc4865dd3be238d5b4f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:36 GMT  
		Size: 51.9 MB (51850404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311f408c80e358d10a47e187941a8bc49c9cbc29a79390da8ab996f24fc35003`  
		Last Modified: Tue, 24 Feb 2026 21:10:35 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:5fadb5681997e02662ae8053f74cd529dc69b2f2cd6f843a3c06b960aefcc1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47d986e9d110e786e67ba7c762c28b8bb68764bdfac6241fbbd298a0529a1c3`

```dockerfile
```

-	Layers:
	-	`sha256:aba92ea8202c851f5df74aa06d5c0d30c5d983c27b371129586b958d1acad9b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 3.3 MB (3278457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229b6829356babbbd8e08e8d795077636d4dadc9b34cd97c9ec1b096b9b1b374`  
		Last Modified: Tue, 24 Feb 2026 21:10:33 GMT  
		Size: 35.9 KB (35872 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:43326ba726f615946af911fa218a19ccceb5d72544acb2f8ba8993af2006480b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144694678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81f81c8f608571e1332534e466cc4bce6a4d44be6237e18d6ab838e2c7bb005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:41 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:59 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 24 Feb 2026 20:01:59 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 24 Feb 2026 20:02:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:15 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:15 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776c6fcbca943e250cb7717026819146c2c3986621ea9125ca3523806734169`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15732dabcc36d4b5fd3115040b7c52d318009b923315b1b83b7f9e1cae4bdfcf`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 17.9 MB (17888534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c762f98953f3f3959fd5bc5d692820f4b3d73714419eb95f5a9a27f94d2f2`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 1.2 MB (1220132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cfad825ffb6e2adf83e44ffc31aa7f14ea00719aa6c677320e75df731692d`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 45.6 MB (45617125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f9f4004a5e1d681b965056eea11359ca257c4d32115dad9c6cd1be3f95879b`  
		Last Modified: Tue, 24 Feb 2026 20:02:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f4e3fe70ce6ac131d0aa3f72ca5aa33da8d18906669501cbc0e14949f354c`  
		Last Modified: Tue, 24 Feb 2026 20:02:31 GMT  
		Size: 51.9 MB (51850347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bed2a99751bef806f11d9f7a4a7e87bb14ca14a1f0eb78349a532f982d4a40`  
		Last Modified: Tue, 24 Feb 2026 20:02:30 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:a07d210d5736829a5952c80dfdbb11939f36e828ef75a09b4507fe531a0231e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c268a290083c9f261a6e404b76edf8ac6ff1385c83d25f3bfcc3b9f12cd2f9a2`

```dockerfile
```

-	Layers:
	-	`sha256:2d6792d7a9be992bb0210c30bf69dbe47cf0778159c4b24625479cfb19687d59`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 3.3 MB (3275078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dba16b3be229d60309c9e0e64d4458b897dc5f886f85822d6688576cfb4c4c9`  
		Last Modified: Tue, 24 Feb 2026 20:02:28 GMT  
		Size: 35.9 KB (35908 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:f549ce9e15bc974835f173aa2cc3c19d6f044b22947b0a954a9b0899608e6d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147382447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da15b83fd3eb3220c8f582c198dd0a50bf2831da718bd7e2809718887e1e`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 23:25:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:56 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:57 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:57 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60bf54c7c2f216842406367a2ab7f8c5f0891bb3592c811701c0947cc1a34e1`  
		Last Modified: Tue, 17 Feb 2026 23:26:17 GMT  
		Size: 51.9 MB (51850532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d9fbda36b1983477dd9702a7d58a21086e387721dc688bb2d54631ff4d1ab`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:5731200717490f3267f8b7ef2a72f2eb1f1ceb5f3b392dd70c5314a185b5ad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279f03ee79381858d2bb135ff991e5aaf0aa8ffaf744a753919912ddb09333c`

```dockerfile
```

-	Layers:
	-	`sha256:2282099bc0f31d58ef838ab6a17c0609606bfe892cc5ac4f1a5d0b4c899cfe4f`  
		Last Modified: Tue, 17 Feb 2026 23:26:16 GMT  
		Size: 3.3 MB (3278991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f848c0809977295036c07c2b1f7e4825a956355a0b6fdbdaf1b49fbf77e902`  
		Last Modified: Tue, 17 Feb 2026 23:26:15 GMT  
		Size: 35.8 KB (35781 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.0.19-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:8ad326fa7497c0118c03ba6624917718382996ac6bfcd0fc83059501b7f3edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138736174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3add3a4d7738e85685b5c08976da7e2ab6dbfe08a051f72fed26029d5ea8af0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:58:47 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 17 Feb 2026 21:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 21:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 21:59:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:59:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:59:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:59:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_VERSION=4.0.19
# Tue, 17 Feb 2026 21:59:51 GMT
ENV CASSANDRA_SHA512=2b12b97ebe2be27a468397ab58006708a474d53d3cf636de7405cce404cbffad2194e72de85e5d60a9f4d9626cbdfc7d06588a0cea037e34497f0aa1edc80e44
# Tue, 17 Feb 2026 22:00:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 22:00:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 22:00:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:00:26 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 22:00:26 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c1d613eb90a63326ac47071d5fd3825317137acb4a94756ce9a04d2388496`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d84ab4976a7aa1013ab95c7c6cc3f6b9a11fa592233e14569df223ff1583b5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 17.5 MB (17454908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ae11a27e935ea0df1d1a506e31ebefa8cf04807ac3f7c30b95bf384852cf5`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 1.2 MB (1240737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9886db6e61a662ba25a7faaef3af2630ba7f28983462b969ab6514c6d01e805`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 41.3 MB (41303109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c72d5ae6113f4c0b31330cdd50c0faa6bee4df7a036dd233a062a41d7236d7`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbd9b4a3a8eb40d1b01a1aae186bb9b7af51bd3a4b114fd3e3b9c9e2cd283e`  
		Last Modified: Tue, 17 Feb 2026 22:01:15 GMT  
		Size: 51.9 MB (51850573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387db55b22c8771f280c74d5cd2a4154a5b4dc3df08a7dee065ebd35f874574b`  
		Last Modified: Tue, 17 Feb 2026 22:01:14 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.0.19-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:c8b6521ff9e158467284b2ad39208efc2f68405858b2a24df998f73d6a18233a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58caa7320ab4172c7d6d49e7adb4634a25c8a4d3b3db496c997a2d97d1b3007`

```dockerfile
```

-	Layers:
	-	`sha256:6040450fec81cbf0a29d5b821ec2dc6bd83a0021e69e2b307fc9808873f4c54a`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 3.3 MB (3270885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9c266e2a2da75cb7a6a16db61513d92825c6efe5aebb21906a6e4427b4865f`  
		Last Modified: Tue, 17 Feb 2026 22:01:13 GMT  
		Size: 35.7 KB (35719 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1`

```console
$ docker pull cassandra@sha256:3b96901e62443e4c241952d0de88abea083b0fb98cdde4a5b52021c164cc95dd
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
$ docker pull cassandra@sha256:17dc669f7c9a1260816e8f908711d6c17deaed17742ae171416d1e3fb221b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ced33659ee23d14e1a0d5d957d9409047313c734d5bfc7983afdac8be3fe9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:08 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 19:51:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:43 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:43 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c451d7bd1bdd623e0e08ab6dff5e016bcbe8f36861aa9a030c62f323c8a0e0`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0924908ceb4159ebfa239a90b4c3b237f672fc7c5276a42cba6d52c5b1b40ed4`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 18.1 MB (18149822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284250caa4b9682a982bca8ca932f21122c0f5e4f76240aad7e58194aee8a2e`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 1.3 MB (1266583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2567053f78671b186f9dad73efbdf200b173a1bd2aec9d3f3c85b0f4af645`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 47.3 MB (47294889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4787c302506d4d556de5d633ad1e4ee205c26d30f37bdb299c2b5a21569fceb6`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb904ebfcf32042b33e0386e9bb0fc6d1dee70aa787df30eb3e2c17dfbac68a`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 52.9 MB (52914354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34cd45cc2b16685214894fda1ff13a9a39acc2d039aa4b274529dc30997118`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:1efc4518fc2df4d6816e8c3af0bfc89d18ced91ba57fafec2653242efec380fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea705d0c2b3dadf5eedd15c6017ae0ae6236dc0e07aa50c59ad1e6c75c4c858`

```dockerfile
```

-	Layers:
	-	`sha256:8ab1755e0b922fac453c7d7e8c3f02a04fc226e3209b9fc4fed00da9d05255a2`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c20d9b6468f2d2f9818b33012a128104a02580fbf1ded5fe254913e24ca113e`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:6c37b87490cb8d3573e30ee104f15f342abede27d2b2a01a07294bf55ee19052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1ec595db034761a62a17961e5ab30ce4c7725a026134405006132ce8b5790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:32 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 21:10:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:12 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:12 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc7063224ccd2d852c86ca2d3e9ba35718da1ff1487c0b99b3a32645e5c9e10`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13e196ef36b54bcb66d87ad4d4de07f63e79c2d522e3d213d84e89fbb279a9`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 16.2 MB (16209300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83637cdc95e7bb122906eee09ba9cd9eefd9c37b055ae9628eb8f7aaab276b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.2 MB (1232642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824a46883e448fd7a4022dbdd5340aaea423cbb18e302c7bfe47ef7482731beb`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 45.4 MB (45413860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbe148ec44193032e42de9b2b7334ae48dfc5a582b771f16b4f3a698c65dbe`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d7c1eedfe6c0fc1ca4aa0af78ebf527002fe812e9f4e28da7765d566cb79e`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 52.9 MB (52914505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6f221d4f32c84daffbc7f2df93d48ceb0a17e2544f30220d4f4092c43ec45`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4479cd4e3a0c13d73f1bcf5087adb3a2e96da176ba6e47a9d7cf323a7c61d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95514322c075a261e447ed962ab70d011cf7052cf35faf70c0e350acbf19c76`

```dockerfile
```

-	Layers:
	-	`sha256:138f65c798315d52ad9b7e22fd65208ea49dda746e2183ddd836bf26dd45b53b`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da383a9b628463bb5ae9005d4a307016fe050bcf71971021281f8f4b8d125db`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:e8555f52b54a31acba9f0bf10d6ced1426b09caa1c2a1a3642b28c7a2d911ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3906bfa310c774f020a5e76fed9c9e3c15e7205c183e160b641bfbc61e7891dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:31 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:08 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef79d776c2b52fe440faa84c52e71c6230a23a4ba30224c87cb1420baad085d`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c948817d15e429f907513f5421702f5049800cbd80d4fef6bfe47432ef0f7`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 17.9 MB (17888673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41730693b0a73838483aa3515f3ecf51ea817cda056d457bf38ae6ce1697bc68`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac89d9c702f85a7acb7578d5d6596d29a397e8328160b2b070bb461ebbb10d7`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 45.6 MB (45617132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4a6dd9827dac2a273a204977dc2366aec5e476c6b699155b5a5688dd9236e`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec0f2a506a5054efa6a0b65ba627944d264981867a580310084f82ae36dc0b`  
		Last Modified: Tue, 24 Feb 2026 20:02:24 GMT  
		Size: 52.9 MB (52914436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79bec185a2d3ced951cc759b4de25d2d5d719fe39d17f2e822ce3196426f92c`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:e62270f4072338ce6e88ec443891c88c11dd7a9fa6d988de617be08ef6e2bf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6093a2ab0ed44333db3ae568d889ed569187324385152acd5709fa9c41dccd4`

```dockerfile
```

-	Layers:
	-	`sha256:5dc81ead25e1d00e1b2b87619ecb927b8bf1e672120498ea42248219ae90f681`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d6b03010f966e94de1d7c6f1f0cf14b0907068b7a6bb5dd4b16ec8499b2d3`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; ppc64le

```console
$ docker pull cassandra@sha256:3c37654ffdc9ebfc42c9fd5b49c2e38f07d72b5e330843277a491f2511ea4d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148446597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e5b5640a3df560846af52408926e9b7413446a7dd346fc5c7a71a50a48798`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 23:25:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:05 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:07 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad00f890abc48b985889dd9a231206a616f5cf1142fdc34cf379e4e1919978`  
		Last Modified: Tue, 17 Feb 2026 23:25:37 GMT  
		Size: 52.9 MB (52914681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a66f595378cad72ae44f0d032e2027db2941617a80748f9dfa3017a603c6f`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:9df10ae3e45f48d92eb1e0ee7f99fa3033ee6fa616e3ce7bbe62c9a023e59be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62759e1f57179d440733fe70cdfd9f3f4c730e95ff0804d1be574ec2170bd61`

```dockerfile
```

-	Layers:
	-	`sha256:639da1b568fbcf17866e05bd424e64b49b5f82aa14419a34d3ab7651b8129592`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d55c1cb6b8039832a3af27eaebe0fd3ba0d90a034a4e5cead1099ec2901a54`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 36.4 KB (36399 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1` - linux; s390x

```console
$ docker pull cassandra@sha256:643c323fc6f76a60e642fb41f61ca911ad3bb425e1245f888f0ceb5bbe9d4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139800049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f93ff6d0cb01ca2f9fb0f6f579f1f8110dde06ddb5a9ca51ebc4e63001d014`
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
# Tue, 17 Feb 2026 21:58:58 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 21:59:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:59:34 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:59:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:59:35 GMT
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
	-	`sha256:0bd18c0204322ef5bbba2d083e811e3f75cf6f32c94cf27dc4de277cf388ae03`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 41.3 MB (41303100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e1cd4d6d74ba9151275bb4500293ed750b9a9dd0fce14293c868f36ab8818`  
		Last Modified: Tue, 17 Feb 2026 22:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c8d780a09144af0f6ac9227774c238d327d8208201fff0a443fd4b1b3d0ba`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 52.9 MB (52914739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a40fd716f56a8144e5164fcd4ec85fe9cccc266e207b3ecf321123b950256`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1` - unknown; unknown

```console
$ docker pull cassandra@sha256:195cb6b7b00c4cd94dafb56e962d11a3eea1a111465e6b66009c47536467c495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63c07a9788c1a3a386aff2204908f77414d3c09ccb386d30cfe4f1e843fe2c4`

```dockerfile
```

-	Layers:
	-	`sha256:15101ce78632fc025fdee03d4d0d7afb71594a1cc9c686ffaf90e9dd2c0af682`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92262922929100823e3cff817bf33a620e15b2781dbe40d738056ec8a7a46027`  
		Last Modified: Tue, 17 Feb 2026 22:00:15 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1-bookworm`

```console
$ docker pull cassandra@sha256:3b96901e62443e4c241952d0de88abea083b0fb98cdde4a5b52021c164cc95dd
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
$ docker pull cassandra@sha256:17dc669f7c9a1260816e8f908711d6c17deaed17742ae171416d1e3fb221b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ced33659ee23d14e1a0d5d957d9409047313c734d5bfc7983afdac8be3fe9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:08 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 19:51:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:43 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:43 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c451d7bd1bdd623e0e08ab6dff5e016bcbe8f36861aa9a030c62f323c8a0e0`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0924908ceb4159ebfa239a90b4c3b237f672fc7c5276a42cba6d52c5b1b40ed4`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 18.1 MB (18149822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284250caa4b9682a982bca8ca932f21122c0f5e4f76240aad7e58194aee8a2e`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 1.3 MB (1266583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2567053f78671b186f9dad73efbdf200b173a1bd2aec9d3f3c85b0f4af645`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 47.3 MB (47294889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4787c302506d4d556de5d633ad1e4ee205c26d30f37bdb299c2b5a21569fceb6`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb904ebfcf32042b33e0386e9bb0fc6d1dee70aa787df30eb3e2c17dfbac68a`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 52.9 MB (52914354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34cd45cc2b16685214894fda1ff13a9a39acc2d039aa4b274529dc30997118`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:1efc4518fc2df4d6816e8c3af0bfc89d18ced91ba57fafec2653242efec380fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea705d0c2b3dadf5eedd15c6017ae0ae6236dc0e07aa50c59ad1e6c75c4c858`

```dockerfile
```

-	Layers:
	-	`sha256:8ab1755e0b922fac453c7d7e8c3f02a04fc226e3209b9fc4fed00da9d05255a2`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c20d9b6468f2d2f9818b33012a128104a02580fbf1ded5fe254913e24ca113e`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:6c37b87490cb8d3573e30ee104f15f342abede27d2b2a01a07294bf55ee19052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1ec595db034761a62a17961e5ab30ce4c7725a026134405006132ce8b5790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:32 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 21:10:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:12 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:12 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc7063224ccd2d852c86ca2d3e9ba35718da1ff1487c0b99b3a32645e5c9e10`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13e196ef36b54bcb66d87ad4d4de07f63e79c2d522e3d213d84e89fbb279a9`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 16.2 MB (16209300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83637cdc95e7bb122906eee09ba9cd9eefd9c37b055ae9628eb8f7aaab276b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.2 MB (1232642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824a46883e448fd7a4022dbdd5340aaea423cbb18e302c7bfe47ef7482731beb`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 45.4 MB (45413860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbe148ec44193032e42de9b2b7334ae48dfc5a582b771f16b4f3a698c65dbe`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d7c1eedfe6c0fc1ca4aa0af78ebf527002fe812e9f4e28da7765d566cb79e`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 52.9 MB (52914505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6f221d4f32c84daffbc7f2df93d48ceb0a17e2544f30220d4f4092c43ec45`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4479cd4e3a0c13d73f1bcf5087adb3a2e96da176ba6e47a9d7cf323a7c61d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95514322c075a261e447ed962ab70d011cf7052cf35faf70c0e350acbf19c76`

```dockerfile
```

-	Layers:
	-	`sha256:138f65c798315d52ad9b7e22fd65208ea49dda746e2183ddd836bf26dd45b53b`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da383a9b628463bb5ae9005d4a307016fe050bcf71971021281f8f4b8d125db`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:e8555f52b54a31acba9f0bf10d6ced1426b09caa1c2a1a3642b28c7a2d911ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3906bfa310c774f020a5e76fed9c9e3c15e7205c183e160b641bfbc61e7891dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:31 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:08 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef79d776c2b52fe440faa84c52e71c6230a23a4ba30224c87cb1420baad085d`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c948817d15e429f907513f5421702f5049800cbd80d4fef6bfe47432ef0f7`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 17.9 MB (17888673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41730693b0a73838483aa3515f3ecf51ea817cda056d457bf38ae6ce1697bc68`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac89d9c702f85a7acb7578d5d6596d29a397e8328160b2b070bb461ebbb10d7`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 45.6 MB (45617132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4a6dd9827dac2a273a204977dc2366aec5e476c6b699155b5a5688dd9236e`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec0f2a506a5054efa6a0b65ba627944d264981867a580310084f82ae36dc0b`  
		Last Modified: Tue, 24 Feb 2026 20:02:24 GMT  
		Size: 52.9 MB (52914436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79bec185a2d3ced951cc759b4de25d2d5d719fe39d17f2e822ce3196426f92c`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:e62270f4072338ce6e88ec443891c88c11dd7a9fa6d988de617be08ef6e2bf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6093a2ab0ed44333db3ae568d889ed569187324385152acd5709fa9c41dccd4`

```dockerfile
```

-	Layers:
	-	`sha256:5dc81ead25e1d00e1b2b87619ecb927b8bf1e672120498ea42248219ae90f681`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d6b03010f966e94de1d7c6f1f0cf14b0907068b7a6bb5dd4b16ec8499b2d3`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:3c37654ffdc9ebfc42c9fd5b49c2e38f07d72b5e330843277a491f2511ea4d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148446597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e5b5640a3df560846af52408926e9b7413446a7dd346fc5c7a71a50a48798`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 23:25:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:05 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:07 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad00f890abc48b985889dd9a231206a616f5cf1142fdc34cf379e4e1919978`  
		Last Modified: Tue, 17 Feb 2026 23:25:37 GMT  
		Size: 52.9 MB (52914681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a66f595378cad72ae44f0d032e2027db2941617a80748f9dfa3017a603c6f`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:9df10ae3e45f48d92eb1e0ee7f99fa3033ee6fa616e3ce7bbe62c9a023e59be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62759e1f57179d440733fe70cdfd9f3f4c730e95ff0804d1be574ec2170bd61`

```dockerfile
```

-	Layers:
	-	`sha256:639da1b568fbcf17866e05bd424e64b49b5f82aa14419a34d3ab7651b8129592`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d55c1cb6b8039832a3af27eaebe0fd3ba0d90a034a4e5cead1099ec2901a54`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 36.4 KB (36399 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:643c323fc6f76a60e642fb41f61ca911ad3bb425e1245f888f0ceb5bbe9d4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139800049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f93ff6d0cb01ca2f9fb0f6f579f1f8110dde06ddb5a9ca51ebc4e63001d014`
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
# Tue, 17 Feb 2026 21:58:58 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 21:59:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:59:34 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:59:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:59:35 GMT
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
	-	`sha256:0bd18c0204322ef5bbba2d083e811e3f75cf6f32c94cf27dc4de277cf388ae03`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 41.3 MB (41303100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e1cd4d6d74ba9151275bb4500293ed750b9a9dd0fce14293c868f36ab8818`  
		Last Modified: Tue, 17 Feb 2026 22:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c8d780a09144af0f6ac9227774c238d327d8208201fff0a443fd4b1b3d0ba`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 52.9 MB (52914739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a40fd716f56a8144e5164fcd4ec85fe9cccc266e207b3ecf321123b950256`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:195cb6b7b00c4cd94dafb56e962d11a3eea1a111465e6b66009c47536467c495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63c07a9788c1a3a386aff2204908f77414d3c09ccb386d30cfe4f1e843fe2c4`

```dockerfile
```

-	Layers:
	-	`sha256:15101ce78632fc025fdee03d4d0d7afb71594a1cc9c686ffaf90e9dd2c0af682`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92262922929100823e3cff817bf33a620e15b2781dbe40d738056ec8a7a46027`  
		Last Modified: Tue, 17 Feb 2026 22:00:15 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1.10`

```console
$ docker pull cassandra@sha256:3b96901e62443e4c241952d0de88abea083b0fb98cdde4a5b52021c164cc95dd
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
$ docker pull cassandra@sha256:17dc669f7c9a1260816e8f908711d6c17deaed17742ae171416d1e3fb221b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ced33659ee23d14e1a0d5d957d9409047313c734d5bfc7983afdac8be3fe9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:08 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 19:51:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:43 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:43 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c451d7bd1bdd623e0e08ab6dff5e016bcbe8f36861aa9a030c62f323c8a0e0`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0924908ceb4159ebfa239a90b4c3b237f672fc7c5276a42cba6d52c5b1b40ed4`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 18.1 MB (18149822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284250caa4b9682a982bca8ca932f21122c0f5e4f76240aad7e58194aee8a2e`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 1.3 MB (1266583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2567053f78671b186f9dad73efbdf200b173a1bd2aec9d3f3c85b0f4af645`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 47.3 MB (47294889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4787c302506d4d556de5d633ad1e4ee205c26d30f37bdb299c2b5a21569fceb6`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb904ebfcf32042b33e0386e9bb0fc6d1dee70aa787df30eb3e2c17dfbac68a`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 52.9 MB (52914354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34cd45cc2b16685214894fda1ff13a9a39acc2d039aa4b274529dc30997118`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:1efc4518fc2df4d6816e8c3af0bfc89d18ced91ba57fafec2653242efec380fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea705d0c2b3dadf5eedd15c6017ae0ae6236dc0e07aa50c59ad1e6c75c4c858`

```dockerfile
```

-	Layers:
	-	`sha256:8ab1755e0b922fac453c7d7e8c3f02a04fc226e3209b9fc4fed00da9d05255a2`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c20d9b6468f2d2f9818b33012a128104a02580fbf1ded5fe254913e24ca113e`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:6c37b87490cb8d3573e30ee104f15f342abede27d2b2a01a07294bf55ee19052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1ec595db034761a62a17961e5ab30ce4c7725a026134405006132ce8b5790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:32 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 21:10:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:12 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:12 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc7063224ccd2d852c86ca2d3e9ba35718da1ff1487c0b99b3a32645e5c9e10`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13e196ef36b54bcb66d87ad4d4de07f63e79c2d522e3d213d84e89fbb279a9`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 16.2 MB (16209300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83637cdc95e7bb122906eee09ba9cd9eefd9c37b055ae9628eb8f7aaab276b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.2 MB (1232642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824a46883e448fd7a4022dbdd5340aaea423cbb18e302c7bfe47ef7482731beb`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 45.4 MB (45413860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbe148ec44193032e42de9b2b7334ae48dfc5a582b771f16b4f3a698c65dbe`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d7c1eedfe6c0fc1ca4aa0af78ebf527002fe812e9f4e28da7765d566cb79e`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 52.9 MB (52914505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6f221d4f32c84daffbc7f2df93d48ceb0a17e2544f30220d4f4092c43ec45`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4479cd4e3a0c13d73f1bcf5087adb3a2e96da176ba6e47a9d7cf323a7c61d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95514322c075a261e447ed962ab70d011cf7052cf35faf70c0e350acbf19c76`

```dockerfile
```

-	Layers:
	-	`sha256:138f65c798315d52ad9b7e22fd65208ea49dda746e2183ddd836bf26dd45b53b`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da383a9b628463bb5ae9005d4a307016fe050bcf71971021281f8f4b8d125db`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:e8555f52b54a31acba9f0bf10d6ced1426b09caa1c2a1a3642b28c7a2d911ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3906bfa310c774f020a5e76fed9c9e3c15e7205c183e160b641bfbc61e7891dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:31 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:08 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef79d776c2b52fe440faa84c52e71c6230a23a4ba30224c87cb1420baad085d`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c948817d15e429f907513f5421702f5049800cbd80d4fef6bfe47432ef0f7`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 17.9 MB (17888673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41730693b0a73838483aa3515f3ecf51ea817cda056d457bf38ae6ce1697bc68`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac89d9c702f85a7acb7578d5d6596d29a397e8328160b2b070bb461ebbb10d7`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 45.6 MB (45617132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4a6dd9827dac2a273a204977dc2366aec5e476c6b699155b5a5688dd9236e`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec0f2a506a5054efa6a0b65ba627944d264981867a580310084f82ae36dc0b`  
		Last Modified: Tue, 24 Feb 2026 20:02:24 GMT  
		Size: 52.9 MB (52914436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79bec185a2d3ced951cc759b4de25d2d5d719fe39d17f2e822ce3196426f92c`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:e62270f4072338ce6e88ec443891c88c11dd7a9fa6d988de617be08ef6e2bf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6093a2ab0ed44333db3ae568d889ed569187324385152acd5709fa9c41dccd4`

```dockerfile
```

-	Layers:
	-	`sha256:5dc81ead25e1d00e1b2b87619ecb927b8bf1e672120498ea42248219ae90f681`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d6b03010f966e94de1d7c6f1f0cf14b0907068b7a6bb5dd4b16ec8499b2d3`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; ppc64le

```console
$ docker pull cassandra@sha256:3c37654ffdc9ebfc42c9fd5b49c2e38f07d72b5e330843277a491f2511ea4d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148446597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e5b5640a3df560846af52408926e9b7413446a7dd346fc5c7a71a50a48798`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 23:25:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:05 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:07 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad00f890abc48b985889dd9a231206a616f5cf1142fdc34cf379e4e1919978`  
		Last Modified: Tue, 17 Feb 2026 23:25:37 GMT  
		Size: 52.9 MB (52914681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a66f595378cad72ae44f0d032e2027db2941617a80748f9dfa3017a603c6f`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:9df10ae3e45f48d92eb1e0ee7f99fa3033ee6fa616e3ce7bbe62c9a023e59be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62759e1f57179d440733fe70cdfd9f3f4c730e95ff0804d1be574ec2170bd61`

```dockerfile
```

-	Layers:
	-	`sha256:639da1b568fbcf17866e05bd424e64b49b5f82aa14419a34d3ab7651b8129592`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d55c1cb6b8039832a3af27eaebe0fd3ba0d90a034a4e5cead1099ec2901a54`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 36.4 KB (36399 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10` - linux; s390x

```console
$ docker pull cassandra@sha256:643c323fc6f76a60e642fb41f61ca911ad3bb425e1245f888f0ceb5bbe9d4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139800049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f93ff6d0cb01ca2f9fb0f6f579f1f8110dde06ddb5a9ca51ebc4e63001d014`
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
# Tue, 17 Feb 2026 21:58:58 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 21:59:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:59:34 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:59:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:59:35 GMT
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
	-	`sha256:0bd18c0204322ef5bbba2d083e811e3f75cf6f32c94cf27dc4de277cf388ae03`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 41.3 MB (41303100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e1cd4d6d74ba9151275bb4500293ed750b9a9dd0fce14293c868f36ab8818`  
		Last Modified: Tue, 17 Feb 2026 22:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c8d780a09144af0f6ac9227774c238d327d8208201fff0a443fd4b1b3d0ba`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 52.9 MB (52914739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a40fd716f56a8144e5164fcd4ec85fe9cccc266e207b3ecf321123b950256`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10` - unknown; unknown

```console
$ docker pull cassandra@sha256:195cb6b7b00c4cd94dafb56e962d11a3eea1a111465e6b66009c47536467c495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63c07a9788c1a3a386aff2204908f77414d3c09ccb386d30cfe4f1e843fe2c4`

```dockerfile
```

-	Layers:
	-	`sha256:15101ce78632fc025fdee03d4d0d7afb71594a1cc9c686ffaf90e9dd2c0af682`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92262922929100823e3cff817bf33a620e15b2781dbe40d738056ec8a7a46027`  
		Last Modified: Tue, 17 Feb 2026 22:00:15 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:4.1.10-bookworm`

```console
$ docker pull cassandra@sha256:3b96901e62443e4c241952d0de88abea083b0fb98cdde4a5b52021c164cc95dd
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
$ docker pull cassandra@sha256:17dc669f7c9a1260816e8f908711d6c17deaed17742ae171416d1e3fb221b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147864387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ced33659ee23d14e1a0d5d957d9409047313c734d5bfc7983afdac8be3fe9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:08 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:25 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:25 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 19:51:25 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 19:51:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:43 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:43 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c451d7bd1bdd623e0e08ab6dff5e016bcbe8f36861aa9a030c62f323c8a0e0`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0924908ceb4159ebfa239a90b4c3b237f672fc7c5276a42cba6d52c5b1b40ed4`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 18.1 MB (18149822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284250caa4b9682a982bca8ca932f21122c0f5e4f76240aad7e58194aee8a2e`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 1.3 MB (1266583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2567053f78671b186f9dad73efbdf200b173a1bd2aec9d3f3c85b0f4af645`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 47.3 MB (47294889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4787c302506d4d556de5d633ad1e4ee205c26d30f37bdb299c2b5a21569fceb6`  
		Last Modified: Tue, 24 Feb 2026 19:51:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb904ebfcf32042b33e0386e9bb0fc6d1dee70aa787df30eb3e2c17dfbac68a`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 52.9 MB (52914354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34cd45cc2b16685214894fda1ff13a9a39acc2d039aa4b274529dc30997118`  
		Last Modified: Tue, 24 Feb 2026 19:51:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:1efc4518fc2df4d6816e8c3af0bfc89d18ced91ba57fafec2653242efec380fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea705d0c2b3dadf5eedd15c6017ae0ae6236dc0e07aa50c59ad1e6c75c4c858`

```dockerfile
```

-	Layers:
	-	`sha256:8ab1755e0b922fac453c7d7e8c3f02a04fc226e3209b9fc4fed00da9d05255a2`  
		Last Modified: Tue, 24 Feb 2026 19:51:56 GMT  
		Size: 3.3 MB (3277695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c20d9b6468f2d2f9818b33012a128104a02580fbf1ded5fe254913e24ca113e`  
		Last Modified: Tue, 24 Feb 2026 19:51:55 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:6c37b87490cb8d3573e30ee104f15f342abede27d2b2a01a07294bf55ee19052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1ec595db034761a62a17961e5ab30ce4c7725a026134405006132ce8b5790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:32 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 21:09:51 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 21:10:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:12 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:12 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc7063224ccd2d852c86ca2d3e9ba35718da1ff1487c0b99b3a32645e5c9e10`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13e196ef36b54bcb66d87ad4d4de07f63e79c2d522e3d213d84e89fbb279a9`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 16.2 MB (16209300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83637cdc95e7bb122906eee09ba9cd9eefd9c37b055ae9628eb8f7aaab276b6`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 1.2 MB (1232642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824a46883e448fd7a4022dbdd5340aaea423cbb18e302c7bfe47ef7482731beb`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 45.4 MB (45413860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbe148ec44193032e42de9b2b7334ae48dfc5a582b771f16b4f3a698c65dbe`  
		Last Modified: Tue, 24 Feb 2026 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d7c1eedfe6c0fc1ca4aa0af78ebf527002fe812e9f4e28da7765d566cb79e`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 52.9 MB (52914505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6f221d4f32c84daffbc7f2df93d48ceb0a17e2544f30220d4f4092c43ec45`  
		Last Modified: Tue, 24 Feb 2026 21:10:26 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b4479cd4e3a0c13d73f1bcf5087adb3a2e96da176ba6e47a9d7cf323a7c61d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95514322c075a261e447ed962ab70d011cf7052cf35faf70c0e350acbf19c76`

```dockerfile
```

-	Layers:
	-	`sha256:138f65c798315d52ad9b7e22fd65208ea49dda746e2183ddd836bf26dd45b53b`  
		Last Modified: Tue, 24 Feb 2026 21:10:24 GMT  
		Size: 3.3 MB (3281425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da383a9b628463bb5ae9005d4a307016fe050bcf71971021281f8f4b8d125db`  
		Last Modified: Tue, 24 Feb 2026 21:10:23 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:e8555f52b54a31acba9f0bf10d6ced1426b09caa1c2a1a3642b28c7a2d911ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145758917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3906bfa310c774f020a5e76fed9c9e3c15e7205c183e160b641bfbc61e7891dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:31 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:01:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:01:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:50 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 24 Feb 2026 20:01:50 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:08 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef79d776c2b52fe440faa84c52e71c6230a23a4ba30224c87cb1420baad085d`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c948817d15e429f907513f5421702f5049800cbd80d4fef6bfe47432ef0f7`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 17.9 MB (17888673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41730693b0a73838483aa3515f3ecf51ea817cda056d457bf38ae6ce1697bc68`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac89d9c702f85a7acb7578d5d6596d29a397e8328160b2b070bb461ebbb10d7`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 45.6 MB (45617132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4a6dd9827dac2a273a204977dc2366aec5e476c6b699155b5a5688dd9236e`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec0f2a506a5054efa6a0b65ba627944d264981867a580310084f82ae36dc0b`  
		Last Modified: Tue, 24 Feb 2026 20:02:24 GMT  
		Size: 52.9 MB (52914436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79bec185a2d3ced951cc759b4de25d2d5d719fe39d17f2e822ce3196426f92c`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:e62270f4072338ce6e88ec443891c88c11dd7a9fa6d988de617be08ef6e2bf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6093a2ab0ed44333db3ae568d889ed569187324385152acd5709fa9c41dccd4`

```dockerfile
```

-	Layers:
	-	`sha256:5dc81ead25e1d00e1b2b87619ecb927b8bf1e672120498ea42248219ae90f681`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 3.3 MB (3278054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d6b03010f966e94de1d7c6f1f0cf14b0907068b7a6bb5dd4b16ec8499b2d3`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 36.5 KB (36539 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:3c37654ffdc9ebfc42c9fd5b49c2e38f07d72b5e330843277a491f2511ea4d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148446597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e5b5640a3df560846af52408926e9b7413446a7dd346fc5c7a71a50a48798`
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
# Tue, 17 Feb 2026 23:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:24:24 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:24:24 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 23:24:24 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 23:25:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:25:05 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:25:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:25:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:25:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:25:07 GMT
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
	-	`sha256:81ddcab3bb23e6ac42f4c3b74fae9e421c0b145929540a1e23572e4e81bda39c`  
		Last Modified: Tue, 17 Feb 2026 23:25:36 GMT  
		Size: 42.7 MB (42741952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee08986307c3dbecfa78b9f6a88b6cad2d6e65f3f53a547aaa40c41ab3c9a36`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad00f890abc48b985889dd9a231206a616f5cf1142fdc34cf379e4e1919978`  
		Last Modified: Tue, 17 Feb 2026 23:25:37 GMT  
		Size: 52.9 MB (52914681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a66f595378cad72ae44f0d032e2027db2941617a80748f9dfa3017a603c6f`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:9df10ae3e45f48d92eb1e0ee7f99fa3033ee6fa616e3ce7bbe62c9a023e59be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62759e1f57179d440733fe70cdfd9f3f4c730e95ff0804d1be574ec2170bd61`

```dockerfile
```

-	Layers:
	-	`sha256:639da1b568fbcf17866e05bd424e64b49b5f82aa14419a34d3ab7651b8129592`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 3.3 MB (3281955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d55c1cb6b8039832a3af27eaebe0fd3ba0d90a034a4e5cead1099ec2901a54`  
		Last Modified: Tue, 17 Feb 2026 23:25:34 GMT  
		Size: 36.4 KB (36399 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:4.1.10-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:643c323fc6f76a60e642fb41f61ca911ad3bb425e1245f888f0ceb5bbe9d4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139800049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f93ff6d0cb01ca2f9fb0f6f579f1f8110dde06ddb5a9ca51ebc4e63001d014`
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
# Tue, 17 Feb 2026 21:58:58 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 21:58:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_VERSION=4.1.10
# Tue, 17 Feb 2026 21:58:58 GMT
ENV CASSANDRA_SHA512=42b941e230287adc6a3763db5d2d5d3b57e80f1d151f9582b6ac17a86971d601a5a1979b341ac1e00c1ca0eb7d0690c7e615dbad1d81fa76df195de0376d78a8
# Tue, 17 Feb 2026 21:59:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 21:59:34 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 21:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:59:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 21:59:35 GMT
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
	-	`sha256:0bd18c0204322ef5bbba2d083e811e3f75cf6f32c94cf27dc4de277cf388ae03`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 41.3 MB (41303100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e1cd4d6d74ba9151275bb4500293ed750b9a9dd0fce14293c868f36ab8818`  
		Last Modified: Tue, 17 Feb 2026 22:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c8d780a09144af0f6ac9227774c238d327d8208201fff0a443fd4b1b3d0ba`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 52.9 MB (52914739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a40fd716f56a8144e5164fcd4ec85fe9cccc266e207b3ecf321123b950256`  
		Last Modified: Tue, 17 Feb 2026 22:00:18 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:4.1.10-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:195cb6b7b00c4cd94dafb56e962d11a3eea1a111465e6b66009c47536467c495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63c07a9788c1a3a386aff2204908f77414d3c09ccb386d30cfe4f1e843fe2c4`

```dockerfile
```

-	Layers:
	-	`sha256:15101ce78632fc025fdee03d4d0d7afb71594a1cc9c686ffaf90e9dd2c0af682`  
		Last Modified: Tue, 17 Feb 2026 22:00:16 GMT  
		Size: 3.3 MB (3273837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92262922929100823e3cff817bf33a620e15b2781dbe40d738056ec8a7a46027`  
		Last Modified: Tue, 17 Feb 2026 22:00:15 GMT  
		Size: 36.3 KB (36325 bytes)  
		MIME: application/vnd.in-toto+json

## `cassandra:5`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5` - linux; s390x

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

### `cassandra:5` - unknown; unknown

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

## `cassandra:5-bookworm`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; s390x

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

### `cassandra:5-bookworm` - unknown; unknown

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

## `cassandra:5.0`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0` - linux; s390x

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

### `cassandra:5.0` - unknown; unknown

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

## `cassandra:5.0-bookworm`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0-bookworm` - linux; s390x

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

### `cassandra:5.0-bookworm` - unknown; unknown

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

## `cassandra:5.0.6`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6` - linux; s390x

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

### `cassandra:5.0.6` - unknown; unknown

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

## `cassandra:5.0.6-bookworm`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5.0.6-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5.0.6-bookworm` - linux; s390x

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

### `cassandra:5.0.6-bookworm` - unknown; unknown

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

## `cassandra:bookworm`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:bookworm` - linux; s390x

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

### `cassandra:bookworm` - unknown; unknown

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

## `cassandra:latest`

```console
$ docker pull cassandra@sha256:c4ceeea3f8006de96d63e0bc0f970d7cdc10b3b8de466759076ac26bd23357d0
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
$ docker pull cassandra@sha256:43d999c17c85e79690b767c4b8ab717b69d4f0ef446d7ec02a7d2cf623f0b96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168330940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd6e3860c588ee6f458cb16e25380dd409ace904ca83c667b1d433796fa30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:58 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 19:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:51:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:51:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 19:51:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 19:51:16 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 19:51:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 19:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:51:36 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 19:51:36 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27baa5432da969484585f2aff66cd2bc6ca042e5cc548473cab994d3310b2c8`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc42dcbc39bb4fb5dc7d857881a0c3c69c478e47834c42f269832cf6d0325b8`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 18.1 MB (18149928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c8e6c95cfd32a23b4a10174f33b200aa9742ffbd5156ebec53e94ba5f6172c`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 1.3 MB (1266597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce2b52e9b5477ee760829f83e96aae7b9f8866debd3ac59aefef24506b32177`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 47.4 MB (47429818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20b4b8b2250e0bd41534753d6b4f548ee55217005a3b768b1f5c57c705a019`  
		Last Modified: Tue, 24 Feb 2026 19:51:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00f7329f3e802f81d5b0dd9f48cc2452c2c640be5bfa97c7d0fa85037eacb3`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 73.2 MB (73245858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f75375eebfa8ed3ed9331da2da35076be26d02630074bcbbe95d6dd59eaf8b`  
		Last Modified: Tue, 24 Feb 2026 19:51:51 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:549d6ed8b0247d479f53770af5c5b4d7d7df7a1df6bd2e12098f0195771c39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64d298717c0478bc1c266172771369be1aaa2d2418ebf9adb20074ce70cfc2d`

```dockerfile
```

-	Layers:
	-	`sha256:0f000f9c9da3b20dfbcce70a54d99f1805b07d10865fdec72b1fce179d3fa478`  
		Last Modified: Tue, 24 Feb 2026 19:51:49 GMT  
		Size: 3.3 MB (3306162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3709b88bc8405622dc885912ac43249dfbb169e1d6c3a55182eae399254c8fa2`  
		Last Modified: Tue, 24 Feb 2026 19:51:48 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cc14882c9ce293c85b0ddf4f3230f870a6d5461dc7018b487106de057aa8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb70e949a430a7410d6269a64fb5ec3a35132f7e3e2cbed3c1b7f1193f35d9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:09:25 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 21:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:09:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 21:09:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 21:09:45 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:45 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 21:09:45 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 21:10:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 21:10:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:10:07 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 21:10:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36feb43969f5011a394e61887c844ff61dc475a3d4efdab3bf4ee4c8e4c1e90f`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcf2aae45f180ed9513c9f05d3bb1f2763cbc8676a005317f2bc7ae38d25f4`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 16.2 MB (16209278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f29277dcb0c4e3d58d737773364d5c0b50149eb0e417f2ad439f839321ecc2`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 1.2 MB (1232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb979853e6a1d7a0dcab6e195d8dce2c7c46a21469dbb79da88fedcfbddba`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 45.0 MB (45037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c4baf1c9871c8c4f2c75ac8a79193cfd503617422b8d0c95a287d7ce134d6`  
		Last Modified: Tue, 24 Feb 2026 21:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2358148cb36a98539a4fdea308c8bf2f16144c76b497313e8cbf6a96b6d`  
		Last Modified: Tue, 24 Feb 2026 21:10:22 GMT  
		Size: 73.2 MB (73245908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30e16871850e1edc32eb57db06e5d89dcb588013185fcf3e27e47ca1285385`  
		Last Modified: Tue, 24 Feb 2026 21:10:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:53fbd2d8b61ff38c4e800118c571b01421c7a5752a26965c5977907f13bc8850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e72e19353ae452c8eb957215ba6bc89d14ec25fe2e485b0aba6fe45c5137ba7`

```dockerfile
```

-	Layers:
	-	`sha256:71c942593efedc74d0bb4c56935122f886a3a84013ae77c0591fdb235b5e0146`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 3.3 MB (3308645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9cb9978b631b393a89b92355ffdb39ba359bed9872b28906f549c68dfd79ed`  
		Last Modified: Tue, 24 Feb 2026 21:10:19 GMT  
		Size: 37.1 KB (37113 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:4b125b89280bdc360719f417dc0ace98ad37d1e7cfc83e397511a27837e4f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279dba66eb1697fb6d956502102e5c44481daa8164a4992538fb85d4dcd61e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Tue, 24 Feb 2026 20:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:02:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
RUN java --version # buildkit
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 24 Feb 2026 20:02:09 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:09 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 24 Feb 2026 20:02:09 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 24 Feb 2026 20:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 24 Feb 2026 20:02:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 24 Feb 2026 20:02:28 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1168cbeb0023920e5f5f39fe2f0024ce679ba71f856a00c8785df94cc8f7a94`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c5762cdc58f0f3947a8c55168df624c5b48ebb26b20a2a643b06977afeb968`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 17.9 MB (17888414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2053c887af64adeb885d53fe908e276c6f502034f01b7c62f925790618c6432`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 1.2 MB (1220118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1bd1d3d92da07d3b0a8267714ecb5fd6192ebcfb05becd94ab53205bc572d`  
		Last Modified: Tue, 24 Feb 2026 20:02:43 GMT  
		Size: 46.9 MB (46910199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c07bfe2518aeb0b09a48e1e969d8dacb6d595e2f6e4053132c4e56075924617`  
		Last Modified: Tue, 24 Feb 2026 20:02:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218dd6f29fa8a65e7cf333b233f28a51d0bca4db7b91ca5b0aa538e320b647f`  
		Last Modified: Tue, 24 Feb 2026 20:02:45 GMT  
		Size: 73.2 MB (73245816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505925c28a839e91d6e6a6f054b2893201c74d16a36009b9fbe05b82cf34b8b`  
		Last Modified: Tue, 24 Feb 2026 20:02:44 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:788af65992bf90b5be5c897e4fbb6cb445252678a2e40e01e70734f5e5b21fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7505bdf2e4394c3a3dd01f2bac1fddb1761d0a578e1bf2a506950e77dd971`

```dockerfile
```

-	Layers:
	-	`sha256:9b30032a978f1aa8fc3875868c5e30f083d7de69a91edc1f6d8a137dec6fab40`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 3.3 MB (3305927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8525d7c09e5022fd5f9f4d060cd27964a1309fae473e4eb295aa169e0f2b1e`  
		Last Modified: Tue, 24 Feb 2026 20:02:41 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:bbb44377a7e2c0071904e4891f9e5d9986a3acd7f898e1133bf87062dfb31838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173363701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493098acb508a21fd0a9e772c9a11e93b88b1431cdfe45ec28b939ec7e695d42`
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
# Tue, 17 Feb 2026 23:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
RUN java --version # buildkit
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Tue, 17 Feb 2026 23:23:26 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:23:26 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_VERSION=5.0.6
# Tue, 17 Feb 2026 23:23:26 GMT
ENV CASSANDRA_SHA512=cab82049269e91ecd13e525254427d9b6139d8982fd1ddb8256ac7ebebc2fae412721750d7b30b1ee4e86f81d1960a87a2220d4a4a34d11f05c5aca0be6cd649
# Tue, 17 Feb 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
VOLUME [/var/lib/cassandra]
# Tue, 17 Feb 2026 23:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 23:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 23:24:28 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Tue, 17 Feb 2026 23:24:28 GMT
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
	-	`sha256:75e677c38b220f7f859b9811f4a6857307ff7848a3d01b4372d4e4e5d1cd5de9`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 47.3 MB (47327647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba8a46a3b9a512e9216442956ba03768e32d57ef2a29916c32c7d817397e54`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b02ba306a4ddbfa81a23cddd4225bd1530ece25cc037af7518f693110c7be`  
		Last Modified: Tue, 17 Feb 2026 23:25:01 GMT  
		Size: 73.2 MB (73246091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04d0bde08b2985e08fdc234ae956e2e0f27467a33587f3839ea254efbe5994`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:latest` - unknown; unknown

```console
$ docker pull cassandra@sha256:bc53591663540e59f08265b3cba7ca308665739b67cc8894f99e1e2d18e842fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3032402c5ce8f256f682211dd3523c5c5f4d5426a95d00f8fa2ff3ec21da596e`

```dockerfile
```

-	Layers:
	-	`sha256:af9dc185b7d7bcb150463d8ea1356f172fd3ad556c9e586a3ea002108b71cb3a`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
		Size: 3.3 MB (3310428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3a4a51c8e403101493ef7808845d178b4fe6f7abfe09ebabc88d0f1bfe0ba`  
		Last Modified: Tue, 17 Feb 2026 23:24:58 GMT  
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
