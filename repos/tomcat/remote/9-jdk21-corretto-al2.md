## `tomcat:9-jdk21-corretto-al2`

```console
$ docker pull tomcat@sha256:27a90e94d35a88afa2c23413f816c61761807267a60957afd10322376149da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk21-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:f3fd9ff5c8d53ae0d9df1b93c37a29d95fb5c3603518009d9f4554217f73b456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245279866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1fd169821cccbb885b765136ef31187cfe9d34bb27b322c7978994bf2f56f8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 01 Feb 2024 23:54:01 GMT
COPY dir:2df8955a095aec5442eb78c5eb2b2d5ec8efe73514e149ef530142d09c10ab53 in / 
# Thu, 01 Feb 2024 23:54:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:45:21 GMT
ARG version=21.0.2.13-1
# Fri, 02 Feb 2024 00:45:48 GMT
# ARGS: version=21.0.2.13-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 02 Feb 2024 00:45:48 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:45:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 02 Feb 2024 12:25:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Feb 2024 12:25:52 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 12:25:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Feb 2024 12:25:53 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Feb 2024 12:25:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 12:25:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 12:25:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Feb 2024 12:25:53 GMT
ENV TOMCAT_MAJOR=9
# Wed, 21 Feb 2024 01:07:54 GMT
ENV TOMCAT_VERSION=9.0.86
# Wed, 21 Feb 2024 01:07:54 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Wed, 21 Feb 2024 01:08:31 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 21 Feb 2024 01:08:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Feb 2024 01:08:33 GMT
EXPOSE 8080
# Wed, 21 Feb 2024 01:08:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7c46e61fc0317cccadde1288fd50789f5fcc06bddf47082f5ba5894613f35b38`  
		Last Modified: Thu, 01 Feb 2024 03:07:26 GMT  
		Size: 62.6 MB (62646486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aa8a7b34d9d00065712ed12b31cb2ce237d67023e031cf6617677322aff470`  
		Last Modified: Fri, 02 Feb 2024 00:55:32 GMT  
		Size: 165.7 MB (165679845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b5db1e9c138be068b710331c0f4fa9ff33326226f600125beabae79c5d6907`  
		Last Modified: Fri, 02 Feb 2024 12:50:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2c054689ec107c91195b026944f6f192cc00da54f2c072e1e445bef8473473`  
		Last Modified: Wed, 21 Feb 2024 01:33:47 GMT  
		Size: 17.0 MB (16953231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7c80081936142da147877adbf361f48ef3448885ea9b84b752d0ef79caf3c3`  
		Last Modified: Wed, 21 Feb 2024 01:33:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk21-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e642f58c14b6a00b61134b49ccb24b628ac1d623be993993305972538501ad96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245050036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f79e13189de39fb70dcada4707c6ba8f296bca26151de42311efd98cbed32e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:29 GMT
COPY dir:ed6a811a4137d0b4591f2c9dabfdd849cb878c3501af91aa79c89a2e9f4479d5 in / 
# Mon, 26 Feb 2024 23:06:30 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:43:15 GMT
ARG version=21.0.2.13-1
# Mon, 26 Feb 2024 23:43:38 GMT
# ARGS: version=21.0.2.13-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Feb 2024 23:43:40 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:43:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Feb 2024 00:14:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 27 Feb 2024 00:14:54 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 00:14:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 27 Feb 2024 00:14:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 27 Feb 2024 00:14:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 27 Feb 2024 00:14:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 27 Feb 2024 00:14:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 27 Feb 2024 00:14:55 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Feb 2024 00:14:55 GMT
ENV TOMCAT_VERSION=9.0.86
# Tue, 27 Feb 2024 00:14:55 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Tue, 27 Feb 2024 00:15:26 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Tue, 27 Feb 2024 00:15:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Feb 2024 00:15:28 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 00:15:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:53f483bd5fa48049d6551a641e547b302df82b17493915161f3f62020b3648fa`  
		Last Modified: Mon, 26 Feb 2024 23:07:06 GMT  
		Size: 64.4 MB (64445079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88582ffbd571b9c14e7f71c16c2b5d9e93690fdd9a50455dcdffcb4aa7dbf04`  
		Last Modified: Mon, 26 Feb 2024 23:52:05 GMT  
		Size: 163.7 MB (163668212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b510053ae4bfdb313ee0e23d922411ac916e51e9b1a28bfe991c0c961dadb3`  
		Last Modified: Tue, 27 Feb 2024 00:23:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d35ee5c77347464c9e75c0836c8028be7fe8e3ddeb64e17ee0161c2fe93c87`  
		Last Modified: Tue, 27 Feb 2024 00:23:16 GMT  
		Size: 16.9 MB (16936440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3709080a262bbc5dc6f33b306532ba52dce7f8d7be12da99ce005c4a8882174`  
		Last Modified: Tue, 27 Feb 2024 00:23:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
