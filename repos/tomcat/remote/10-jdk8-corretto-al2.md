## `tomcat:10-jdk8-corretto-al2`

```console
$ docker pull tomcat@sha256:778ed9b8f8f6c908ad1b891c9efc1f8eed892ba3a343d81c7ad5d4760a6afbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk8-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:ea8919355eee5de812fd9ca293b4da85c2d192ecb759d108c92bd8ed8ead9731
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154707321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480d32b40598ddd8bbe3ec773a4ac677f205464e61c6d09721d19dadc0739`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Aug 2022 01:19:36 GMT
ADD file:ebfd33425a17b16a9e560de15c91108bf2ee740f284a1482a7105b420ff22678 in / 
# Fri, 26 Aug 2022 01:19:37 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 02:02:55 GMT
ARG version=1.8.0_342.b07-4
# Fri, 26 Aug 2022 02:03:17 GMT
# ARGS: version=1.8.0_342.b07-4
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 02:03:18 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 02:03:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 26 Aug 2022 02:33:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Aug 2022 02:33:53 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 02:33:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 26 Aug 2022 02:33:53 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Aug 2022 02:33:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 02:33:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 02:33:54 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 26 Aug 2022 02:33:54 GMT
ENV TOMCAT_MAJOR=10
# Fri, 26 Aug 2022 02:33:54 GMT
ENV TOMCAT_VERSION=10.0.23
# Fri, 26 Aug 2022 02:33:54 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Fri, 26 Aug 2022 02:34:27 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 26 Aug 2022 02:34:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 26 Aug 2022 02:34:28 GMT
EXPOSE 8080
# Fri, 26 Aug 2022 02:34:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fd06b60db4951fd95b43a9e73fb084fe7d2afcd4ff464472ead5548cd1c28717`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 62.3 MB (62326701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6626eeeb161e510cb277ee5c8edd4e8c33de2e80145c25c54050fc21e1d357e2`  
		Last Modified: Fri, 26 Aug 2022 02:07:06 GMT  
		Size: 75.6 MB (75579879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92457f0aa10a1bc67abf89502674c69221acdf4ca91433b39dd433f68db729e`  
		Last Modified: Fri, 26 Aug 2022 02:46:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7986113585734a7888725af6d1cf0d617c2dc803a61010be39b9f5551ce76e6a`  
		Last Modified: Fri, 26 Aug 2022 02:46:24 GMT  
		Size: 16.8 MB (16800435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6102e80610df0be8b38576df1873bb376c9c25625d578726df159edc1ad35`  
		Last Modified: Fri, 26 Aug 2022 02:46:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk8-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3073b96e7fff4540919b4ba198841223240b1df691862588cc80c45ab8d99d4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140322820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ede86db79e11045748dde64d31450c2e06f52c3f856340adf0a05f59fbe06`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 01:01:01 GMT
ARG version=1.8.0_342.b07-4
# Fri, 26 Aug 2022 01:01:18 GMT
# ARGS: version=1.8.0_342.b07-4
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 01:01:18 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 01:01:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 26 Aug 2022 01:47:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Aug 2022 01:47:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 01:47:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 26 Aug 2022 01:47:18 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Aug 2022 01:47:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 01:47:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Aug 2022 01:47:21 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 26 Aug 2022 01:47:22 GMT
ENV TOMCAT_MAJOR=10
# Fri, 26 Aug 2022 01:47:23 GMT
ENV TOMCAT_VERSION=10.0.23
# Fri, 26 Aug 2022 01:47:24 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Fri, 26 Aug 2022 01:47:44 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 26 Aug 2022 01:47:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 26 Aug 2022 01:47:46 GMT
EXPOSE 8080
# Fri, 26 Aug 2022 01:47:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851b3384c6fc6a4bb8506747a4edc13e891c8719d6ac5f3e846350bc2080b93b`  
		Last Modified: Fri, 26 Aug 2022 01:03:31 GMT  
		Size: 59.6 MB (59602242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbe0f06daba876088e0e9383744a8ab0f2385905b2b1f2bb8a9c9595e0afe67`  
		Last Modified: Fri, 26 Aug 2022 02:06:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88274198904f96750dad6aab7e2ba6662e65de5e9d852fad177b6f8317264c06`  
		Last Modified: Fri, 26 Aug 2022 02:06:20 GMT  
		Size: 16.8 MB (16781675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
