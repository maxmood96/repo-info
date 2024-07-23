## `tomcat:9-jdk11-corretto`

```console
$ docker pull tomcat@sha256:69323f1368b427002fe349f1ba06c35816668bea6a9667ef355dab60c90f6dea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:ec07f4a40c188ea4d4ba30a6f17666cad8dd0fec400855975b64f62726922beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228653498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8883a5470e0734c2bbafd11818e6cfb4b006668bb1803ab234ebb1b2c92c2d4b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 08:03:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ARG version=11.0.24.8-1
# Mon, 08 Jul 2024 08:03:40 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f697a63c5ecbed6b80df52f720b223f2624353098f1788b6a60c47493f15a07f`  
		Last Modified: Tue, 23 Jul 2024 00:07:29 GMT  
		Size: 148.1 MB (148142114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0011c63ee606be6f318df040492928bfe7a5911b0843e731ca18482614da2887`  
		Last Modified: Tue, 23 Jul 2024 00:59:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a242ccf28739c8bebbf6f3814232f6781a8ffba3813469ac28b9d6910ddcc8`  
		Last Modified: Tue, 23 Jul 2024 00:59:53 GMT  
		Size: 17.9 MB (17861775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk11-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:87131a4391e65caa4cd391d3a8f9e6a1adec7a1c363a7a7d23b8298931f9be4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410fe3cbfd48d3983a06bb3f67e607eee5917170833b53e54ea08e4e85fc52c6`

```dockerfile
```

-	Layers:
	-	`sha256:b22bf22445434cef54f370221e1af197c65d445853ab74ea450b293b99a618f3`  
		Last Modified: Tue, 23 Jul 2024 00:59:53 GMT  
		Size: 5.6 MB (5596483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edaad3578b075699d72f9ee823dbf6e6da9db6d93ec160961a4a8a1edb9fc25`  
		Last Modified: Tue, 23 Jul 2024 00:59:52 GMT  
		Size: 28.1 KB (28125 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:1174ccc701fb94d458239099788375d79582206b5bf9d9b25fae73119d659ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226831907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1751845d149a4cf65c415fd4c0584a78ed8ea3ffb00afe490dd3d30bfbea84`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 08:03:40 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ARG version=11.0.24.8-1
# Mon, 08 Jul 2024 08:03:40 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771241495db9d5a402a12da9e45caac55e6c6e69b34ad47de31c73a4d0d9b2b8`  
		Last Modified: Thu, 18 Jul 2024 22:52:16 GMT  
		Size: 145.3 MB (145257531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7755b33f93571a602cab1edb6268acdcbb4d71470a6da7b729eea453966f69da`  
		Last Modified: Thu, 18 Jul 2024 23:59:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7e2b9e914718861321284f4a239139b326558b7a1e9c5f69c4292ce13c35f0`  
		Last Modified: Thu, 18 Jul 2024 23:59:50 GMT  
		Size: 17.0 MB (16998862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk11-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:654f2f99c7ca28c3bfe5726c946c56d3e3ea5c871d6f266d434c539f299c284a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0e7e40acfe34a9bae0f526045d68906c41cb271d3eb8b8dc8c0e141d5c6981`

```dockerfile
```

-	Layers:
	-	`sha256:80465547a6cab704ed32fd1d643e79714fc5ed7e6c0b107a2b755b004a0a20ab`  
		Last Modified: Thu, 18 Jul 2024 23:59:49 GMT  
		Size: 5.6 MB (5595952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c6fdd6cc5c4176546e578fa027674d4d552ebb6b001c77141c054f28519511`  
		Last Modified: Thu, 18 Jul 2024 23:59:49 GMT  
		Size: 28.6 KB (28563 bytes)  
		MIME: application/vnd.in-toto+json
