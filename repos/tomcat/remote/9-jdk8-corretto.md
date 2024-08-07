## `tomcat:9-jdk8-corretto`

```console
$ docker pull tomcat@sha256:55aa68ca4b8877aeb08486e1d86ad75e68bac2f4688bf07d4daf0131168259ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:fab919ff8aa9d2384e038ec6d505b3a6fcdbbe53e3cbb000c66d6edaaea403b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155195241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f66388b67a9088909f3897f35e5d9b11aa4f8f4db76ef9379c92495c47f738`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 08:03:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ARG version=1.8.0_422.b05-1
# Mon, 08 Jul 2024 08:03:40 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 08 Jul 2024 08:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_VERSION=9.0.91
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba3e469516848c9e5827a5c193c9649717e5fc70dc9e65985a1ab4065891012`  
		Last Modified: Thu, 25 Jul 2024 21:01:03 GMT  
		Size: 75.6 MB (75568332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b978e145752e63b9ae819714b505e53dfc2c8788b78c9ab8032b09462dc65e7`  
		Last Modified: Thu, 25 Jul 2024 22:01:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1638cc49174a3c81f57d77aa3e9a8453dad1e2986e92038385c85adefa94b071`  
		Last Modified: Thu, 25 Jul 2024 22:01:06 GMT  
		Size: 16.9 MB (16947540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:a76ed1ac04c68163948e0ecf1c01faa6c67abad9e2840b0377877a6f4ebd8d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac87c29fabbc28ca183f68124638e85098116816850efb86bd23e07ae383302`

```dockerfile
```

-	Layers:
	-	`sha256:8db1d6794e10e703b1cbc4439ab5e21d93ff5a1d8fc37d3b4392cc5cd1f1bf17`  
		Last Modified: Thu, 25 Jul 2024 22:01:05 GMT  
		Size: 5.4 MB (5430780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:111e77b90427c11e28d6d109b4e2bfe790ebac593e0c0f44dcb1888bd522173e`  
		Last Modified: Thu, 25 Jul 2024 22:01:05 GMT  
		Size: 28.1 KB (28114 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2b77224693ca84c87fe670ddcec512d6aa39d11b7239ea997e9be911c0124b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141580443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed92bf4d0e8e42c5ddaf08e624366f1fd3dd514ec3346275c79fb726a39ed3af`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7ae84cee97a8a17573116f568e78a8d7c8415a733e0ccb92185dd2e22634f9c6`  
		Last Modified: Tue, 23 Jul 2024 13:50:38 GMT  
		Size: 64.6 MB (64572700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1a293592675dedef36879a73d5ca3a5f38d1373c13888a09927e61b13d983c`  
		Last Modified: Fri, 26 Jul 2024 01:46:03 GMT  
		Size: 59.7 MB (59656039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315a5ba603a73b71af509709af98637cff9092fd519a0897ab55a3c527d8c206`  
		Last Modified: Fri, 26 Jul 2024 02:47:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ae94002d2730dc360fd3b76f051a961a0e28ef04d5ca6298350a00d62b0fd1`  
		Last Modified: Wed, 07 Aug 2024 00:22:07 GMT  
		Size: 17.4 MB (17351501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:7a978db92874e89a1fa339ea5813a298c199a5d53eb6342dcabed16b19ced5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5440246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efeb9a789c033534c113482203d8f708e4a291cf85b075f124184cd24405579`

```dockerfile
```

-	Layers:
	-	`sha256:325b071e4f6a2cb128d6df4ae4ea741d37bf971d315bafc1650815e6d69334e1`  
		Last Modified: Wed, 07 Aug 2024 00:22:07 GMT  
		Size: 5.4 MB (5411723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46b2160e3acd58e73c5dcc5591575aa80a437d8f61f1bdc06e8ed91399e9140`  
		Last Modified: Wed, 07 Aug 2024 00:22:06 GMT  
		Size: 28.5 KB (28523 bytes)  
		MIME: application/vnd.in-toto+json
