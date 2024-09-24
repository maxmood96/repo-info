## `tomcat:9-jdk17-corretto-al2`

```console
$ docker pull tomcat@sha256:2207324e3451780529b53a3e339c4a58d8af75262f67f482f433ccaad861466d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk17-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:09c8742c2e32ab75a0fc13180f3b6a39cb98a8672b84d2caa758926bfec7bb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232840305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5824f9c58f55e86b5e74a74d5d6ca69b43edcae173e69a40a84f355c4fb0bb0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Sep 2024 14:16:43 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 14:16:43 GMT
ARG version=17.0.12.7-1
# Tue, 17 Sep 2024 14:16:43 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LANG=C.UTF-8
# Tue, 17 Sep 2024 14:16:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 17 Sep 2024 14:16:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:16:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b45a8065fa810969d1a7ad2d02ce0e3de81402ebff98decd2b63731c4947a13`  
		Last Modified: Tue, 24 Sep 2024 01:56:52 GMT  
		Size: 152.2 MB (152247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa77b844a6ef89ef71ef4e39930a5527876be1cf298278d564d6ac1ba74e9175`  
		Last Modified: Tue, 24 Sep 2024 02:53:10 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59313b5fefbbbe89dd7c93e23202df3ceab9dcaa811f1a7586d227973f22c0ca`  
		Last Modified: Tue, 24 Sep 2024 02:53:10 GMT  
		Size: 17.9 MB (17914056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:ef77c853a1edd9810cc960d6f24690d290ad7539f9173394483dfc986fb3f4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 KB (27906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d93676d38d3a6c6819ab13a30e565ac96e43e097d933bf1acda09e00266cae7`

```dockerfile
```

-	Layers:
	-	`sha256:21d19e06a3368aa8329c6b2b2c3776973973127936f562afded313d95d02c1ae`  
		Last Modified: Tue, 24 Sep 2024 02:53:10 GMT  
		Size: 27.9 KB (27906 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk17-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:5402426537d9a3ae35ca1343283c187d05fc517612c854441cf64307927c9fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233406035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88781818fc1907ba7ce09434d72bfe6b225c21cee1da3befb340293cdb01abac`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Sep 2024 14:16:43 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 14:16:43 GMT
ARG version=17.0.12.7-1
# Tue, 17 Sep 2024 14:16:43 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LANG=C.UTF-8
# Tue, 17 Sep 2024 14:16:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 17 Sep 2024 14:16:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:16:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:16:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 17 Sep 2024 14:16:43 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46effa7b22d687fc510d9b6c929635519e7c4f3d222388e71564cea3659e1e`  
		Last Modified: Tue, 24 Sep 2024 02:36:02 GMT  
		Size: 150.9 MB (150865036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14525f3a8760d25e2047206a2d9acf0a55ced083bfce01f83bb4b68aa38c7c1`  
		Last Modified: Tue, 24 Sep 2024 03:15:14 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e47929192242c1180fb6908dbe44e49ca3be709ae880170e34597608a2284d`  
		Last Modified: Tue, 24 Sep 2024 03:15:14 GMT  
		Size: 18.0 MB (17954250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:67d5bdc1c35e9a87eecd2d630510f7bb2249c9e06faf38ddd7497778e65b96ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe20bbd95b236ddca30f1e408fb3af6b87009fbe46f7fe0bed229b0bd7d19fc`

```dockerfile
```

-	Layers:
	-	`sha256:6c0fdaf97c4f270b3911832e0f58c76044aa0c0dab05c442707ba026e3207edf`  
		Last Modified: Tue, 24 Sep 2024 03:15:14 GMT  
		Size: 5.6 MB (5589459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc26792d5045878dcb82ce05904325232b582821b86243b5b4e4adbaa73aee6`  
		Last Modified: Tue, 24 Sep 2024 03:15:13 GMT  
		Size: 28.5 KB (28534 bytes)  
		MIME: application/vnd.in-toto+json
