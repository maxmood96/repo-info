## `tomcat:9-jdk8-corretto-al2`

```console
$ docker pull tomcat@sha256:f00ffa62935644128f31fede426c33ea1348d0659eaa32aa359474a5713d0dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk8-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:bc86ce8d63b2a8b420663e0e468191539653e4089021ef6159a456a8c69553a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154847974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6219573bf162d8acf40de8e53d268f9caeac2763bfa3f9ba99427e6af0fd5cb6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:59:12 GMT
COPY dir:a1cfeec8f9b5a4b857222f4bbc7f5fb80ef351168a5f48841d4545523a0a3e1c in / 
# Mon, 07 Aug 2023 19:59:13 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:49:33 GMT
ARG version=1.8.0_382.b05-1
# Mon, 07 Aug 2023 20:49:54 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:49:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 07 Aug 2023 22:19:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 07 Aug 2023 22:19:42 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 22:19:43 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 07 Aug 2023 22:19:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 07 Aug 2023 22:19:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 22:19:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 22:19:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 07 Aug 2023 22:19:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 15 Aug 2023 23:56:33 GMT
ENV TOMCAT_VERSION=9.0.79
# Tue, 15 Aug 2023 23:56:33 GMT
ENV TOMCAT_SHA512=7a0d99b5fc37c9e9ac26b554fab9147ce0a2ba59fad41e2565b15e9f6e137bf0105f5c9cd6b7b508837ff24feb7b95b2aba49e0abc7b1480a30a11606e79802a
# Tue, 15 Aug 2023 23:57:11 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Tue, 15 Aug 2023 23:57:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 15 Aug 2023 23:57:12 GMT
EXPOSE 8080
# Tue, 15 Aug 2023 23:57:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c0184eb4a5d5dddba3605f9adcde7e4af58050e9e4ed44751e74957c2ad0f1b4`  
		Last Modified: Tue, 01 Aug 2023 21:03:56 GMT  
		Size: 62.5 MB (62467383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997557714b4c7f4bfbeba7f8419f30a74e35de676255221cb6092e66fa0918d9`  
		Last Modified: Mon, 07 Aug 2023 21:02:00 GMT  
		Size: 75.6 MB (75565568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623eaa9ebc9747a7fdb52d0a6165d82e6e17ba765566287e94d41ed9501503c`  
		Last Modified: Mon, 07 Aug 2023 22:27:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad24b964496a69d1d8460b43b469a727fc8051e71f9fe579a5042685e36fd626`  
		Last Modified: Wed, 16 Aug 2023 00:19:35 GMT  
		Size: 16.8 MB (16814719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbd3a230d91a53593fbf40f0a208ffd14016953fc08adb6d6c2076c7ea2762b`  
		Last Modified: Wed, 16 Aug 2023 00:19:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk8-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9eb832f96482e1b97399c0330487bccedfddc5ea495e62ecaa41b3c0227731e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140512194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3a47f201bdbae6b8c83d054a95831539a716fee78d9bdf1ca6fb2d4021239`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:40:56 GMT
COPY dir:95dabd7a234aac70a826a1e3c0eafa3928b0be72717af1dea469f66b7db891d5 in / 
# Mon, 07 Aug 2023 19:40:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:21:31 GMT
ARG version=1.8.0_382.b05-1
# Mon, 07 Aug 2023 20:21:48 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:21:49 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:21:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 07 Aug 2023 21:44:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 07 Aug 2023 21:44:32 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 21:44:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 07 Aug 2023 21:44:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 07 Aug 2023 21:44:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 21:44:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 21:44:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 07 Aug 2023 21:44:33 GMT
ENV TOMCAT_MAJOR=9
# Mon, 07 Aug 2023 21:44:33 GMT
ENV TOMCAT_VERSION=9.0.78
# Mon, 07 Aug 2023 21:44:33 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Mon, 07 Aug 2023 21:45:01 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Mon, 07 Aug 2023 21:45:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 07 Aug 2023 21:45:02 GMT
EXPOSE 8080
# Mon, 07 Aug 2023 21:45:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c3b5a1e75067e9d540ad8d844cad5a291a8cce89e1a3ed8e0f362a5736d3030c`  
		Last Modified: Wed, 02 Aug 2023 19:26:38 GMT  
		Size: 64.1 MB (64129548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbd1cb3365e06c166f4568a7f2334e62e5e58ba9fe399ffc875b4a390d9e0e1`  
		Last Modified: Mon, 07 Aug 2023 20:33:09 GMT  
		Size: 59.6 MB (59621903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e7828233f6351a6186cc203393aa5d51ea37f516e671cd3f1c763af991ce65`  
		Last Modified: Mon, 07 Aug 2023 21:51:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6d26020c08e1f4c54ae72a259ab375fa831dd504c4123e7b33a666e56da022`  
		Last Modified: Mon, 07 Aug 2023 21:51:27 GMT  
		Size: 16.8 MB (16760438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45762a4adf588b688a28b0f90ef77cdfb5a5974c699a821e9aeba2c1305ba616`  
		Last Modified: Mon, 07 Aug 2023 21:51:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
