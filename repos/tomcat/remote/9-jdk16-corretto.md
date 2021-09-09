## `tomcat:9-jdk16-corretto`

```console
$ docker pull tomcat@sha256:4ef2e9a528c21130b041af72fe7aa15306264b6f766a0fc593c86cb4ad7e62b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk16-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:c3e3000e34ef9f14fe37526380e50515ac37b291d4cb5940ee97447cf0405d48
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238880441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d971bc9e4e17212bbf2f72d0bab0186022f0676a58bf60f686f5400462c05ed`
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
# Thu, 09 Sep 2021 01:36:06 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 09 Sep 2021 01:36:07 GMT
ENV TOMCAT_MAJOR=9
# Thu, 09 Sep 2021 01:36:07 GMT
ENV TOMCAT_VERSION=9.0.52
# Thu, 09 Sep 2021 01:36:07 GMT
ENV TOMCAT_SHA512=35e007e8e30e12889da27f9c71a6f4997b9cb5023b703d99add5de9271828e7d8d4956bf34dd2f48c7c71b4f8480f318c9067a4cd2a6d76eaae466286db4897b
# Thu, 09 Sep 2021 01:36:41 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 09 Sep 2021 01:36:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 09 Sep 2021 01:36:43 GMT
EXPOSE 8080
# Thu, 09 Sep 2021 01:36:43 GMT
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
	-	`sha256:0cb2dbf2e9870bc41cda8d3c8a6c65eb36e8f899519b0cce32ce1d5138bb7c1b`  
		Last Modified: Thu, 09 Sep 2021 01:54:45 GMT  
		Size: 16.9 MB (16909949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a65d1b14ea8bf09c0ae7ddcf515411fe80eeba68ac1d8b25a70097539cbe5`  
		Last Modified: Thu, 09 Sep 2021 01:54:42 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk16-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:809136da900c246ca7cc5872d08adf1e190b6f17a97e292f145d669c78a34f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240295340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85283e920b6aebdd3cba26c1255b6e9ccdb78a4f52dd828f1b0b932e3d865fe`
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
# Thu, 09 Sep 2021 01:26:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 09 Sep 2021 01:26:54 GMT
ENV TOMCAT_MAJOR=9
# Thu, 09 Sep 2021 01:26:54 GMT
ENV TOMCAT_VERSION=9.0.52
# Thu, 09 Sep 2021 01:26:54 GMT
ENV TOMCAT_SHA512=35e007e8e30e12889da27f9c71a6f4997b9cb5023b703d99add5de9271828e7d8d4956bf34dd2f48c7c71b4f8480f318c9067a4cd2a6d76eaae466286db4897b
# Thu, 09 Sep 2021 01:27:29 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 09 Sep 2021 01:27:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 09 Sep 2021 01:27:31 GMT
EXPOSE 8080
# Thu, 09 Sep 2021 01:27:31 GMT
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
	-	`sha256:89ff26333cdf1b15135fb497414d2ab6d72f80196055341f694255b7f69ec70c`  
		Last Modified: Thu, 09 Sep 2021 01:59:35 GMT  
		Size: 16.9 MB (16920098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fc3ae7b4ce562f19f1421d3e317af4cef4edbbb3cc8c821926355886458813`  
		Last Modified: Thu, 09 Sep 2021 01:59:33 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
