## `tomcat:10-jdk16-corretto`

```console
$ docker pull tomcat@sha256:9892025dfc9bba5fb250070d901de72b9413683e0fd20fa2a0910a1147db82b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk16-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:c3a69791b7fe71d09c3caf34a1af46d62c2593d6e1e7cd8e800d0d026b968641
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239224783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a16f77473ff1a51a9820bf37fcd682ea5e3a6278ea066c6b5e24068247a0a0d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 01:06:14 GMT
ARG version=16.0.2.7-1
# Thu, 09 Sep 2021 01:06:35 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 09 Sep 2021 01:06:35 GMT
ENV LANG=C.UTF-8
# Thu, 09 Sep 2021 01:06:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Thu, 09 Sep 2021 01:30:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 09 Sep 2021 01:30:22 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 01:30:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 09 Sep 2021 01:30:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 09 Sep 2021 01:30:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 09 Sep 2021 01:30:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 09 Sep 2021 01:30:23 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 09 Sep 2021 01:30:23 GMT
ENV TOMCAT_MAJOR=10
# Thu, 09 Sep 2021 01:32:34 GMT
ENV TOMCAT_VERSION=10.0.10
# Thu, 09 Sep 2021 01:32:35 GMT
ENV TOMCAT_SHA512=3f6d5d292ab67348b3134c1013044c948caf5a4bf142b4e856b5ee63693a6e80994b0b4dbb3404d0fd3542fd6f7f52b4cbe404fc5a0f716ac98d68db879b7112
# Thu, 09 Sep 2021 01:33:07 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 09 Sep 2021 01:33:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 09 Sep 2021 01:33:09 GMT
EXPOSE 8080
# Thu, 09 Sep 2021 01:33:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7253b94dc9693b8579464ae8831e09e7487e1759e5c94665a32de6736cffc600`  
		Last Modified: Thu, 09 Sep 2021 01:08:26 GMT  
		Size: 160.0 MB (159969885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d053bdcc20a28557da519376f9b636478814108c6cd80e809f8d3cfa8ab4c93`  
		Last Modified: Thu, 09 Sep 2021 01:51:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350af58e1e3621a5e9729e25ef069da30032576159182ac07a6ea323c1e7c0f`  
		Last Modified: Thu, 09 Sep 2021 01:52:41 GMT  
		Size: 17.3 MB (17254291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67dc57a41ec20aad66d1ced9423f3ba8d982c419f6fe192412a4f836dba1ac2`  
		Last Modified: Thu, 09 Sep 2021 01:52:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk16-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:4b286b59a5c27101c6f3c9d331230026407474c94e1bd95012ee53125b8b5302
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240636046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea9958474ec8b69384126381b2ec63e9ad4775bd54adce619768af5a5c64d6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:58:12 GMT
ARG version=16.0.2.7-1
# Thu, 09 Sep 2021 00:58:31 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 09 Sep 2021 00:58:32 GMT
ENV LANG=C.UTF-8
# Thu, 09 Sep 2021 00:58:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Thu, 09 Sep 2021 01:18:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 09 Sep 2021 01:18:21 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 01:18:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 09 Sep 2021 01:18:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 09 Sep 2021 01:18:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 09 Sep 2021 01:18:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 09 Sep 2021 01:18:23 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 09 Sep 2021 01:18:23 GMT
ENV TOMCAT_MAJOR=10
# Thu, 09 Sep 2021 01:21:39 GMT
ENV TOMCAT_VERSION=10.0.10
# Thu, 09 Sep 2021 01:21:40 GMT
ENV TOMCAT_SHA512=3f6d5d292ab67348b3134c1013044c948caf5a4bf142b4e856b5ee63693a6e80994b0b4dbb3404d0fd3542fd6f7f52b4cbe404fc5a0f716ac98d68db879b7112
# Thu, 09 Sep 2021 01:22:13 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 09 Sep 2021 01:22:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 09 Sep 2021 01:22:14 GMT
EXPOSE 8080
# Thu, 09 Sep 2021 01:22:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c36d5e73d6e867b4f08fd0e94ddf4f1e08e282c11c7e9b493cb02269f5715`  
		Last Modified: Thu, 09 Sep 2021 01:00:43 GMT  
		Size: 159.9 MB (159944134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675073c275a83924dd2daee5185ad872af17b5c4fcb13408bc92d494c088d245`  
		Last Modified: Thu, 09 Sep 2021 01:54:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631d4fbe1c4dff6ced09c3e8da5c67b5faf2dc8b4857c682e883804979df693f`  
		Last Modified: Thu, 09 Sep 2021 01:56:23 GMT  
		Size: 17.3 MB (17260805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321ab3972b3159b94bb9d9d13afe95c26c703b062b667dd04f14e695ebd62653`  
		Last Modified: Thu, 09 Sep 2021 01:56:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
