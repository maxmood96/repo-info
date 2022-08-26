## `tomcat:10-jdk17-corretto`

```console
$ docker pull tomcat@sha256:f636376a73b1740dcda8ee9cd6512000bf925feca879fe52e1a093921f3c1c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk17-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:4e3a7fd0b777e0132430e17c56da2e6e6ef89135980d470be8032f28157f117c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230793812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd3b567e377aae67d6badd920ce21cd9d76a01f40a88c53e9529f86636a189b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Aug 2022 01:19:36 GMT
ADD file:ebfd33425a17b16a9e560de15c91108bf2ee740f284a1482a7105b420ff22678 in / 
# Fri, 26 Aug 2022 01:19:37 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 02:04:12 GMT
ARG version=17.0.4.9-1
# Fri, 26 Aug 2022 02:04:48 GMT
# ARGS: version=17.0.4.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 02:04:48 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 02:04:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 26 Aug 2022 02:31:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Aug 2022 02:31:59 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 02:31:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 26 Aug 2022 02:31:59 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Aug 2022 02:32:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 02:32:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 02:32:00 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 26 Aug 2022 02:32:00 GMT
ENV TOMCAT_MAJOR=10
# Fri, 26 Aug 2022 02:32:00 GMT
ENV TOMCAT_VERSION=10.0.23
# Fri, 26 Aug 2022 02:32:00 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Fri, 26 Aug 2022 02:32:36 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 26 Aug 2022 02:32:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 26 Aug 2022 02:32:38 GMT
EXPOSE 8080
# Fri, 26 Aug 2022 02:32:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fd06b60db4951fd95b43a9e73fb084fe7d2afcd4ff464472ead5548cd1c28717`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 62.3 MB (62326701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb036d0e9663b7f913ccd85668091b61213d2f809739041c219aa4150e95baf8`  
		Last Modified: Fri, 26 Aug 2022 02:08:22 GMT  
		Size: 151.7 MB (151663675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87adba3dc5638aad30c784bdf27e0cf58297e1bcfd5bccdbc186cf43adb6c820`  
		Last Modified: Fri, 26 Aug 2022 02:45:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1805b7b30f266b3eb82ffb0d2741edbdbfe61f24d58f05bf32752227d0fb1d02`  
		Last Modified: Fri, 26 Aug 2022 02:45:09 GMT  
		Size: 16.8 MB (16803132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aeecc0aebe2ba64c42a575349ca6fbf1ec82c56879e6ca220c1171383aeadf1`  
		Last Modified: Fri, 26 Aug 2022 02:45:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:bba32d4cf4566eff13598a0766da33bc9df07d503f418c6b0b09358dcf32ac8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230892030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dd02423b292a220ccb91edc007cf198ea046cbed8ab055e20c22d8c9009e21`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 01:01:47 GMT
ARG version=17.0.4.9-1
# Fri, 26 Aug 2022 01:02:06 GMT
# ARGS: version=17.0.4.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 01:02:06 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 01:02:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 26 Aug 2022 01:44:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Aug 2022 01:44:58 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 01:44:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 26 Aug 2022 01:45:00 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Aug 2022 01:45:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 01:45:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 01:45:03 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 26 Aug 2022 01:45:04 GMT
ENV TOMCAT_MAJOR=10
# Fri, 26 Aug 2022 01:45:05 GMT
ENV TOMCAT_VERSION=10.0.23
# Fri, 26 Aug 2022 01:45:06 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Fri, 26 Aug 2022 01:45:28 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 26 Aug 2022 01:45:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 26 Aug 2022 01:45:30 GMT
EXPOSE 8080
# Fri, 26 Aug 2022 01:45:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d9f6ed17988abb0810c79c739409f7131a60308790d99bb799d5cf30aa148a`  
		Last Modified: Fri, 26 Aug 2022 01:04:43 GMT  
		Size: 150.2 MB (150177681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e38249c4c47931fceddac2b928543d653f1fb6c4f8a667f7b21bd43c6bcba79`  
		Last Modified: Fri, 26 Aug 2022 02:04:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524ce5d741448fa1d51372cd371d55e6cf7c67ec226201159cd57c64e02e1668`  
		Last Modified: Fri, 26 Aug 2022 02:04:32 GMT  
		Size: 16.8 MB (16775445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
