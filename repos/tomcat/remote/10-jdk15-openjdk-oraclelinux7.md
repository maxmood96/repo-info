## `tomcat:10-jdk15-openjdk-oraclelinux7`

```console
$ docker pull tomcat@sha256:d3a12a5e3c872e6c4d5f6794c0d40c0212bc1debe8eada9f6aca5b1a064bbace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk15-openjdk-oraclelinux7` - linux; amd64

```console
$ docker pull tomcat@sha256:3a247b624e47706c79ebffdab2156f6b73cba001393547b07b6764ee05d7bc4e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276546964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a3313b58e9584d60cf30ca4d898b1b559b366dd12a1058bc70f59816aa8122`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 15 Sep 2020 21:23:41 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 06 Jan 2021 20:22:16 GMT
ADD file:dee09ad1ed4e7359b14fabc84890b1fb687ad4efe75f7c4800c0a907fd4f70a3 in / 
# Wed, 06 Jan 2021 20:22:16 GMT
CMD ["/bin/bash"]
# Wed, 06 Jan 2021 20:41:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 06 Jan 2021 20:41:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Jan 2021 20:43:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 06 Jan 2021 20:43:37 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jan 2021 20:43:38 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 06 Jan 2021 20:43:49 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 06 Jan 2021 20:43:50 GMT
CMD ["jshell"]
# Wed, 06 Jan 2021 21:33:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Jan 2021 21:33:33 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jan 2021 21:33:34 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Jan 2021 21:33:34 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Jan 2021 21:33:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Jan 2021 21:33:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Jan 2021 21:33:35 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 06 Jan 2021 21:33:35 GMT
ENV TOMCAT_MAJOR=10
# Wed, 06 Jan 2021 21:33:35 GMT
ENV TOMCAT_VERSION=10.0.0
# Wed, 06 Jan 2021 21:33:35 GMT
ENV TOMCAT_SHA512=bf3592ef3807af6284060aacaf44174fe7d51079196cfe06fd30c17414a4dd59b7b0c8288ccc2c93fbbd38b090f3bbc43fa06ecf971217b8ec1fa383d8095497
# Wed, 06 Jan 2021 21:34:41 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 06 Jan 2021 21:34:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Jan 2021 21:34:43 GMT
EXPOSE 8080
# Wed, 06 Jan 2021 21:34:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:980316e412373040bc280150078ae453b259ece36b750a0a9b6f4c99751ce4f9`  
		Last Modified: Wed, 06 Jan 2021 20:24:02 GMT  
		Size: 48.3 MB (48260808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344a44c175048c7ccd1f6f0be52b7945e1a34a79995fb5de5737026d0474ebfe`  
		Last Modified: Wed, 06 Jan 2021 20:47:51 GMT  
		Size: 15.4 MB (15431553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a8e1188dd1ca21b96bed9711c412fe4d42cd9659dd12964bc816a48e5b73d5`  
		Last Modified: Wed, 06 Jan 2021 20:50:31 GMT  
		Size: 195.8 MB (195779472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b331524c40cc5543715c6d6c6427cfe66e0ef192c2c57b80becebbe3d645`  
		Last Modified: Wed, 06 Jan 2021 21:43:33 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9be13d69caa8f755d8d9f66e47c9ebbe65fa0a25311959e1ca8a239a9748586`  
		Last Modified: Wed, 06 Jan 2021 21:43:33 GMT  
		Size: 17.1 MB (17074864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ae127e4166f2c33a608140de95302b941fdd48205a8bd176f62a5685e68126`  
		Last Modified: Wed, 06 Jan 2021 21:43:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk15-openjdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:21bb641808b38f7306e0a1a7cff47f0f911a563dad5678aa0d296ad91c581115
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256306126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed42e27a7740b06b09a254aa24bdf09fc34e683de40c5b5f9ae99bb82fa553da`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 06 Jan 2021 20:45:46 GMT
ADD file:d4d5ffcc8d57e27f8de10063c4e347d2f4da299f62166d6f6387a7714f5e0f06 in / 
# Wed, 06 Jan 2021 20:45:48 GMT
CMD ["/bin/bash"]
# Wed, 06 Jan 2021 21:06:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 06 Jan 2021 21:06:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Jan 2021 21:10:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 06 Jan 2021 21:10:02 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jan 2021 21:10:03 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 06 Jan 2021 21:10:25 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 06 Jan 2021 21:10:27 GMT
CMD ["jshell"]
# Wed, 06 Jan 2021 21:44:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Jan 2021 21:44:01 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jan 2021 21:44:02 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Jan 2021 21:44:03 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Jan 2021 21:44:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Jan 2021 21:44:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Jan 2021 21:44:05 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 06 Jan 2021 21:44:05 GMT
ENV TOMCAT_MAJOR=10
# Wed, 06 Jan 2021 21:44:06 GMT
ENV TOMCAT_VERSION=10.0.0
# Wed, 06 Jan 2021 21:44:06 GMT
ENV TOMCAT_SHA512=bf3592ef3807af6284060aacaf44174fe7d51079196cfe06fd30c17414a4dd59b7b0c8288ccc2c93fbbd38b090f3bbc43fa06ecf971217b8ec1fa383d8095497
# Wed, 06 Jan 2021 21:45:05 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 06 Jan 2021 21:45:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Jan 2021 21:45:09 GMT
EXPOSE 8080
# Wed, 06 Jan 2021 21:45:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e2e87614faabf530f11811ae8eb1be9e586d5d923036268129a39eae319cb772`  
		Last Modified: Wed, 06 Jan 2021 20:47:54 GMT  
		Size: 48.9 MB (48858154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141908ad8b1f3520523867010d20883b59e3c504867fad3ab621d90a951a0a31`  
		Last Modified: Wed, 06 Jan 2021 21:14:34 GMT  
		Size: 16.5 MB (16470893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6540fbc83e6d769ff59f083586324040cd2317595c3027c2fcdb6bd0e6c0c9`  
		Last Modified: Wed, 06 Jan 2021 21:18:21 GMT  
		Size: 174.9 MB (174886838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee121d898e9e900903bd360e6c32f011de5cc3ab7a147f995420a16d24b273b0`  
		Last Modified: Wed, 06 Jan 2021 21:52:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f823fcb0f39908d645528c9be390b079ca0e704e42f0e02cec6eb640151ea01b`  
		Last Modified: Wed, 06 Jan 2021 21:52:36 GMT  
		Size: 16.1 MB (16089938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab5c6899ddbd34b303d9c1246801f9ac121deb1a4720a477df7be16dbde14ad`  
		Last Modified: Wed, 06 Jan 2021 21:52:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
