## `tomcat:9-jdk11-corretto-al2`

```console
$ docker pull tomcat@sha256:9e4e906cf9c1207e343a4bb5c1e5e363193dbe1160e863330cc91fb183089bf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk11-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:1526bcaf801c9d331abd19c162500b4cb3bb0acf362d42106728cbff0b4cea1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229487859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46460008e836aeaa7d80bcbe3f783f5bcdd0b1266c113b530805dd8a1b3718e3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:07 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:07 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:07 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 03 Apr 2026 17:32:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 17:32:58 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 17:32:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 17:32:58 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 17:32:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:32:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:32:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 17:32:58 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 17:32:58 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 17:33:19 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 03 Apr 2026 17:33:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 17:33:19 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 17:33:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b20d6ad17bf5a5e6c795a6bafe254f811eb55ef5f45999fe7ad9419d1a2c4a`  
		Last Modified: Wed, 11 Mar 2026 18:32:27 GMT  
		Size: 148.1 MB (148126018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5681e97ea6d510e324a290abe2ed31fb788661b1f01da7b4fcabe1aeaab826d7`  
		Last Modified: Fri, 03 Apr 2026 17:33:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a1e352f7a58726a9356db9d48b893c31f0cdc09063149f2d234c8529a92e42`  
		Last Modified: Fri, 03 Apr 2026 17:33:30 GMT  
		Size: 18.4 MB (18405128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk11-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:03d2fb3df8d79155c40c9803d50341c9720be16b0ac020bbbd168e9f51cc47e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd033d9ad7f093d928de8eb4c51abab9080297b9ec5a748400e5d43130148c7`

```dockerfile
```

-	Layers:
	-	`sha256:c1e8395bf194800c6856f32f82bb6732ccb7d465fd7a53e901fdc97bcc094eba`  
		Last Modified: Fri, 03 Apr 2026 17:33:30 GMT  
		Size: 5.6 MB (5609813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abb7f7020840d1eb805e62db0ebfe00bb00bcf0398fb03bf043aa0f2d6d5e7e`  
		Last Modified: Fri, 03 Apr 2026 17:33:30 GMT  
		Size: 29.2 KB (29203 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk11-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b5801651507e83949bba17b14bf013995dbd822d51f3f79c2bae8dc9a9e1ba52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228354004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d89dcc250ec7a8515f88741fd768e10db34d13af8bd8c66a2f0ffd68bcca466`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:21 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:21 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:21 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 03 Apr 2026 17:35:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 17:35:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 17:35:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 17:35:28 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 17:35:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:35:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:35:28 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 17:35:28 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 17:35:28 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 17:35:49 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 03 Apr 2026 17:35:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 17:35:50 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 17:35:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7932995bd594e75f8d5178d3e3fd2c3400b84edd2f1cf6db87ccb7b6cd9e798`  
		Last Modified: Wed, 11 Mar 2026 18:32:47 GMT  
		Size: 145.2 MB (145212347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48938ae4d41f1e6db64dd4b2bf56ee466942c785eac53920ccd8504456c5dca9`  
		Last Modified: Fri, 03 Apr 2026 17:36:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a85333eca6441dd6a98305b2383c9608f5a9d9120dcd5025efe38bf1b89f77c`  
		Last Modified: Fri, 03 Apr 2026 17:36:01 GMT  
		Size: 18.3 MB (18338305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk11-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:ee708a66c412c14158b0160d75664050cd2f4a6968946b7fa7404bf78d8ace3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5638643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f33f6db66b0f66d446a13cb319eea2d0cf3712684d1152aea1c597ebdfe06a`

```dockerfile
```

-	Layers:
	-	`sha256:9fb52d8529395093269741e6b603d79d77d5be2683d3216a8bc228442216d16a`  
		Last Modified: Fri, 03 Apr 2026 17:36:01 GMT  
		Size: 5.6 MB (5609283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472af818ce8a7bea60c55a2c5852dba42960c2beb442de49c2e30ab70e74a32d`  
		Last Modified: Fri, 03 Apr 2026 17:36:00 GMT  
		Size: 29.4 KB (29360 bytes)  
		MIME: application/vnd.in-toto+json
