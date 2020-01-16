## `tomcat:7-jdk8-corretto`

```console
$ docker pull tomcat@sha256:8a8b4da6f43b5477e56ca8b52c28f5207741ff234bd25c8979d11c0d6cdc37fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:7-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:aa1a6f7fe1ef6d60dd12c2e6904226ed0b6e67ddc67f6bef11dbc94b9dd83aed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196507801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73bf34472a6c7702635e66e0da30ba34674ba9e5ff6266e8c0001b83086d68e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:19:29 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.x86_64.rpm
# Wed, 15 Jan 2020 21:19:29 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.07.1
# Wed, 15 Jan 2020 21:19:29 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:19:30 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.aarch64.rpm
# Wed, 15 Jan 2020 21:19:30 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.07.1
# Wed, 15 Jan 2020 21:19:30 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:19:49 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.07.1 path_x64=https://corretto.aws/downloads/resources/8.242.07.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:19:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Jan 2020 21:43:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Jan 2020 21:43:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 21:43:51 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 15 Jan 2020 21:43:51 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Jan 2020 21:43:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 21:43:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 21:49:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 15 Jan 2020 21:50:58 GMT
ENV TOMCAT_MAJOR=7
# Wed, 15 Jan 2020 21:50:58 GMT
ENV TOMCAT_VERSION=7.0.99
# Wed, 15 Jan 2020 21:50:59 GMT
ENV TOMCAT_SHA512=f53fb4fe6e568afe03fcf23043a3125b0c0ad99872146ff150a30333be92e6322b2278bfcfb2cce67112f09c3aa464086442bb8a79280548b179127ed1abbca9
# Wed, 15 Jan 2020 21:52:26 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Wed, 15 Jan 2020 21:52:28 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Jan 2020 21:52:28 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 21:52:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43c86e2643ba1d54bf4f74a4ab1c2686c086e902f9f976b70e853d7889c31d7`  
		Last Modified: Wed, 15 Jan 2020 21:20:48 GMT  
		Size: 121.6 MB (121599762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a334808f848024b90993b0526f2151945bcfb4fa8456067edae0a1447e5dfca`  
		Last Modified: Wed, 15 Jan 2020 21:53:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e571b56c7e3c7affe8c7bb8165ca410d6297b986ec9aada67c53ca310f6f70`  
		Last Modified: Wed, 15 Jan 2020 21:54:35 GMT  
		Size: 13.4 MB (13354915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218b960f81af68b8dd0fb10a675babaac1cd9c1c5d1bf2b9db03b0930a055188`  
		Last Modified: Wed, 15 Jan 2020 21:54:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b948b70e907a5e9dca26a207a3547a6fcb64a72b3a024390de2eed41ab94e333
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181115455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc18a5803cdea4abff6e49a5d2ad3ff289f40375481dd81155c7a8a085cebfb9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:39:35 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.x86_64.rpm
# Wed, 15 Jan 2020 21:39:36 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.07.1
# Wed, 15 Jan 2020 21:39:36 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:39:36 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.aarch64.rpm
# Wed, 15 Jan 2020 21:39:37 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.07.1
# Wed, 15 Jan 2020 21:39:38 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:03 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.07.1 path_x64=https://corretto.aws/downloads/resources/8.242.07.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b07-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Jan 2020 22:05:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Jan 2020 22:05:48 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 22:05:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 15 Jan 2020 22:05:53 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Jan 2020 22:05:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 22:05:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 22:11:22 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 15 Jan 2020 22:12:53 GMT
ENV TOMCAT_MAJOR=7
# Wed, 15 Jan 2020 22:12:53 GMT
ENV TOMCAT_VERSION=7.0.99
# Wed, 15 Jan 2020 22:12:54 GMT
ENV TOMCAT_SHA512=f53fb4fe6e568afe03fcf23043a3125b0c0ad99872146ff150a30333be92e6322b2278bfcfb2cce67112f09c3aa464086442bb8a79280548b179127ed1abbca9
# Wed, 15 Jan 2020 22:14:02 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Wed, 15 Jan 2020 22:14:06 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Jan 2020 22:14:06 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 22:14:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4fd7bb52402180644d7c853ea7a784233711c83c4cb6977f05816332905d63`  
		Last Modified: Wed, 15 Jan 2020 21:41:20 GMT  
		Size: 105.0 MB (104985396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c55ec3352778ead0e7c5239357e528b423ad4561bc2cf965b7a0fc86db01c95`  
		Last Modified: Wed, 15 Jan 2020 22:15:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b731be09baf1fc4697687ff042c1d5700c449e9804fcb3b97cf94b3b54ed60ec`  
		Last Modified: Wed, 15 Jan 2020 22:16:28 GMT  
		Size: 13.3 MB (13332989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f723d900e1b09aaf01cdb14beda9ce67e0f40f98c5e93cded83b18a79b0c9004`  
		Last Modified: Wed, 15 Jan 2020 22:16:25 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
