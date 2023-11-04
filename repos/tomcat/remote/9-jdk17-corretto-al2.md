## `tomcat:9-jdk17-corretto-al2`

```console
$ docker pull tomcat@sha256:6aa83697e589c8280f540973ada9e8b489e1caad75695586c8d50431401d949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk17-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:a1de9b6f063cb84a1bab70bb4dbd3d359aa4784fc8f4c22b8abdff84a1a0e703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231491935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5b2580f53c44fd553f98051c3fe25b21ea387be76897440fd1e5a611c78940`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:53 GMT
COPY dir:3e6cf913ede7c7c09de0465c096dad9a8bea883f026db356d68f0e799e2e3847 in / 
# Fri, 03 Nov 2023 22:21:53 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:44:58 GMT
ARG version=17.0.9.8-1
# Fri, 03 Nov 2023 22:45:24 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:45:25 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:45:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 04 Nov 2023 00:02:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 04 Nov 2023 00:02:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2023 00:02:40 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 04 Nov 2023 00:02:41 GMT
WORKDIR /usr/local/tomcat
# Sat, 04 Nov 2023 00:02:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 04 Nov 2023 00:02:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 04 Nov 2023 00:02:41 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 04 Nov 2023 00:02:41 GMT
ENV TOMCAT_MAJOR=9
# Sat, 04 Nov 2023 00:02:41 GMT
ENV TOMCAT_VERSION=9.0.82
# Sat, 04 Nov 2023 00:02:41 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Sat, 04 Nov 2023 00:03:18 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Sat, 04 Nov 2023 00:03:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 04 Nov 2023 00:03:20 GMT
EXPOSE 8080
# Sat, 04 Nov 2023 00:03:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6ebddf7084e9402a3ba6cf1360703e12633f9c49f51772f99c298cd1048d728e`  
		Last Modified: Fri, 03 Nov 2023 11:40:21 GMT  
		Size: 62.6 MB (62646469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca718df3f344744fb7e718ebbf42fd14046ad4e070b72794404ef6d1b0c3e7e`  
		Last Modified: Fri, 03 Nov 2023 22:56:55 GMT  
		Size: 152.0 MB (151960814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68289a483b84535781194b9f0ff4d3e47762bcc3e1c963f96c72ef0d2b7f41d`  
		Last Modified: Sat, 04 Nov 2023 00:12:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ddeb98571766dff5269a66751b82a8fba32c4457c2293027175fafc50cb3b7`  
		Last Modified: Sat, 04 Nov 2023 00:12:51 GMT  
		Size: 16.9 MB (16884348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aef81e2ef0dd46bbfd3e4eab8f5f899acee13b62b6779feb7f274440df2fdf`  
		Last Modified: Sat, 04 Nov 2023 00:12:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk17-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e29574286864747f4e5f4c0c86b0ded1792be524524e4f4c00d7adee2e9f5808
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231752273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5a664bd625f354afc0e891dcb109d77d38cdd65b8f96236297c8686bc34028`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:00:26 GMT
ARG version=17.0.9.8-1
# Fri, 03 Nov 2023 23:00:49 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 23:00:50 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 23:00:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Nov 2023 23:48:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Nov 2023 23:48:07 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Nov 2023 23:48:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Nov 2023 23:48:08 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Nov 2023 23:48:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Nov 2023 23:48:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Nov 2023 23:48:08 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Nov 2023 23:48:08 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Nov 2023 23:48:08 GMT
ENV TOMCAT_VERSION=9.0.82
# Fri, 03 Nov 2023 23:48:08 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Fri, 03 Nov 2023 23:48:39 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Fri, 03 Nov 2023 23:48:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Nov 2023 23:48:40 GMT
EXPOSE 8080
# Fri, 03 Nov 2023 23:48:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fd1e1b089d93af373eb5127ffbef3bd59dd121a8e1aeafdff2fd334d34418`  
		Last Modified: Fri, 03 Nov 2023 23:10:36 GMT  
		Size: 150.5 MB (150521753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13995ef0085e5035c6f486c3d79e5b3da54f8686906a52d5329c3597d58b29`  
		Last Modified: Fri, 03 Nov 2023 23:56:52 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afaa5fb526ebb4c7255ffefddf4797f7c4e858a73ead7d4266089d49a81ad38c`  
		Last Modified: Fri, 03 Nov 2023 23:56:54 GMT  
		Size: 16.9 MB (16850014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2c5fff90a35b96d49f66834efcd1988bb3b6c340fef38ad43433eb082f8aa`  
		Last Modified: Fri, 03 Nov 2023 23:56:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
