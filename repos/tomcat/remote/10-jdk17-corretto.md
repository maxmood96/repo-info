## `tomcat:10-jdk17-corretto`

```console
$ docker pull tomcat@sha256:e77687e996165428a91e612695fcfeb092c16e150724c6c5c6e92be4b7511ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk17-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:4eeb43ebca586fb5f3b73cd4048eaccd36070faa7185909a01c4705c11ea5003
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230556878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab49008bd162fbbdf6fda0fabbcdc0f08182384b820df790c579b69d854e351f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:36:55 GMT
ARG version=17.0.2.8-1
# Sat, 19 Mar 2022 00:37:27 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 00:37:28 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:37:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 20 Mar 2022 11:03:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 20 Mar 2022 11:03:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 11:03:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 20 Mar 2022 11:03:44 GMT
WORKDIR /usr/local/tomcat
# Sun, 20 Mar 2022 11:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:03:44 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 20 Mar 2022 11:03:44 GMT
ENV TOMCAT_MAJOR=10
# Sun, 20 Mar 2022 11:16:29 GMT
ENV TOMCAT_VERSION=10.0.18
# Sun, 20 Mar 2022 11:16:29 GMT
ENV TOMCAT_SHA512=a9e3c516676369bd9d52e768071898b0e07659a9ff03b9dc491e53f084b9981a929bf2c74a694f06ad26dae0644fb9617cc6e364f0e1dcd953c857978a95a644
# Sun, 20 Mar 2022 11:17:35 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Sun, 20 Mar 2022 11:17:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 20 Mar 2022 11:17:36 GMT
EXPOSE 8080
# Sun, 20 Mar 2022 11:17:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe6dac67102bcfdf5d509e6ecae60bc439768df7e02101826619b7b238cd3`  
		Last Modified: Sat, 19 Mar 2022 00:45:34 GMT  
		Size: 151.6 MB (151604861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fb0304c3a94fcba3f561e849ac9ceb481e8c5eb113204b0bd2f7e2c85faa36`  
		Last Modified: Sun, 20 Mar 2022 12:05:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1f14c04436050e0b2ca1f3b4c862591ee54529f53a24fc4998223412c61522`  
		Last Modified: Sun, 20 Mar 2022 12:10:57 GMT  
		Size: 16.7 MB (16746444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f31174df96f00c5e911e59290d19f752013e4131ab06cc9590bb85443826320`  
		Last Modified: Sun, 20 Mar 2022 12:10:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b975aaeeec011779b78dd1e50cd6c41000d0e2f1c28b5ad9ed7200a33cd9dc93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230701703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1729b050553e2a5cec9f69bb5273b2f9435537217c66e041052eee34b1abb98`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 15:03:43 GMT
ARG version=17.0.2.8-1
# Sat, 19 Mar 2022 15:03:59 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 15:03:59 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 15:04:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 19 Mar 2022 22:40:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 22:40:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 22:40:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 22:40:42 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 22:40:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 22:40:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 22:40:45 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 19 Mar 2022 22:40:46 GMT
ENV TOMCAT_MAJOR=10
# Sat, 19 Mar 2022 22:50:20 GMT
ENV TOMCAT_VERSION=10.0.18
# Sat, 19 Mar 2022 22:50:21 GMT
ENV TOMCAT_SHA512=a9e3c516676369bd9d52e768071898b0e07659a9ff03b9dc491e53f084b9981a929bf2c74a694f06ad26dae0644fb9617cc6e364f0e1dcd953c857978a95a644
# Sat, 19 Mar 2022 22:51:16 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Sat, 19 Mar 2022 22:51:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 22:51:18 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:51:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f890b2334e8fec631b028cc4715d120348412f974e00dc0e06c0d9dfd5f8b7d`  
		Last Modified: Sat, 19 Mar 2022 15:06:03 GMT  
		Size: 150.2 MB (150174108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b566f9a7ba20c821b3b2145c3d3f89177656f940d74c55f04bce83485dcbe9c`  
		Last Modified: Sat, 19 Mar 2022 23:51:14 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5074cc19ae5b50386a0b870b0ce8e65dbab9b23ebbf454633b7e1b4a134506`  
		Last Modified: Sat, 19 Mar 2022 23:54:43 GMT  
		Size: 16.7 MB (16698570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
