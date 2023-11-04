## `tomcat:9-jdk8-corretto-al2`

```console
$ docker pull tomcat@sha256:902047b947d35ec276068bba45f26ee9d77cfec34840ac764aba192cef4876ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk8-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:b74dd6880fb1cd194fe23f3d2bec0cd0e89e79b609302632eb666c09c9e77709
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155109196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaf8bb8e2c9d1881bce96ca2d6c483208912e8c366fecd9108e0d34dd0e0637`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:53 GMT
COPY dir:3e6cf913ede7c7c09de0465c096dad9a8bea883f026db356d68f0e799e2e3847 in / 
# Fri, 03 Nov 2023 22:21:53 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:38:47 GMT
ARG version=1.8.0_392.b08-1
# Fri, 03 Nov 2023 22:39:09 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:39:09 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:39:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 04 Nov 2023 00:04:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 04 Nov 2023 00:04:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2023 00:04:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 04 Nov 2023 00:04:38 GMT
WORKDIR /usr/local/tomcat
# Sat, 04 Nov 2023 00:04:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 04 Nov 2023 00:04:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 04 Nov 2023 00:04:38 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 04 Nov 2023 00:04:38 GMT
ENV TOMCAT_MAJOR=9
# Sat, 04 Nov 2023 00:04:38 GMT
ENV TOMCAT_VERSION=9.0.82
# Sat, 04 Nov 2023 00:04:38 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Sat, 04 Nov 2023 00:05:14 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Sat, 04 Nov 2023 00:05:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 04 Nov 2023 00:05:15 GMT
EXPOSE 8080
# Sat, 04 Nov 2023 00:05:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6ebddf7084e9402a3ba6cf1360703e12633f9c49f51772f99c298cd1048d728e`  
		Last Modified: Fri, 03 Nov 2023 11:40:21 GMT  
		Size: 62.6 MB (62646469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e94e63f60b4802fe552c16fdf0857fa14a4d72107a01b9bbd60dc9c1d8b7a2b`  
		Last Modified: Fri, 03 Nov 2023 22:52:21 GMT  
		Size: 75.6 MB (75586873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a5d4076c9ac9595ee4519e1751accad6db88f3137016273da9a8220173a270`  
		Last Modified: Sat, 04 Nov 2023 00:13:44 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8565825042dd65e00ec9fca6911e4fd212139c54061e9313dea5f6e664e0f8b`  
		Last Modified: Sat, 04 Nov 2023 00:13:46 GMT  
		Size: 16.9 MB (16875552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6531091f411e155416b9afa45da4d6dea13969b50e9aa95e3096043e677f3fa`  
		Last Modified: Sat, 04 Nov 2023 00:13:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk8-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7cae35d9fd2621d88f7e4831df3350e01006da51bb176cf100ca6aff439d5457
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140821215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c1852a84d651d3bab9864b4114efabf7180c4ee9390a2cfd2e83f008ccd31e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:56:15 GMT
ARG version=1.8.0_392.b08-1
# Fri, 03 Nov 2023 22:56:31 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:56:32 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:56:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Nov 2023 23:49:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Nov 2023 23:49:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Nov 2023 23:49:40 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Nov 2023 23:49:40 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Nov 2023 23:49:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Nov 2023 23:49:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Nov 2023 23:49:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Nov 2023 23:49:41 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Nov 2023 23:49:41 GMT
ENV TOMCAT_VERSION=9.0.82
# Fri, 03 Nov 2023 23:49:41 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Fri, 03 Nov 2023 23:50:11 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Fri, 03 Nov 2023 23:50:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Nov 2023 23:50:12 GMT
EXPOSE 8080
# Fri, 03 Nov 2023 23:50:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5a65a128cd0e4a050ccae0c23b1c346c7b82b679bf029de348d4536709ade2`  
		Last Modified: Fri, 03 Nov 2023 23:06:52 GMT  
		Size: 59.6 MB (59613098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e3185585d167e967178afcb05d12744e09663bb7c35e8c44c397ddace271e`  
		Last Modified: Fri, 03 Nov 2023 23:57:50 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92dd1900bef90e30d9046d1e60e36c136b3326b9d2855abcc57a694ebe4c41cb`  
		Last Modified: Fri, 03 Nov 2023 23:57:51 GMT  
		Size: 16.8 MB (16827610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d411755886b81b994e44e6011bd9e1abb64a9e5c8c7c8334333d68662330feb4`  
		Last Modified: Fri, 03 Nov 2023 23:57:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
