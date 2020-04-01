## `tomcat:8-jdk11-corretto`

```console
$ docker pull tomcat@sha256:fca7f7a031a4d248030842b7926bad68147bc92a705f1d740455dae78c1954c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:506c8c8ba838285e6896bd1c3cf8ffdedc11652fc16d25cacb6dbac6fe71b20f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273330394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2157852231054681d659923353e007b1f02cd1bde4253d99cc5680f65aaf28`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 19 Feb 2020 23:19:52 GMT
ADD file:c43f05fa78d78f998cd8e2e45f089e0572877490c7df425e514d44f15d958fad in / 
# Wed, 19 Feb 2020 23:19:52 GMT
CMD ["/bin/bash"]
# Wed, 19 Feb 2020 23:41:43 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 19 Feb 2020 23:41:44 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 19 Feb 2020 23:41:44 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 19 Feb 2020 23:41:44 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 19 Feb 2020 23:41:44 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 19 Feb 2020 23:41:45 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 19 Feb 2020 23:42:21 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 19 Feb 2020 23:42:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 20 Feb 2020 00:18:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 20 Feb 2020 00:18:17 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Feb 2020 00:18:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 20 Feb 2020 00:18:19 GMT
WORKDIR /usr/local/tomcat
# Thu, 20 Feb 2020 00:18:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 20 Feb 2020 00:18:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 20 Feb 2020 00:23:48 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 20 Feb 2020 00:23:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Mar 2020 23:11:51 GMT
ENV TOMCAT_VERSION=8.5.53
# Tue, 17 Mar 2020 23:11:51 GMT
ENV TOMCAT_SHA512=9ab2d12c068e1f9037d683b42ed998206a53fa2ab8dbb7bd49e1c6195db94b622542f18dcaee929e41b7491744f98a8e9aa9ca3ba768b82af2db3c5635ed7ebd
# Tue, 17 Mar 2020 23:13:34 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Tue, 17 Mar 2020 23:13:36 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Mar 2020 23:13:36 GMT
EXPOSE 8080
# Tue, 17 Mar 2020 23:13:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a7583ef20c9db3e6539d4160e9914383701901b24979656a228000718b0d5bea`  
		Last Modified: Wed, 19 Feb 2020 23:20:55 GMT  
		Size: 61.7 MB (61669860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f08580480af489e380b8d5a633c80120671eb871519e69f13dcd561ef1c19`  
		Last Modified: Wed, 19 Feb 2020 23:43:30 GMT  
		Size: 197.5 MB (197488397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9753256eef4ade7d0b8e9b332f722c912abb01219b7baa8c9efff66da84d8f`  
		Last Modified: Thu, 20 Feb 2020 00:32:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820d8ee62d91b9fcda3898f467b3873d0e8635ecb7ee763e67b299a9f760c60`  
		Last Modified: Tue, 17 Mar 2020 23:21:10 GMT  
		Size: 14.2 MB (14171865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3db68b582eb90d446b8dac0385cd67881c2201bfa441ec103bf25391d669be4`  
		Last Modified: Tue, 17 Mar 2020 23:21:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:aa56a31af3e9fb86c743d555c07cf9422d9d1d4b94bbec97e5680dbb676dc9f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274172938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ecbd4a863b65814040d1397ac5bf948aecc0f4a2301bdfdcc59d5cd3f0cc36`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Apr 2020 05:22:43 GMT
ADD file:40b8f329ad6d591029e1a4cde76c1d097315b136796d31bb9d3df35183423c14 in / 
# Wed, 01 Apr 2020 05:22:46 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 08:29:36 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 01 Apr 2020 08:29:37 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 08:29:37 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:38 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 01 Apr 2020 08:29:38 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 08:29:39 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:30:06 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 08:30:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 01 Apr 2020 08:49:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2020 08:49:44 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:49:46 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 01 Apr 2020 08:49:47 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2020 08:49:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2020 08:49:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2020 08:53:20 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 01 Apr 2020 08:53:21 GMT
ENV TOMCAT_MAJOR=8
# Wed, 01 Apr 2020 08:53:21 GMT
ENV TOMCAT_VERSION=8.5.53
# Wed, 01 Apr 2020 08:53:22 GMT
ENV TOMCAT_SHA512=9ab2d12c068e1f9037d683b42ed998206a53fa2ab8dbb7bd49e1c6195db94b622542f18dcaee929e41b7491744f98a8e9aa9ca3ba768b82af2db3c5635ed7ebd
# Wed, 01 Apr 2020 08:54:33 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Wed, 01 Apr 2020 08:54:37 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 01 Apr 2020 08:54:38 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:54:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:01d0a3bd5b98a6512409a10e5e5b065e87b794f924f3f9f7662939925aac631b`  
		Last Modified: Wed, 01 Apr 2020 05:24:01 GMT  
		Size: 63.1 MB (63072580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609ca5b883384db65353f55f91bc6a4c738f6fcfc23e18d46bc4a1d2580bfadc`  
		Last Modified: Wed, 01 Apr 2020 08:31:39 GMT  
		Size: 195.7 MB (195741837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850147b170d3cb6169ec1d64130c4990251c221906a375f5738293411f753b4`  
		Last Modified: Wed, 01 Apr 2020 08:59:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b1ca9f7798ad9cfbb695f196101ba37a77d4fe1819666f2f6452948c32d651`  
		Last Modified: Wed, 01 Apr 2020 09:00:00 GMT  
		Size: 15.4 MB (15358186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c395f91d6f821d0fa83e099ae2bc7b1e5c4c5e021d8a8b39a7dccad2e140e57`  
		Last Modified: Wed, 01 Apr 2020 08:59:57 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
