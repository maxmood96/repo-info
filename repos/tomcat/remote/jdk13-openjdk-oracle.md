## `tomcat:jdk13-openjdk-oracle`

```console
$ docker pull tomcat@sha256:5cce09f2638139f730c21f00b550dd21ba600007f9d2df8c2e554c30b3634d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomcat:jdk13-openjdk-oracle` - linux; amd64

```console
$ docker pull tomcat@sha256:68119b42ba38200cc676588e149ea6159686976b93e01fb7d5be37e7c7393c6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269913425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f0d0094259c8aa39fe43e75aef787f2e8782182d98fce3c9452050002b047f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 28 Jan 2020 21:36:05 GMT
ADD file:a320cfe017a986947ac6b09db573e476eacafc80311e517efcc5e965fcc445fb in / 
# Tue, 28 Jan 2020 21:36:06 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2020 21:53:09 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jan 2020 21:53:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jan 2020 21:58:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 28 Jan 2020 21:58:14 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:58:14 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 28 Jan 2020 21:58:15 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 28 Jan 2020 21:58:15 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 28 Jan 2020 21:58:47 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 28 Jan 2020 21:58:47 GMT
CMD ["jshell"]
# Tue, 28 Jan 2020 22:30:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2020 22:30:06 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 22:30:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jan 2020 22:30:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2020 22:30:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 22:30:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 22:31:53 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 28 Jan 2020 22:31:53 GMT
ENV TOMCAT_MAJOR=8
# Tue, 11 Feb 2020 21:46:44 GMT
ENV TOMCAT_VERSION=8.5.51
# Tue, 11 Feb 2020 21:46:44 GMT
ENV TOMCAT_SHA512=bb9207d33d7b4408292186523f3556a3d1454ea172b4a6cde6e0028e2f7a5d9408615cb4ccf8d9fdb75a9f8ce227580f56f929a811eb24ef99e26f980e4bcb48
# Tue, 11 Feb 2020 21:47:51 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Tue, 11 Feb 2020 21:47:53 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Feb 2020 21:47:53 GMT
EXPOSE 8080
# Tue, 11 Feb 2020 21:47:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:86607bb85307f4e017c6cc236573951482f1de084e0987480fecea9295c2f923`  
		Last Modified: Tue, 28 Jan 2020 21:37:18 GMT  
		Size: 42.7 MB (42725283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d217c4e16034b1dca5abb6ea80aabded93c73f35686d806d9f2aa8555743da`  
		Last Modified: Tue, 28 Jan 2020 22:00:21 GMT  
		Size: 14.8 MB (14793339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9595022a553604b9baa8a02558174325cd4be3fb6b7920f86a7e425fc4539de5`  
		Last Modified: Tue, 28 Jan 2020 22:01:41 GMT  
		Size: 196.4 MB (196372674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5b43ff0910781906336ceeea4c3645a3b023c6962c95942f3cd5d73746492a`  
		Last Modified: Tue, 28 Jan 2020 22:34:31 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b6c929fd99439a1fa4f38165b3f2242895c5d453fc006c561b389e3a115ba5`  
		Last Modified: Tue, 11 Feb 2020 21:59:02 GMT  
		Size: 16.0 MB (16021861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0370991515daca8b257478c7a02201d0feb3cf67e9e1fc9e5c9358ff428c83db`  
		Last Modified: Tue, 11 Feb 2020 21:59:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
