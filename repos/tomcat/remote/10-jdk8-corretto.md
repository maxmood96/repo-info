## `tomcat:10-jdk8-corretto`

```console
$ docker pull tomcat@sha256:13dfd674ce71ae41187238bcd25d02ecdcf07a64445c9538ff5ac49c138b7245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:0f3e404bfdf7303c75a4bcc4151037971b782105248185be2f076c3f3235c05e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152833852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b0685e3388ddc031505a925811adecb0bf871e5444e06bf0c17f0269029f90`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:20 GMT
ADD file:3b750ce7e7425c1cb02261d65b1e301d5818cda51a80dc8ab3b915ee5ca37d4e in / 
# Tue, 30 Mar 2021 21:59:21 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 23:19:20 GMT
ARG version=1.8.0_292.b10-1
# Tue, 20 Apr 2021 23:19:40 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Apr 2021 23:19:41 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:19:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Apr 2021 00:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Apr 2021 00:03:36 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Apr 2021 00:03:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Apr 2021 00:03:37 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Apr 2021 00:03:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:03:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:03:37 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 21 Apr 2021 00:03:37 GMT
ENV TOMCAT_MAJOR=10
# Wed, 21 Apr 2021 00:03:38 GMT
ENV TOMCAT_VERSION=10.0.5
# Wed, 21 Apr 2021 00:03:38 GMT
ENV TOMCAT_SHA512=27271e17c8daf52503490c6657c992cc150cf2942e1b0179b738f34e9aa5e1aac3c7b947c67441d17294a8f1e772a00e38e30b2135372d6ee9d71207ac7261c3
# Wed, 21 Apr 2021 00:04:12 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 21 Apr 2021 00:04:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Apr 2021 00:04:14 GMT
EXPOSE 8080
# Wed, 21 Apr 2021 00:04:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:99a21848b482c10fd4b103b7ab95e1446142e76e3dfa673efd0a23fb264ec5e5`  
		Last Modified: Tue, 30 Mar 2021 13:54:37 GMT  
		Size: 61.9 MB (61946585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ece89ed8d5944dabfaaa536301db77053bc6a2a996a272109b639f20b9cfca`  
		Last Modified: Tue, 20 Apr 2021 23:21:24 GMT  
		Size: 75.3 MB (75291677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ffc7e8fe565d39cc309f023ccbfbc2766a722ada133d550cdf0c7124ca6dd5`  
		Last Modified: Wed, 21 Apr 2021 00:18:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69973f45d78eecdd337f9c85b4954315ca0eded13dbad931b2c2340b00e016d6`  
		Last Modified: Wed, 21 Apr 2021 00:18:55 GMT  
		Size: 15.6 MB (15595287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7352ad805e58c80b1f33e095236ab446603cb40e13bebba4b43557539dba8c79`  
		Last Modified: Wed, 21 Apr 2021 00:18:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:101e145e5d450d43a072ccca2db6c175bab6ebc5045dbb3a08cf8ff18f8f1ac4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138643054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38967da6da37f65f5f622963122da174092f8703075dc9c88e9ae5594c35f577`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:58 GMT
ADD file:540e42c4903b87925bc490b00820f555e531041d1b1fcea6ee56f4cc3bbc895d in / 
# Tue, 30 Mar 2021 22:00:02 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 23:43:19 GMT
ARG version=1.8.0_292.b10-1
# Tue, 20 Apr 2021 23:43:53 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Apr 2021 23:43:55 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:43:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Apr 2021 00:24:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Apr 2021 00:24:07 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Apr 2021 00:24:09 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Apr 2021 00:24:10 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Apr 2021 00:24:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:24:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:24:13 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 21 Apr 2021 00:24:14 GMT
ENV TOMCAT_MAJOR=10
# Wed, 21 Apr 2021 00:24:15 GMT
ENV TOMCAT_VERSION=10.0.5
# Wed, 21 Apr 2021 00:24:16 GMT
ENV TOMCAT_SHA512=27271e17c8daf52503490c6657c992cc150cf2942e1b0179b738f34e9aa5e1aac3c7b947c67441d17294a8f1e772a00e38e30b2135372d6ee9d71207ac7261c3
# Wed, 21 Apr 2021 00:25:11 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 21 Apr 2021 00:25:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Apr 2021 00:25:17 GMT
EXPOSE 8080
# Wed, 21 Apr 2021 00:25:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7d8296f22a3c3f786ce15fb5be7dce44af09932e617f9a981183619985014031`  
		Last Modified: Tue, 30 Mar 2021 22:01:09 GMT  
		Size: 63.7 MB (63660038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19674c905fc4a155e31837e0f8b91c7a503bd185ffae72d35ce7877265d63dae`  
		Last Modified: Tue, 20 Apr 2021 23:45:24 GMT  
		Size: 59.4 MB (59389850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed2a49c1109e02b41ce52819e07afd748db247badb6007af986e4222ec9bb1`  
		Last Modified: Wed, 21 Apr 2021 00:44:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06355ae4894068f05621793f5a569bd3ae95416f5d09724c9c15500ce1c8d7`  
		Last Modified: Wed, 21 Apr 2021 00:44:27 GMT  
		Size: 15.6 MB (15592860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933c8b13f30207b8b602d164534817e510a69585d8acfe4fa2d558c5258afcd`  
		Last Modified: Wed, 21 Apr 2021 00:44:24 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
