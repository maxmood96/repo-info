## `tomcat:jdk8-corretto`

```console
$ docker pull tomcat@sha256:83b7dea3712f63090ab92ec26c5cef49283455441e1de2d8947422f1a74d60a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:75250ffde89571dcf823ec8ccbf254aafcae2b705572af89f292b05a0c6aa99f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154458206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f937ee52059dbbfd1c94c4db6b9b3d3b135634ad24312095a87c5401c4c604d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 12 Jan 2022 02:20:04 GMT
ADD file:618cac8c5b6f6ff56ce221df12002d34997bcc996a0af3200b58db07d68be275 in / 
# Wed, 12 Jan 2022 02:20:04 GMT
CMD ["/bin/bash"]
# Wed, 19 Jan 2022 22:01:35 GMT
ARG version=1.8.0_322.b06-2
# Wed, 19 Jan 2022 22:01:56 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 19 Jan 2022 22:01:56 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:01:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 20 Jan 2022 01:00:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 20 Jan 2022 01:00:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jan 2022 01:00:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 20 Jan 2022 01:00:17 GMT
WORKDIR /usr/local/tomcat
# Thu, 20 Jan 2022 01:00:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 20 Jan 2022 01:00:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 20 Jan 2022 01:00:17 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 20 Jan 2022 01:00:17 GMT
ENV TOMCAT_MAJOR=10
# Thu, 20 Jan 2022 01:00:18 GMT
ENV TOMCAT_VERSION=10.0.14
# Thu, 20 Jan 2022 01:00:18 GMT
ENV TOMCAT_SHA512=c2d2ad5ed17f7284e3aac5415774a8ef35434f14dbd9a87bc7230d8bfdbe9aa1258b97a59fa5c4030e4c973e4d93d29d20e40b6254347dbb66fae269ff4a61a5
# Thu, 20 Jan 2022 01:00:52 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 20 Jan 2022 01:00:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 20 Jan 2022 01:00:54 GMT
EXPOSE 8080
# Thu, 20 Jan 2022 01:00:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3a461b3ae562f8b6cf015b4c480a21b630a874f7fec851457680159226c81632`  
		Last Modified: Mon, 10 Jan 2022 23:29:44 GMT  
		Size: 62.2 MB (62212074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa51ad4401a3e61c51b1c30b9b21b3aaf8243cf97d982ecd0bbc6aeb82b3f5cb`  
		Last Modified: Wed, 19 Jan 2022 22:07:06 GMT  
		Size: 75.5 MB (75530704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16756b758cd2487d710a789b1988eba3bc82ca5d06c692a2194e995a37640071`  
		Last Modified: Thu, 20 Jan 2022 01:33:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e4c394a816f3f7a87780709f15c17be0026130d474f170f8ce9367689d5bbf`  
		Last Modified: Thu, 20 Jan 2022 01:34:00 GMT  
		Size: 16.7 MB (16715123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbb9f5834fe0cbb9f170b72e810db6eb6c5acf17fa2bfd37cdbb8c2aae95689`  
		Last Modified: Thu, 20 Jan 2022 01:33:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2aa6282bfeb5b6f53666378ea32a18cf557b333fe3118dbf77a5023247961589
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140055961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57161b021beb37642ac56118a615a7caa53df1921cae5e162df3c96ce4ac9b00`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 12 Jan 2022 02:39:41 GMT
ADD file:afc90ca87d61fdaef5c9d192a5151ab745ac8b8ea4d7544c2dfdd66bdb3b7993 in / 
# Wed, 12 Jan 2022 02:39:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Jan 2022 22:29:34 GMT
ARG version=1.8.0_322.b06-2
# Wed, 19 Jan 2022 22:29:46 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 19 Jan 2022 22:29:47 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:29:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 19 Jan 2022 23:41:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jan 2022 23:41:44 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jan 2022 23:41:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 19 Jan 2022 23:41:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jan 2022 23:41:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jan 2022 23:41:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jan 2022 23:41:49 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 19 Jan 2022 23:41:50 GMT
ENV TOMCAT_MAJOR=10
# Wed, 19 Jan 2022 23:41:51 GMT
ENV TOMCAT_VERSION=10.0.14
# Wed, 19 Jan 2022 23:41:52 GMT
ENV TOMCAT_SHA512=c2d2ad5ed17f7284e3aac5415774a8ef35434f14dbd9a87bc7230d8bfdbe9aa1258b97a59fa5c4030e4c973e4d93d29d20e40b6254347dbb66fae269ff4a61a5
# Wed, 19 Jan 2022 23:42:15 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 19 Jan 2022 23:42:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 19 Jan 2022 23:42:18 GMT
EXPOSE 8080
# Wed, 19 Jan 2022 23:42:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b2e274b2b0f90c3d6329566163244a0f2e6d97e4c010c62133388ac89652105f`  
		Last Modified: Wed, 12 Jan 2022 02:41:56 GMT  
		Size: 63.8 MB (63836908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919a27f3eab379747fcb1e953cdbafe1f8abdb7d8787d8ee5255eb8af7693534`  
		Last Modified: Wed, 19 Jan 2022 22:31:30 GMT  
		Size: 59.5 MB (59542456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4618740a69a000238eb4b2ec097fcbf460764eaf90662c908f9e0e4602c6efa`  
		Last Modified: Thu, 20 Jan 2022 00:20:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223d9a8bd150ce2eeab6f350d43b89c0deb6052bdaf4b4e1e7d2411fe48d668b`  
		Last Modified: Thu, 20 Jan 2022 00:20:58 GMT  
		Size: 16.7 MB (16676458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
