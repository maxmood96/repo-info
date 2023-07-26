## `cassandra:latest`

```console
$ docker pull cassandra@sha256:2d5be53f58a8f26d64aa221f8991f8fbc1856655a0aea989ee2da7a53d370941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `cassandra:latest` - linux; amd64

```console
$ docker pull cassandra@sha256:96ec7506e490ed654e2ac1de0f69b863528586adcf5dfbb7bd8c59597900f206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156256372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d92574273714bf8129ccbd4c0a8b0022ec6e82771776260252c44e78af41c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:34:45 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 12:29:48 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 05 Jul 2023 12:30:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 05 Jul 2023 12:30:03 GMT
ENV GOSU_VERSION=1.16
# Wed, 05 Jul 2023 12:30:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Jul 2023 12:30:18 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 05 Jul 2023 12:30:18 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 05 Jul 2023 12:30:18 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 12:30:18 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 05 Jul 2023 12:30:19 GMT
ENV CASSANDRA_VERSION=4.1.2
# Wed, 05 Jul 2023 12:30:19 GMT
ENV CASSANDRA_SHA512=e6ba9efc46743547130cbcd0e174d6761e442f97b17732df8f15d25c9dcf5eaf009e0ac550aad3e34e5f8fc1b300062ad248def3ca85ef372d20d745698f01f9
# Wed, 05 Jul 2023 12:30:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 05 Jul 2023 12:30:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 05 Jul 2023 12:30:39 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 05 Jul 2023 12:30:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 12:30:39 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 05 Jul 2023 12:30:39 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5a95d495e73dfab77c2563516938a7f1fac0cba3871cc473b28cb12c993db5`  
		Last Modified: Tue, 04 Jul 2023 20:40:47 GMT  
		Size: 46.7 MB (46664989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413534cbbb8239054e674b789c9b54fb3923af44d6d276c9edc0de956e4ff388`  
		Last Modified: Tue, 04 Jul 2023 20:40:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e5dc3c54c15580159f35514ad78190c231a986e4007f0dfec66d09fd547079`  
		Last Modified: Wed, 05 Jul 2023 12:32:33 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d44a842e736cddaee786b328fbc860691e54debc39828e982dfa11616967b2`  
		Last Modified: Wed, 05 Jul 2023 12:32:35 GMT  
		Size: 11.0 MB (10952178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8b19243de1e1d04d71bf52e3f1c68ce7d0e6c629809fa2347c09b2bd59ec0f`  
		Last Modified: Wed, 05 Jul 2023 12:32:33 GMT  
		Size: 1.3 MB (1338356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa7445414fd5a8e3aa0d79d5a5fabecb50659a7d6aec5ba924c0089b2013ef9`  
		Last Modified: Wed, 05 Jul 2023 12:32:36 GMT  
		Size: 52.3 MB (52304234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1b2aeeb332d8e286577bc83bc6b39b898203b4de5f08197c553f506662d47`  
		Last Modified: Wed, 05 Jul 2023 12:32:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:fb816f5aff60b7451717a019c598f21f4664681477cb7bac7a10ff9432927538
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148567345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30372357f80fc46ec5bacf4f12f95418737f38091ae354ece59db14db9e064a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:08:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:08:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:08:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:09:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:58:52 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 25 Jul 2023 23:59:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 23:59:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:29:08 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 26 Jul 2023 00:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 26 Jul 2023 00:29:25 GMT
ENV GOSU_VERSION=1.16
# Wed, 26 Jul 2023 00:29:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Jul 2023 00:29:33 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 26 Jul 2023 00:29:33 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 26 Jul 2023 00:29:33 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:29:33 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 26 Jul 2023 00:29:33 GMT
ENV CASSANDRA_VERSION=4.1.2
# Wed, 26 Jul 2023 00:29:33 GMT
ENV CASSANDRA_SHA512=e6ba9efc46743547130cbcd0e174d6761e442f97b17732df8f15d25c9dcf5eaf009e0ac550aad3e34e5f8fc1b300062ad248def3ca85ef372d20d745698f01f9
# Wed, 26 Jul 2023 00:29:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 26 Jul 2023 00:29:59 GMT
VOLUME [/var/lib/cassandra]
# Wed, 26 Jul 2023 00:29:59 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 26 Jul 2023 00:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:29:59 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 26 Jul 2023 00:29:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0186b47b0f035fc3bcf39b19dfd039f6fa8694a7e17ba90a3fc477b5753c106`  
		Last Modified: Tue, 04 Jul 2023 20:13:22 GMT  
		Size: 15.2 MB (15239799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67ea8133961e376908b592e0e5e4406be885407b6e73ceddda0e6ed831e5f1f`  
		Last Modified: Wed, 26 Jul 2023 00:01:25 GMT  
		Size: 45.0 MB (45013349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3603d4068f02f433f43e44c09db2f1355703933e9d6784745bb0e9cb44b22cfd`  
		Last Modified: Wed, 26 Jul 2023 00:01:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08101371d1ab180e2a51a988a4c315271b49e3023d9f2541bd600dee975077ff`  
		Last Modified: Wed, 26 Jul 2023 00:30:40 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5c4912a17991b7edc5592c2bfd2b55e335a1580a9444c352a2d423031f6706`  
		Last Modified: Wed, 26 Jul 2023 00:30:42 GMT  
		Size: 10.1 MB (10112715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de44dd98a934a8e5469165a118a84cb3297ddb038db66a90c0f6a35b1acc1fa`  
		Last Modified: Wed, 26 Jul 2023 00:30:40 GMT  
		Size: 1.3 MB (1305814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936c73c14b5bc3e7d7c09e68e9cc41b9e7363d10bcfa5e5e508f27bd533ed333`  
		Last Modified: Wed, 26 Jul 2023 00:30:44 GMT  
		Size: 52.3 MB (52304402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef461b25408344c5121efcc69e2b53ea579c62cb75d9d72eca62d2a2a38b7d1`  
		Last Modified: Wed, 26 Jul 2023 00:30:40 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:14298d24243db6143970228a25acf3c7fd3f3f3a59e09ad1b58defbf1cad5742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153062847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd511cbdedcfb309813f6f3f22598d070dc8b477ce07a88b48756d3ccb3bbabc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:25 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 03:53:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 05 Jul 2023 03:53:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 05 Jul 2023 03:53:42 GMT
ENV GOSU_VERSION=1.16
# Wed, 05 Jul 2023 03:53:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Jul 2023 03:53:51 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 05 Jul 2023 03:53:51 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 05 Jul 2023 03:53:51 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:53:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 05 Jul 2023 03:53:51 GMT
ENV CASSANDRA_VERSION=4.1.2
# Wed, 05 Jul 2023 03:53:51 GMT
ENV CASSANDRA_SHA512=e6ba9efc46743547130cbcd0e174d6761e442f97b17732df8f15d25c9dcf5eaf009e0ac550aad3e34e5f8fc1b300062ad248def3ca85ef372d20d745698f01f9
# Wed, 05 Jul 2023 03:54:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 05 Jul 2023 03:54:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 05 Jul 2023 03:54:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 05 Jul 2023 03:54:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 03:54:07 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 05 Jul 2023 03:54:07 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e136d60ae492f8f26e56be7dccc8e38df93e1fadd1cedf3c019bf3adc2bf6bda`  
		Last Modified: Tue, 04 Jul 2023 15:38:24 GMT  
		Size: 45.0 MB (45009918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae0a81a63f732c9b0d4c93e38f8eac3e6ef26be7f98c628240fd5d7c86d09f8`  
		Last Modified: Tue, 04 Jul 2023 15:38:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8770b09705ec26e1039fdba472837ade4b3e3a0bd6adbd07c8e6223ff7027`  
		Last Modified: Wed, 05 Jul 2023 03:55:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a394c7663656484ad9a9262b745ae8e7c2b9dee03749ac17f4e652d35072c08e`  
		Last Modified: Wed, 05 Jul 2023 03:55:44 GMT  
		Size: 11.0 MB (11007055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df84f36d690fbdd71ad557a3186e0e343931211fe54064e97485c09dd8c48005`  
		Last Modified: Wed, 05 Jul 2023 03:55:42 GMT  
		Size: 1.3 MB (1271507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ee1a632dd0c318877b4f74a8f09bab4380a152815f4e13b0d138486c5b41`  
		Last Modified: Wed, 05 Jul 2023 03:55:45 GMT  
		Size: 52.3 MB (52304743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42e899616c43b196471a50be823c672340d36a4f89ab428b8797673bc7a456`  
		Last Modified: Wed, 05 Jul 2023 03:55:42 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:2eaca688289f2c1b34858880fe9039e4acb34401a20cec2aaa092155d7c49c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158785140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377dcb289737806208c09c1cc22896f07f613ef07a3ac0721e65ae53c04d191d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 28 Jun 2023 10:04:43 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:04:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:04:46 GMT
ADD file:df651ead0b69eb261098e765354dbdf5ffca51275c037d8881fedcaa1c91c36d in / 
# Wed, 28 Jun 2023 10:04:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 00:16:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 00:16:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 00:16:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jul 2023 00:17:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:16:55 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:19:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:41:38 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 26 Jul 2023 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 26 Jul 2023 00:42:11 GMT
ENV GOSU_VERSION=1.16
# Wed, 26 Jul 2023 00:42:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Jul 2023 00:42:40 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 26 Jul 2023 00:42:41 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 26 Jul 2023 00:42:41 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:42:42 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 26 Jul 2023 00:42:42 GMT
ENV CASSANDRA_VERSION=4.1.2
# Wed, 26 Jul 2023 00:42:43 GMT
ENV CASSANDRA_SHA512=e6ba9efc46743547130cbcd0e174d6761e442f97b17732df8f15d25c9dcf5eaf009e0ac550aad3e34e5f8fc1b300062ad248def3ca85ef372d20d745698f01f9
# Wed, 26 Jul 2023 00:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 26 Jul 2023 00:43:22 GMT
VOLUME [/var/lib/cassandra]
# Wed, 26 Jul 2023 00:43:22 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 26 Jul 2023 00:43:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:43:23 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 26 Jul 2023 00:43:24 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:4e95615eadb7a0d90a47ca15a5c0693371494902f54d8d78a50d53e89e7a20de`  
		Last Modified: Tue, 04 Jul 2023 04:40:49 GMT  
		Size: 33.3 MB (33308759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900a3bee385ed74b6117be4963259e4ef65f261ee58fc971b7206f32acb0572b`  
		Last Modified: Wed, 05 Jul 2023 00:27:54 GMT  
		Size: 17.6 MB (17648843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ce872eb087bec481ffba60ffc2738f5138ba53cc674dfc8992faca452191a8`  
		Last Modified: Wed, 26 Jul 2023 00:24:25 GMT  
		Size: 42.3 MB (42295625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd43dd9923257943d8313f3158968681c195786df3b219223e87011dfa37a092`  
		Last Modified: Wed, 26 Jul 2023 00:24:16 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb154bfcb33ed0095f87ba1feadf0674613ffc2710f7d3af9679638424a3574`  
		Last Modified: Wed, 26 Jul 2023 00:44:29 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52b234363dd6ea8b8b94cffd92b054d08bdb23bbc9a4d4f3c0fbb8e4c243437`  
		Last Modified: Wed, 26 Jul 2023 00:44:32 GMT  
		Size: 12.0 MB (11963796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d98fc3f1605a4b4918438bc171516031d49247a78fb9b60f7d8a1977cea12f`  
		Last Modified: Wed, 26 Jul 2023 00:44:30 GMT  
		Size: 1.3 MB (1260030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6ef892f0a753c08b6416f478d7f0e5302b20761acc5d41d04dfc60088a5b71`  
		Last Modified: Wed, 26 Jul 2023 00:44:34 GMT  
		Size: 52.3 MB (52304949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7a4d6401aa191656216fcd29343efcb9ca80c178e7c4e01320f21651ca8882`  
		Last Modified: Wed, 26 Jul 2023 00:44:29 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; s390x

```console
$ docker pull cassandra@sha256:e65eb59d37bca92d777fcf4ede7d81e8e5e1b024e134d95a8312ecc33b05800c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148056244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822afb132a0620478bd2d1506c25f7c80ff078eaacb139aaca400c22f9bea063`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 28 Jun 2023 10:01:13 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:01:14 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:01:15 GMT
ADD file:777fd71e798b91bf768b21e1ca4403f388db9936ef55ef68b4b019cb167fa707 in / 
# Wed, 28 Jun 2023 10:01:15 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:23:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 16:23:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 16:23:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 16:23:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:23:53 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 16:25:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 16:25:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 11:01:54 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 05 Jul 2023 11:02:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 05 Jul 2023 11:02:06 GMT
ENV GOSU_VERSION=1.16
# Wed, 05 Jul 2023 11:02:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Jul 2023 11:02:18 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 05 Jul 2023 11:02:18 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 05 Jul 2023 11:02:19 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:02:19 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55 	7464AAD9068241C50BA6A26232F35CB2F546D93E 	CEC5C50B9C629EF0F5AB2706650B72EB14CCD622
# Wed, 05 Jul 2023 11:02:19 GMT
ENV CASSANDRA_VERSION=4.1.2
# Wed, 05 Jul 2023 11:02:19 GMT
ENV CASSANDRA_SHA512=e6ba9efc46743547130cbcd0e174d6761e442f97b17732df8f15d25c9dcf5eaf009e0ac550aad3e34e5f8fc1b300062ad248def3ca85ef372d20d745698f01f9
# Wed, 05 Jul 2023 11:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm-server.options"; 			sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm-server.options"; 			grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm-server.options"; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 1777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 05 Jul 2023 11:02:35 GMT
VOLUME [/var/lib/cassandra]
# Wed, 05 Jul 2023 11:02:35 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 05 Jul 2023 11:02:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 11:02:35 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 05 Jul 2023 11:02:35 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:f5ebe8481b30a6d3b710b0efdec29843cca805811e3be1a4e375761725c40e5a`  
		Last Modified: Tue, 04 Jul 2023 13:07:41 GMT  
		Size: 27.0 MB (27013645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3533c99e551f88519f4e20865cc3f7f85d6c5a6083a720282116b19596c7043`  
		Last Modified: Tue, 04 Jul 2023 16:28:03 GMT  
		Size: 16.1 MB (16103623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abecfabd626e6f2244b9acbc421a0e8c5e3038f88921dad4af3d6f6a1e7e3fe`  
		Last Modified: Tue, 04 Jul 2023 16:28:45 GMT  
		Size: 40.5 MB (40540253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0381561ef75cfc398ff010e48309dce70fab3d2854d3522c49e42f5c616682c`  
		Last Modified: Tue, 04 Jul 2023 16:28:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5645d63cd607f8fa1bc16cd5fa4ffc5e303667242f80b2ce4306ef278a7f83`  
		Last Modified: Wed, 05 Jul 2023 11:03:13 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38afd2ac03505b7b38d6e76b4b757758ea9df325a2cc1fbf11da4f91bd8a65f`  
		Last Modified: Wed, 05 Jul 2023 11:03:14 GMT  
		Size: 10.8 MB (10785151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bba04fdb10b8dca96fb52394fe959b7e05e98fe3ff928a157edd1469961d0e`  
		Last Modified: Wed, 05 Jul 2023 11:03:13 GMT  
		Size: 1.3 MB (1305732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885a41ad86128172a501956330b2cd8c712e4fbb2e39f26b6addb1e25c6c51ee`  
		Last Modified: Wed, 05 Jul 2023 11:03:15 GMT  
		Size: 52.3 MB (52304700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d8398aa4ce71fcf11b20c326a10086e1773ece1aed0e358b9bd2f7081ce4c6`  
		Last Modified: Wed, 05 Jul 2023 11:03:13 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
