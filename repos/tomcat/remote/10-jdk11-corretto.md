## `tomcat:10-jdk11-corretto`

```console
$ docker pull tomcat@sha256:2b704bb35292512cea1e4dff8f278fa5fe93a4359b1b81e8474a52a016b76ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:849964eef9a3dbe8190f61aea0fdcbfa0339b1b249e19e092c01a5e539896ccd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225891352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2b0af7690e8bf21c0ecf350ac5a3bb2b023dd35291f6a625daa29f1a189857`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:33:07 GMT
ARG version=11.0.11.9-1
# Fri, 16 Jul 2021 00:33:30 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Jul 2021 00:33:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jul 2021 00:33:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Jul 2021 00:53:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jul 2021 00:53:19 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jul 2021 00:53:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Jul 2021 00:53:20 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jul 2021 00:53:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jul 2021 00:53:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jul 2021 00:53:21 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Jul 2021 00:53:21 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Jul 2021 00:53:21 GMT
ENV TOMCAT_VERSION=10.0.8
# Fri, 16 Jul 2021 00:53:22 GMT
ENV TOMCAT_SHA512=188fb84f86ae5f5b88ddbe6f38c8dec6ec733a5ef166c5875e1c6728701e49f9d01f494a419186fd8da80ab21576e0a056382d59f7fe17695c4ec63aaf543897
# Fri, 16 Jul 2021 00:53:59 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 16 Jul 2021 00:54:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Jul 2021 00:54:01 GMT
EXPOSE 8080
# Fri, 16 Jul 2021 00:54:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a3fc4711644454fbc9851b78f9c371b21a34549e0c5cfb9136c6faaef71e7c`  
		Last Modified: Fri, 16 Jul 2021 00:35:28 GMT  
		Size: 146.7 MB (146678002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154b581e90dc4d80f6b3eaf57a0036d79ba02004e47a773a421abd11fd4415f9`  
		Last Modified: Fri, 16 Jul 2021 01:05:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89af0a712e5dd2a603750e54d1402d80814430baa50083df4b26cfecdd69caea`  
		Last Modified: Fri, 16 Jul 2021 01:05:56 GMT  
		Size: 17.2 MB (17247041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ff7167bcdb088c75cba03fe8da246814c39b9a027e80dc54349b9208b5d0a7`  
		Last Modified: Fri, 16 Jul 2021 01:05:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9c3ab2c86a2e1902519eeceb48083fada7bb1a6c266651deb1605bcf11e352b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225520724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0b776a7a0a51358fd79411552e4f9cec2502f7456933efdbae75930d619c9e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:39:30 GMT
ARG version=11.0.11.9-1
# Fri, 16 Jul 2021 00:39:58 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Jul 2021 00:39:58 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jul 2021 00:39:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Jul 2021 01:13:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jul 2021 01:13:54 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jul 2021 01:13:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Jul 2021 01:13:55 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jul 2021 01:13:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jul 2021 01:13:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jul 2021 01:13:55 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Jul 2021 01:13:56 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Jul 2021 01:13:56 GMT
ENV TOMCAT_VERSION=10.0.8
# Fri, 16 Jul 2021 01:13:56 GMT
ENV TOMCAT_SHA512=188fb84f86ae5f5b88ddbe6f38c8dec6ec733a5ef166c5875e1c6728701e49f9d01f494a419186fd8da80ab21576e0a056382d59f7fe17695c4ec63aaf543897
# Fri, 16 Jul 2021 01:14:34 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 16 Jul 2021 01:14:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Jul 2021 01:14:36 GMT
EXPOSE 8080
# Fri, 16 Jul 2021 01:14:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c303754cf668ab4480ec5b49db7d581120ef9d4abe16449f1dbe54eaec133f`  
		Last Modified: Fri, 16 Jul 2021 00:42:05 GMT  
		Size: 144.8 MB (144752643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d590d52062c419d9cc144adfc74581c608fac1e821501df6a2c54ffea3c3ba2`  
		Last Modified: Fri, 16 Jul 2021 01:31:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0177bc038973d65239bb35a3270ae894dc52e80517d5ed7e04fed61c43910ad3`  
		Last Modified: Fri, 16 Jul 2021 01:31:06 GMT  
		Size: 17.2 MB (17199887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17b2dc1e28f590d1d56773c43d203f0b34ae16422e4f039c223ea94d7e11089`  
		Last Modified: Fri, 16 Jul 2021 01:31:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
