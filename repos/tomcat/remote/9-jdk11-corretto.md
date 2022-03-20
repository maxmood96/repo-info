## `tomcat:9-jdk11-corretto`

```console
$ docker pull tomcat@sha256:6da0a94adfa8169e4ffa7129281a0bcfe3f7fd14b2b0e239a715d9ead483f618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:8db05f64b9372171eeeb6bf0063e7aff6f6ce399993b4ac5accff53bdd2b0407
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225478695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88124a6162eac9dec4258f37d03968da677659dfd818273aeed31f9380417fa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:35:29 GMT
ARG version=11.0.14.9-1
# Sat, 19 Mar 2022 00:35:58 GMT
# ARGS: version=11.0.14.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 00:35:58 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:35:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sun, 20 Mar 2022 11:11:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 20 Mar 2022 11:11:09 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 11:11:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 20 Mar 2022 11:11:10 GMT
WORKDIR /usr/local/tomcat
# Sun, 20 Mar 2022 11:11:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:11:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:37:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sun, 20 Mar 2022 11:37:03 GMT
ENV TOMCAT_MAJOR=9
# Sun, 20 Mar 2022 11:37:03 GMT
ENV TOMCAT_VERSION=9.0.60
# Sun, 20 Mar 2022 11:37:03 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Sun, 20 Mar 2022 11:38:06 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Sun, 20 Mar 2022 11:38:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 20 Mar 2022 11:38:08 GMT
EXPOSE 8080
# Sun, 20 Mar 2022 11:38:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77db69e35f1786a5ca4b8b4a5fa64882cfc3100f27262d0b018881f203179fd`  
		Last Modified: Sat, 19 Mar 2022 00:43:06 GMT  
		Size: 146.9 MB (146878018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc8606c1a37023182a01f3c7ef9257ad51ca8748524c402a029e4e4548ed3b`  
		Last Modified: Sun, 20 Mar 2022 12:08:59 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb625ac550ff2dc03d598e9089456f5bbffa84fd8f1af7c61634813d3df78711`  
		Last Modified: Sun, 20 Mar 2022 12:23:04 GMT  
		Size: 16.4 MB (16395102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc9fabbd4a9bec608af38b6b3b224f9abc19bb85ad3989698869d850fa8440a`  
		Last Modified: Sun, 20 Mar 2022 12:23:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e34344b46d7851fac24456bd594cc9805cc627f6b993bd378f93a6a9c92496fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224253575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1fde38a8dc08ae8d65c608d4e030f9fcc8ab5fe5ed1d3184ee075b57255ef2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 15:03:19 GMT
ARG version=11.0.14.9-1
# Sat, 19 Mar 2022 15:03:35 GMT
# ARGS: version=11.0.14.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 15:03:35 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 15:03:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 19 Mar 2022 22:46:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 22:46:34 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 22:46:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 22:46:36 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 22:46:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 22:46:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 23:10:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 19 Mar 2022 23:10:41 GMT
ENV TOMCAT_MAJOR=9
# Sat, 19 Mar 2022 23:10:42 GMT
ENV TOMCAT_VERSION=9.0.60
# Sat, 19 Mar 2022 23:10:43 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Sat, 19 Mar 2022 23:11:58 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Sat, 19 Mar 2022 23:11:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 23:12:00 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 23:12:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633892078b4e36d0ebf06999214dc79c7e5584ff6412bf83950d80a686fa9d6`  
		Last Modified: Sat, 19 Mar 2022 15:05:24 GMT  
		Size: 144.1 MB (144091030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78eb7e664f8b7530ef27c532df8dec8f8fdb13baa30dbaff8a852358210bd1a8`  
		Last Modified: Sat, 19 Mar 2022 23:53:16 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe6ac46876c6d1304d2408d66a7f56b3dd765a4d6a21f83b13bbc0ee7131828`  
		Last Modified: Sun, 20 Mar 2022 00:03:00 GMT  
		Size: 16.3 MB (16333521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
