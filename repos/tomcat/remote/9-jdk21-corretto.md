## `tomcat:9-jdk21-corretto`

```console
$ docker pull tomcat@sha256:3d54c80e74b28c03adb2ea7d4f966b4333d27cbead646a15f69ef4535d2455ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk21-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:7a853eb5148fee65cff417dfcc1f7431b9fa0fb31df30ec11d37ae80bfb7ab80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245315790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a0983860171ef8ff13f399d0a9978f0ecf918c5c64388a3b717cc2214f1a80`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 26 Feb 2024 22:52:13 GMT
COPY dir:54de4a09e8ed7b6d891ffc8d82bcabfb18706cd08eadb7193bbf9e8397ee4d73 in / 
# Mon, 26 Feb 2024 22:52:14 GMT
CMD ["/bin/bash"]
# Tue, 27 Feb 2024 20:53:01 GMT
ARG version=21.0.2.14-1
# Tue, 27 Feb 2024 20:53:26 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 27 Feb 2024 20:53:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 20:53:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Feb 2024 21:33:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 27 Feb 2024 21:33:04 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 21:33:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 27 Feb 2024 21:33:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 27 Feb 2024 21:33:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 27 Feb 2024 21:33:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 27 Feb 2024 21:33:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 27 Feb 2024 21:33:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Feb 2024 21:33:05 GMT
ENV TOMCAT_VERSION=9.0.86
# Tue, 27 Feb 2024 21:33:05 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Tue, 27 Feb 2024 21:33:42 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Tue, 27 Feb 2024 21:33:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Feb 2024 21:33:43 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 21:33:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e24f20ed38d851720ffd5b15a06dad772c10fa9feea0e462fb5065d997fcb0bb`  
		Last Modified: Sat, 24 Feb 2024 04:13:54 GMT  
		Size: 62.6 MB (62646731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65aa1d9db07ada9a2a5b4a0639f7f172d6455047e28e85f0820b2ecbab083f42`  
		Last Modified: Tue, 27 Feb 2024 20:57:24 GMT  
		Size: 165.7 MB (165693563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e68e8638e7acccfd37a18b820b750a2280b4db6b4d84f0eb23a65e612cb21a1`  
		Last Modified: Tue, 27 Feb 2024 21:38:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816b9346605a7d516fc3f5383a9d068efbde6858f3ff0796b2de9ef8e5816a79`  
		Last Modified: Tue, 27 Feb 2024 21:38:36 GMT  
		Size: 17.0 MB (16975191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e72cfdd21c484abcf099f1e47bc94a8b1b03cbf8301ba2d2530d9a91a95b83`  
		Last Modified: Tue, 27 Feb 2024 21:38:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9864fa561e7e0958f6501c371fc6da52222bdab86563fae858ca66949fc639ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245048481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1c48ce562af5d5abf5a69d31a242c647314c1a5d3ac930b7895ae29b668971`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:29 GMT
COPY dir:ed6a811a4137d0b4591f2c9dabfdd849cb878c3501af91aa79c89a2e9f4479d5 in / 
# Mon, 26 Feb 2024 23:06:30 GMT
CMD ["/bin/bash"]
# Tue, 27 Feb 2024 21:07:28 GMT
ARG version=21.0.2.14-1
# Tue, 27 Feb 2024 21:07:50 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 27 Feb 2024 21:07:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 21:07:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Feb 2024 21:44:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 27 Feb 2024 21:44:14 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 21:44:15 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 27 Feb 2024 21:44:15 GMT
WORKDIR /usr/local/tomcat
# Tue, 27 Feb 2024 21:44:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 27 Feb 2024 21:44:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 27 Feb 2024 21:44:15 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 27 Feb 2024 21:44:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Feb 2024 21:44:15 GMT
ENV TOMCAT_VERSION=9.0.86
# Tue, 27 Feb 2024 21:44:15 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Tue, 27 Feb 2024 21:44:45 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Tue, 27 Feb 2024 21:44:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Feb 2024 21:44:46 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 21:44:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:53f483bd5fa48049d6551a641e547b302df82b17493915161f3f62020b3648fa`  
		Last Modified: Mon, 26 Feb 2024 23:07:06 GMT  
		Size: 64.4 MB (64445079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941afd9563243fdf387f8568f0c597eea409bf24c6eb89f386125dbf384f6087`  
		Last Modified: Tue, 27 Feb 2024 21:12:01 GMT  
		Size: 163.7 MB (163666566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d754290fe35a99eeab9299c650750422786f8f0430afb2961370ad005c21b8`  
		Last Modified: Tue, 27 Feb 2024 21:49:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9cccf3032d8cbb0a2e9aef07515c6dd855f185bcf9c7dc649a6471a3d3908b`  
		Last Modified: Tue, 27 Feb 2024 21:49:03 GMT  
		Size: 16.9 MB (16936532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaea840a37327a99c593823830435da33dc928fb34a2aeefa2fba6c143b5447`  
		Last Modified: Tue, 27 Feb 2024 21:49:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
