## `tomcat:9-jdk16-corretto`

```console
$ docker pull tomcat@sha256:ec2e7ba5933286c50d73c7e16d3b71c90b7961757f18ef41575a40598c37ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk16-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:4810244109d3f53bc1727182dbdac400014d2de810a2decf85fe2eae84009227
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237169311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe4af337bdee9abe6d149f8e85d65c0ae40ba7931a3c035f179bc360e06fa29`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:39:48 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:49 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Mon, 14 Jun 2021 23:07:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Jun 2021 23:07:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 23:07:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Jun 2021 23:07:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Jun 2021 23:07:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Jun 2021 23:07:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 17 Jun 2021 00:32:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 17 Jun 2021 00:32:54 GMT
ENV TOMCAT_MAJOR=9
# Thu, 17 Jun 2021 00:32:54 GMT
ENV TOMCAT_VERSION=9.0.48
# Thu, 17 Jun 2021 00:32:54 GMT
ENV TOMCAT_SHA512=9fcde76bc192c5b02b467c7fc01727ec7c72acfc207741b03a582c67565218dd9b6ea9b9cf007b5964e7794f271433f66e3452b33352b9b657cd7e2bfff08f02
# Thu, 17 Jun 2021 00:33:32 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 17 Jun 2021 00:33:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 17 Jun 2021 00:33:34 GMT
EXPOSE 8080
# Thu, 17 Jun 2021 00:33:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d47f3a5aebc9df1b6beb67ad88ecf895637897682242d0cefb068414e38e606`  
		Last Modified: Mon, 14 Jun 2021 22:41:42 GMT  
		Size: 159.9 MB (159943483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1f0870dab29498903db5374da4c47ab4f583ebdc9cd6d6bcf1c2e267462fe`  
		Last Modified: Mon, 14 Jun 2021 23:20:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d253ac05931034ec4b239cfa6a91960ae90d90a916ebe5591a698797fd722f0f`  
		Last Modified: Thu, 17 Jun 2021 00:59:09 GMT  
		Size: 15.3 MB (15276465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716ad1b6ed7d16fb4df9d3ec18cca2e19ce19325def74db7a404035f9faf0202`  
		Last Modified: Thu, 17 Jun 2021 00:59:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk16-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:4cc71346396f31d360241ae1f1b19240d99643f83fba76921d6b352242c2d7e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238657994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137e3f219de6b9d29dfdf5b654cf6c8ec4ef436a18d708aa5593054bfc3b463`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:57:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:57:47 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Mon, 14 Jun 2021 23:24:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Jun 2021 23:24:12 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 23:24:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Jun 2021 23:24:13 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Jun 2021 23:24:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Jun 2021 23:24:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 17 Jun 2021 00:14:38 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 17 Jun 2021 00:14:38 GMT
ENV TOMCAT_MAJOR=9
# Thu, 17 Jun 2021 00:14:38 GMT
ENV TOMCAT_VERSION=9.0.48
# Thu, 17 Jun 2021 00:14:39 GMT
ENV TOMCAT_SHA512=9fcde76bc192c5b02b467c7fc01727ec7c72acfc207741b03a582c67565218dd9b6ea9b9cf007b5964e7794f271433f66e3452b33352b9b657cd7e2bfff08f02
# Thu, 17 Jun 2021 00:15:24 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 17 Jun 2021 00:15:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 17 Jun 2021 00:15:26 GMT
EXPOSE 8080
# Thu, 17 Jun 2021 00:15:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b510dae9b488c119034982e25017574f0769cd7d8b9c193e8981a7646541d`  
		Last Modified: Mon, 14 Jun 2021 22:59:55 GMT  
		Size: 159.9 MB (159927765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a1651828373c9d4b111771d54449e54b638d20c14fe1cc251071e94f149d16`  
		Last Modified: Mon, 14 Jun 2021 23:42:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5532b8c5dce39eb3cadcc7eecf03c8d31ac79b30b9f826f013a5c95e9138a337`  
		Last Modified: Thu, 17 Jun 2021 00:43:30 GMT  
		Size: 15.3 MB (15281397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e57211b9a365ccc1b15d789ad3279578e4a1bc3b72cb366685aea01a9424bc5`  
		Last Modified: Thu, 17 Jun 2021 00:43:28 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
