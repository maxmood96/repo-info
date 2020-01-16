## `tomcat:9-jdk11-corretto`

```console
$ docker pull tomcat@sha256:b6820baedb9afd121a9567e92aedae47bde8b6818b85781eeb0cee4cacbbd1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:48489023cc7a4e2ee7ddfe1252118aa3d69bea2c241e24cd04575b36842ff0d0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273864932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048774332db964dbdae8a4cffad0b48c47c1872eebfa0fe08342a08b767b0c1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:19:53 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:19:53 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:53 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:19:54 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:19:54 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:54 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:20:15 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:20:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 15 Jan 2020 21:41:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Jan 2020 21:41:39 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 21:41:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 15 Jan 2020 21:41:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Jan 2020 21:41:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 21:41:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 21:41:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 15 Jan 2020 21:41:40 GMT
ENV TOMCAT_MAJOR=9
# Wed, 15 Jan 2020 21:41:41 GMT
ENV TOMCAT_VERSION=9.0.30
# Wed, 15 Jan 2020 21:41:41 GMT
ENV TOMCAT_SHA512=40bf428a534816317e5e8732b679e6d73f6ed977aab4ac5e2b9eaf1eb087eaa68a18b0fd3da8c39ca4b96f5b6fd919dec84517abba0d5e797285ade934a92990
# Wed, 15 Jan 2020 21:43:26 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Wed, 15 Jan 2020 21:43:28 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Jan 2020 21:43:29 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 21:43:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6433498f093ea7337102f34b01b34fd62fc0e53fa3bfbcdf13dab58f1b6cbb4`  
		Last Modified: Wed, 15 Jan 2020 21:21:13 GMT  
		Size: 197.5 MB (197495610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8957328713ee94a0e29f29a9e83956748b7249d6fe0c3de3c1ec271045ce4d22`  
		Last Modified: Wed, 15 Jan 2020 21:53:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9b6da80b1a3fef50e66ff78eb1c33efa7a1485adff69edbb3e25eca037aec`  
		Last Modified: Wed, 15 Jan 2020 21:53:34 GMT  
		Size: 14.8 MB (14816196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4c6339107844ffef4e95a06e3e3d371748dd74c21a0bc5d139b2e1872b0d6d`  
		Last Modified: Wed, 15 Jan 2020 21:53:33 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:05c1105d7c361c40f8fd983ba51bf46fba05fd32e5c7d67240ff985ae9f0f67b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273339075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c467fbcf41ea9e9bd220af3c43844b5f1c13b45fb5f71fb148020565a1b96b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:40:10 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:40:10 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:11 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:12 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:40:12 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:13 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:40 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:40:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 15 Jan 2020 22:04:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Jan 2020 22:04:02 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 22:04:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 15 Jan 2020 22:04:04 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Jan 2020 22:04:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 22:04:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Jan 2020 22:04:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 15 Jan 2020 22:04:07 GMT
ENV TOMCAT_MAJOR=9
# Wed, 15 Jan 2020 22:04:07 GMT
ENV TOMCAT_VERSION=9.0.30
# Wed, 15 Jan 2020 22:04:08 GMT
ENV TOMCAT_SHA512=40bf428a534816317e5e8732b679e6d73f6ed977aab4ac5e2b9eaf1eb087eaa68a18b0fd3da8c39ca4b96f5b6fd919dec84517abba0d5e797285ade934a92990
# Wed, 15 Jan 2020 22:05:24 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Wed, 15 Jan 2020 22:05:28 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Jan 2020 22:05:29 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 22:05:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da2db97f6fae3dad031512af96b94e04f8f044e961aa09b35cc5b70c1db57b`  
		Last Modified: Wed, 15 Jan 2020 21:42:02 GMT  
		Size: 195.7 MB (195747087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a546038bde61aa5614d69244c8b28bdc28f23d4c2e0fe229b079507cc7b422f6`  
		Last Modified: Wed, 15 Jan 2020 22:15:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affbdd6949cf77221f9863e71353b00f0d7b21fb0cb7a374a830716a854090e9`  
		Last Modified: Wed, 15 Jan 2020 22:15:18 GMT  
		Size: 14.8 MB (14794916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514285286574e4c7b65c2d06078b359b9927e9c876207e8d83cb36fd876fc2aa`  
		Last Modified: Wed, 15 Jan 2020 22:15:15 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
