## `cassandra:5-bookworm`

```console
$ docker pull cassandra@sha256:6370140cb5de7d10c97e3abb163b13cc2ae0920a6d58719b8c1d483f5129185b
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
$ docker pull cassandra@sha256:ac10bc94b076a42c0bca9c089907ad83863dd8d49c9cce517e40958c673a81fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168858647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df528166c2fa0b6adcffa271e5afbe136cf8e8d2f9bcf2dd6a8ebda08265a009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 21:59:59 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 15 Apr 2026 22:00:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 15 Apr 2026 22:00:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 22:00:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:00:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:00:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:00:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:16 GMT
RUN java --version # buildkit
# Wed, 15 Apr 2026 22:00:16 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 15 Apr 2026 22:00:16 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 15 Apr 2026 22:00:16 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:16 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 15 Apr 2026 22:00:16 GMT
ENV CASSANDRA_VERSION=5.0.7
# Wed, 15 Apr 2026 22:00:16 GMT
ENV CASSANDRA_SHA512=7a36805a87adacd1c897dabf81e5c7007334936ae200340504474e09eb0800c0a7ff5f8c7778fd19a96a93b1b3f5844aff5644e55cd33928b358fea53159c2c9
# Wed, 15 Apr 2026 22:00:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 15 Apr 2026 22:00:33 GMT
VOLUME [/var/lib/cassandra]
# Wed, 15 Apr 2026 22:00:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:00:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:00:33 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 15 Apr 2026 22:00:33 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b197b19e345b89266229acf7b40d0332157be4aae7859aef73de39e6a591f4d9`  
		Last Modified: Wed, 15 Apr 2026 22:00:54 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e5abb87d496a9ba63e29588034efdb3cd240dbb8bb20b09fbcd4733592a9a8`  
		Last Modified: Wed, 15 Apr 2026 22:00:55 GMT  
		Size: 18.2 MB (18150211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fd8eb8e49957e9352cce0a5334f02ebf3cebd586568a1e7cf48dd2cc56627f`  
		Last Modified: Wed, 15 Apr 2026 22:00:54 GMT  
		Size: 1.3 MB (1266590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f64c611b598ef95eab4433db3a1d0f24fec96f9949d55258593b6c03d3d4f4`  
		Last Modified: Wed, 15 Apr 2026 22:00:57 GMT  
		Size: 47.4 MB (47429848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fead93d2b13aa0894edb2bf25be3ce9a8c131c6e46fa1190eb6710e009a01c5`  
		Last Modified: Wed, 15 Apr 2026 22:00:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a468db1b25ee494b686fca03349f09fc673f8059829e16177013eac400d4be80`  
		Last Modified: Wed, 15 Apr 2026 22:00:59 GMT  
		Size: 73.8 MB (73773204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3c8d695067fdd4dc4c26f238543c517ddbd3aca8dd12d7ffeeace70a6d3e1b`  
		Last Modified: Wed, 15 Apr 2026 22:01:00 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:dd8996de2acd75e3800d666c372e19752645ff1190b42f7d26ad091f5f04f7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2267ddc7fc2b5807a10bd2b75ad5f3d6796501b8124e03f42304b28b1dc704`

```dockerfile
```

-	Layers:
	-	`sha256:ac9a802af8ec4238f6a6e97d70c339644cb7bea0c6aaba24787f9ec38dee5fe8`  
		Last Modified: Wed, 15 Apr 2026 22:00:46 GMT  
		Size: 3.3 MB (3306163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817cc6a35bb6ec2f939e028dad1ce487aba96c8a9f73916553409a3d48ba273f`  
		Last Modified: Wed, 15 Apr 2026 22:00:46 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:cfc3965ca7d4f825c6b2db7781d8124409ed93b6abd3ec24333054dabdd34329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160196592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667bfe4f16c41c6ce685631ed9109c7c71334345e6a13002920f5cdef1137dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 21:40:22 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 15 Apr 2026 21:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 15 Apr 2026 21:40:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 21:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:40:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:40:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 21:40:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:40:43 GMT
RUN java --version # buildkit
# Wed, 15 Apr 2026 21:40:43 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 15 Apr 2026 21:40:43 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 15 Apr 2026 21:40:43 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:40:43 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 15 Apr 2026 21:40:43 GMT
ENV CASSANDRA_VERSION=5.0.7
# Wed, 15 Apr 2026 21:40:43 GMT
ENV CASSANDRA_SHA512=7a36805a87adacd1c897dabf81e5c7007334936ae200340504474e09eb0800c0a7ff5f8c7778fd19a96a93b1b3f5844aff5644e55cd33928b358fea53159c2c9
# Wed, 15 Apr 2026 21:41:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 15 Apr 2026 21:41:04 GMT
VOLUME [/var/lib/cassandra]
# Wed, 15 Apr 2026 21:41:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:41:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:41:04 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 15 Apr 2026 21:41:04 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8979def684332fdd7418a2c0c663c054b2226e18dd912f6bb1b433347e2d149`  
		Last Modified: Wed, 15 Apr 2026 21:41:17 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9514216a828d5e36e70cdfe6d0cc96066ce222c29a2ae88c8cfed4d1600b3e99`  
		Last Modified: Wed, 15 Apr 2026 21:41:17 GMT  
		Size: 16.2 MB (16209540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8a2692639446dffc8ad017f7d50f922931250727538b3be583ecd700c42735`  
		Last Modified: Wed, 15 Apr 2026 21:41:17 GMT  
		Size: 1.2 MB (1232583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cbe33ccca3a9618d6d750417cd2720e0eddf105629f091c5b19234a7a948af`  
		Last Modified: Wed, 15 Apr 2026 21:41:18 GMT  
		Size: 45.0 MB (45037289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340d4a0a4bf9ab33562e410486d6e8267106daa77445d40b792e07ef23117186`  
		Last Modified: Wed, 15 Apr 2026 21:41:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5665a52769ea36ee6763ff0cf40ad63e29f2b8d0575d47d6d6d493c51ed4b4`  
		Last Modified: Wed, 15 Apr 2026 21:41:20 GMT  
		Size: 73.8 MB (73773257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debf2b59b048da5bb1d2b7abd55a2215a0af8ad93fc78b277d7a88af08ac7ff2`  
		Last Modified: Wed, 15 Apr 2026 21:41:19 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:086d260d9f2b022da4578251d8a0a5d43bf6a28ffdc14fd96b4c43385e46640b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227a4e36f03df20b33cc4ec8c16e8d007947b8fec55aa023ecbaf27ebf439bfd`

```dockerfile
```

-	Layers:
	-	`sha256:cb9ca97e47230c3b290a0c6dbd6588a3a702358c22631a111162cf306ec783bf`  
		Last Modified: Wed, 15 Apr 2026 21:41:17 GMT  
		Size: 3.3 MB (3308646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a70a7784c8e739781745610c30015700046993a134386977ce6de423041bdb01`  
		Last Modified: Wed, 15 Apr 2026 21:41:16 GMT  
		Size: 37.1 KB (37114 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:2ea4c6c767a3bf99fb22af17aca31013532d4e0fe5c0c7b149605f9b55021b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167913182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed15e85755aadf3456309b6a64105e588f0c3aa7f16c9ea96ea6696044772a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:12:01 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Wed, 15 Apr 2026 22:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Wed, 15 Apr 2026 22:12:17 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 22:12:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:12:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:18 GMT
RUN java --version # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 15 Apr 2026 22:12:18 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 15 Apr 2026 22:12:18 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:18 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 15 Apr 2026 22:12:18 GMT
ENV CASSANDRA_VERSION=5.0.7
# Wed, 15 Apr 2026 22:12:18 GMT
ENV CASSANDRA_SHA512=7a36805a87adacd1c897dabf81e5c7007334936ae200340504474e09eb0800c0a7ff5f8c7778fd19a96a93b1b3f5844aff5644e55cd33928b358fea53159c2c9
# Wed, 15 Apr 2026 22:12:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Wed, 15 Apr 2026 22:12:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 15 Apr 2026 22:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:35 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Wed, 15 Apr 2026 22:12:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80166d9df6f943d978fb9c113ddb9bebff73c44408d826d2da23b9b79b231c6`  
		Last Modified: Wed, 15 Apr 2026 22:12:48 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c46f6def0bdab3f8af52f62eac0691d6e93ea559bf080e6f9cae39b8c78343`  
		Last Modified: Wed, 15 Apr 2026 22:12:49 GMT  
		Size: 17.9 MB (17890807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b296b04dbd91640876a2f77f1ce22090af74d744882ed4dea2efb43dd22b95a0`  
		Last Modified: Wed, 15 Apr 2026 22:12:49 GMT  
		Size: 1.2 MB (1220117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca715013c7f0f2cc5a00ec00b2a750c7dd614114562b7aa191e79547f476975`  
		Last Modified: Wed, 15 Apr 2026 22:12:50 GMT  
		Size: 46.9 MB (46910248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ec46dd2cb12d6fa1260b22184d4d8bc5744541c7e671d0c2d14054f7951b43`  
		Last Modified: Wed, 15 Apr 2026 22:12:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efffbf2e2894fe4f437fb5c02b8f2fb7805120295da95239dccb4195981126b`  
		Last Modified: Wed, 15 Apr 2026 22:12:52 GMT  
		Size: 73.8 MB (73773383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6303f180414b61da2ed687095320e68b6ce8011d81b75baeadbe4f36a6b4073`  
		Last Modified: Wed, 15 Apr 2026 22:12:51 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:714836e645e16be0f8e99f34566385fb69a2e995d08366c896d3fbcfce68fb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3de873332e9a0705a16bde3f518efbdb2b570d7592008a9bfd7d5161ea0e19b`

```dockerfile
```

-	Layers:
	-	`sha256:18044d67119f3cea38caa97c796b624a888831dee3826a8bb681e1cc31e9a395`  
		Last Modified: Wed, 15 Apr 2026 22:12:49 GMT  
		Size: 3.3 MB (3305928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcdb5ba5c408b2f9616ef434c8195d2a33fdb78ceb33937ccdacc48fee0c5419`  
		Last Modified: Wed, 15 Apr 2026 22:12:49 GMT  
		Size: 37.2 KB (37166 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; ppc64le

```console
$ docker pull cassandra@sha256:a0a4c9b21ad9a879eb79c856208f15ee731964a2bda12da405ab9d24dde12135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173902406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3225d7ed5a6ca35e4f178fc40c712e7b03bc74fb55f2a7078a280d3ee613efed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:27:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 16 Apr 2026 02:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 16 Apr 2026 02:27:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 16 Apr 2026 02:27:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:27:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:27:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:27:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:27:58 GMT
RUN java --version # buildkit
# Thu, 16 Apr 2026 02:27:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 16 Apr 2026 02:27:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 16 Apr 2026 02:27:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:27:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 16 Apr 2026 02:27:58 GMT
ENV CASSANDRA_VERSION=5.0.7
# Thu, 16 Apr 2026 02:27:58 GMT
ENV CASSANDRA_SHA512=7a36805a87adacd1c897dabf81e5c7007334936ae200340504474e09eb0800c0a7ff5f8c7778fd19a96a93b1b3f5844aff5644e55cd33928b358fea53159c2c9
# Thu, 16 Apr 2026 02:28:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 16 Apr 2026 02:28:38 GMT
VOLUME [/var/lib/cassandra]
# Thu, 16 Apr 2026 02:28:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 02:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:28:38 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 16 Apr 2026 02:28:38 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05af3d50f921e24b45c85137412e9367dfd225b791864cd3378c62a2e1346cbb`  
		Last Modified: Thu, 16 Apr 2026 02:29:06 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a8d99b89a341653c18fda52195541d030eddd896d00383789b6cbbfa043d8b`  
		Last Modified: Thu, 16 Apr 2026 02:29:07 GMT  
		Size: 19.5 MB (19494817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29695fe461205238e5e3e283e80a4548002ef6731461e29b683bd438515e87f2`  
		Last Modified: Thu, 16 Apr 2026 02:29:06 GMT  
		Size: 1.2 MB (1225545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1a3648a31d3089315a969905235cc0e140d6f025482c3c480df060e88d0d03`  
		Last Modified: Thu, 16 Apr 2026 02:29:09 GMT  
		Size: 47.3 MB (47327563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c46a9af9f9efd7ee8dfabebfb77538367156c4421426c077d9511853420f67`  
		Last Modified: Thu, 16 Apr 2026 02:29:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a6ba77794de35196d402f088ef4888ead527d70f58da13025e68e70cd722d6`  
		Last Modified: Thu, 16 Apr 2026 02:29:11 GMT  
		Size: 73.8 MB (73773553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9ae3d70e690fa98b4aadce6c06b4d2e7b4fa9943a93e6b3adb15e97c7626c1`  
		Last Modified: Thu, 16 Apr 2026 02:29:09 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:fbe75c70c98154b8af47d32b37ebc403244186b43fd03a752471505223e54fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6e80043d8cb5e2cd99b19205d668f535f261217edde5e644894b0ee91d1d5a`

```dockerfile
```

-	Layers:
	-	`sha256:591a3371ea20ad1f0ba47cabdb428dc6a85ad72ae45d19abb697d9ee5ffff814`  
		Last Modified: Thu, 16 Apr 2026 02:29:08 GMT  
		Size: 3.3 MB (3310429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dffc888e3c44b888b18b78d14da2ac840269dd71349cc26e6809f7830bd754df`  
		Last Modified: Thu, 16 Apr 2026 02:29:07 GMT  
		Size: 37.0 KB (37014 bytes)  
		MIME: application/vnd.in-toto+json

### `cassandra:5-bookworm` - linux; s390x

```console
$ docker pull cassandra@sha256:1787276e2954e9d8f20e3fdb413c0a04476b573374eae37cd1bd28e7e721c799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163761523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5ad28319571faa27b5da464a8c9952c4751a2e4d03c42fb6e91bc63ea93056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:33:37 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra # buildkit
# Thu, 16 Apr 2026 00:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig # buildkit
# Thu, 16 Apr 2026 00:33:57 GMT
ENV GOSU_VERSION=1.19
# Thu, 16 Apr 2026 00:33:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:33:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:33:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:33:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:33:58 GMT
RUN java --version # buildkit
# Thu, 16 Apr 2026 00:33:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Thu, 16 Apr 2026 00:33:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Thu, 16 Apr 2026 00:33:58 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:33:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Thu, 16 Apr 2026 00:33:58 GMT
ENV CASSANDRA_VERSION=5.0.7
# Thu, 16 Apr 2026 00:33:58 GMT
ENV CASSANDRA_SHA512=7a36805a87adacd1c897dabf81e5c7007334936ae200340504474e09eb0800c0a7ff5f8c7778fd19a96a93b1b3f5844aff5644e55cd33928b358fea53159c2c9
# Thu, 16 Apr 2026 00:34:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v # buildkit
# Thu, 16 Apr 2026 00:34:13 GMT
VOLUME [/var/lib/cassandra]
# Thu, 16 Apr 2026 00:34:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:34:13 GMT
EXPOSE map[7000/tcp:{} 7001/tcp:{} 7199/tcp:{} 9042/tcp:{} 9160/tcp:{}]
# Thu, 16 Apr 2026 00:34:13 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670dd8c620cbcf0a2a3327d255b28d20ac62076a7a50ec9cbefefea7a35ce39`  
		Last Modified: Thu, 16 Apr 2026 00:34:33 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cd73f59bc9734066ee06281ddfe74cad7ed0eef4a44454ec506ed216c67d8`  
		Last Modified: Thu, 16 Apr 2026 00:34:34 GMT  
		Size: 17.5 MB (17455220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde06729224de12579e8f2be7a4bcab01ebc271abf1ee5ad632f0b8614efc6ff`  
		Last Modified: Thu, 16 Apr 2026 00:34:33 GMT  
		Size: 1.2 MB (1240469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b4998455cd744038b823f2f3fed679c3d9163be5b2da32df60fe59765d7f35`  
		Last Modified: Thu, 16 Apr 2026 00:34:34 GMT  
		Size: 44.4 MB (44398464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f1c8004d215e3d3a1788d8ab2241a9bdb3e4b85926468b004c70e3c0d4860f`  
		Last Modified: Thu, 16 Apr 2026 00:34:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a393822bc232e58565a1d6968bf3a67e30582d393225722fd41073e8254e893`  
		Last Modified: Thu, 16 Apr 2026 00:34:36 GMT  
		Size: 73.8 MB (73773276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74dc30fb294666641537799898bba7010faa6a9f7bd9b3194a1841f99332ef6`  
		Last Modified: Thu, 16 Apr 2026 00:34:35 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cassandra:5-bookworm` - unknown; unknown

```console
$ docker pull cassandra@sha256:b8bf290d826dcbbf9710fb0467fc5315c1b14345ac53989d2ee2cd6b4ae899ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483a69bbec423f992854932df2585cfdcee4b67ca3a35e0c970c90deb7c6d868`

```dockerfile
```

-	Layers:
	-	`sha256:a24b3d368b6802e3c2ef865dcfe2b1fb89f142b4dcde03f3056d7b4d4b4887c1`  
		Last Modified: Thu, 16 Apr 2026 00:34:34 GMT  
		Size: 3.3 MB (3302299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176738b40d1d0fd27e3c1320362277fb52cb3111af0ca6656358deda9dbbd6b1`  
		Last Modified: Thu, 16 Apr 2026 00:34:33 GMT  
		Size: 36.9 KB (36928 bytes)  
		MIME: application/vnd.in-toto+json
