## `tomcat:jdk14-openjdk-buster`

```console
$ docker pull tomcat@sha256:7b5a8a206dcd0e39b3a606ca24248b48354aead214a6d30da0c45dc0ec487dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomcat:jdk14-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:2ebfc4f0b110d5147ab59eabf3bf74dda2b9f51c828bd02f104f4aaa0293e1a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344409287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b782f03fe24e61ef8bc59f68e449387cb94de2d69a1f00e2a41c0580496cb5d2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:31:31 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:32:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Tue, 31 Mar 2020 21:32:43 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:32:44 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:32:44 GMT
ENV JAVA_VERSION=14
# Tue, 31 Mar 2020 21:32:45 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14/076bab302c7b4508975440c56f6cc26a/36/GPL/openjdk-14_linux-x64_bin.tar.gz
# Tue, 31 Mar 2020 21:32:45 GMT
ENV JAVA_SHA256=c7006154dfb8b66328c6475447a396feb0042608ee07a96956547f574a911c09
# Tue, 31 Mar 2020 21:33:23 GMT
RUN set -eux; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Tue, 31 Mar 2020 21:33:23 GMT
CMD ["jshell"]
# Wed, 01 Apr 2020 08:43:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2020 08:43:23 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:43:24 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 01 Apr 2020 08:43:24 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2020 08:43:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2020 08:43:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2020 08:48:14 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 01 Apr 2020 08:48:14 GMT
ENV TOMCAT_MAJOR=8
# Thu, 09 Apr 2020 23:35:56 GMT
ENV TOMCAT_VERSION=8.5.54
# Thu, 09 Apr 2020 23:35:57 GMT
ENV TOMCAT_SHA512=dc3ba0183d1e6f6006e5430e91abbc0758bdb719efebea5809f7034c9a28c590a764d8fcf2528a27a98cb86531e94cd9dc5a92cdbcae36e808ced0e5f1c665b8
# Thu, 09 Apr 2020 23:36:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Thu, 09 Apr 2020 23:36:23 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 09 Apr 2020 23:36:23 GMT
EXPOSE 8080
# Thu, 09 Apr 2020 23:36:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bdaf2f151ec945dbcaf0355685f51dfefdcdf882b30fc65259d4b30b410184`  
		Last Modified: Tue, 31 Mar 2020 21:35:43 GMT  
		Size: 13.9 MB (13920151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0ae0909e9495ba00fbfaa0824535d0415b80b3bd0afbdb499ae8adf41eada5`  
		Last Modified: Tue, 31 Mar 2020 21:36:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb2901a0a42480c29ba218b6370439f0e9df7769770902a7296ed147903d06a`  
		Last Modified: Tue, 31 Mar 2020 21:36:31 GMT  
		Size: 199.2 MB (199172786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba405cb9584da768bfcc44ac5c87e520a7b66fbdc9f1e40b7d73a23f2331b40`  
		Last Modified: Wed, 01 Apr 2020 08:54:29 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb93454607a55c6dbb73ac590c2af290af90b0522218ca5e25c0bd1db394eb58`  
		Last Modified: Thu, 09 Apr 2020 23:49:00 GMT  
		Size: 11.3 MB (11335066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fa5535feb4a06093868e16c016bf8be885f925719862db71a382f4e69eac89`  
		Last Modified: Thu, 09 Apr 2020 23:48:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
