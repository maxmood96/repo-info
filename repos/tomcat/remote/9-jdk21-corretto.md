## `tomcat:9-jdk21-corretto`

```console
$ docker pull tomcat@sha256:787d6326b149d253cfce37295b2f166eb25b7ef3aba8337540830b59ffdc3b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk21-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:84900448953ad267eb52b15fe13a75d0796926a161ddec746d67f0393b7ed644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246913764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08adfcf387b2e5bc8d53af2c08eb088ff14f78bdbe66dc7ab04aec1105b2fbd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:50 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:33:50 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:33:50 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:32:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 17:32:25 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 17:32:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 17:32:25 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 17:32:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:32:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:32:25 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 17:32:25 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 17:32:25 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 17:32:44 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 03 Apr 2026 17:32:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 17:32:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 17:32:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cfed88fbdc8fe99aa0cb833426754c814895b56d511b326630c5ce48040861`  
		Last Modified: Wed, 11 Mar 2026 18:34:14 GMT  
		Size: 165.5 MB (165549236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976b142bd37194ab0b417c6bb173626714b5c909ca92782aa20589dfd2ee4f4c`  
		Last Modified: Fri, 03 Apr 2026 17:32:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b8cf336360b6361021572a6c30c0c5480c7f60e02518a0aa15dcf09f4d073e`  
		Last Modified: Fri, 03 Apr 2026 17:32:56 GMT  
		Size: 18.4 MB (18407815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:c9c4a7cb13565518930cf320ffed2bae1fb56f6b449f3d8e9f416435f2d9b911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5631614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea3395307ee46616f8e917496239bc084697bde76bb1cddedc0b1460886c123`

```dockerfile
```

-	Layers:
	-	`sha256:de7b608a459b9777bd6ec392a20afb51f142f881b544a07834a6f99b5e4d2709`  
		Last Modified: Fri, 03 Apr 2026 17:32:56 GMT  
		Size: 5.6 MB (5602411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee64f761ec241ac9e3ed8610d32656c98ecd19581e4ffffca38261f362cc302`  
		Last Modified: Fri, 03 Apr 2026 17:32:55 GMT  
		Size: 29.2 KB (29203 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:59b372e0d96c0c7ee03b96b15b7784010e09c51a249a878a24eba0938304bb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246744299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9e5a6b7f67ff4f03acea512a6b7387045a65e7e012ca4e14ee9e67b38f3c4f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:22 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:33:22 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:33:22 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:34:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 17:34:45 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 17:34:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 17:34:45 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 17:34:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:34:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 17:34:45 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 17:34:45 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 17:34:45 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 17:35:05 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 03 Apr 2026 17:35:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 17:35:05 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 17:35:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed568f4d62eac4bc11a392a36c1d1ebf9f9574527b3d72f9d4c88b9a749d26`  
		Last Modified: Wed, 11 Mar 2026 18:33:45 GMT  
		Size: 163.6 MB (163600514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9801b492b2d6127a360a683fc9b45e303c1bbf72ef6f896c00b757d2271fb05`  
		Last Modified: Fri, 03 Apr 2026 17:35:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d384fa8817523243341ae2c25a31228810c7ba4aaf8d86ffeee31556e9cadcd`  
		Last Modified: Fri, 03 Apr 2026 17:35:18 GMT  
		Size: 18.3 MB (18340433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:8e51bbc4f95ca2052b1e1bc29273e8c9701a59653125110070c800ff78985b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d1711f10aac61dd92874d4d8466327d1470a21a705e81190fd8043f3f7203`

```dockerfile
```

-	Layers:
	-	`sha256:2ee00bb112dc86c411aac215900d6c6264fc8bb56f65ae73ae4782153bdfc14a`  
		Last Modified: Fri, 03 Apr 2026 17:35:17 GMT  
		Size: 5.6 MB (5601076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8cd18292a93a58b1dd409275391f3e551643eb9d47b7a866266fe79a53d8f1`  
		Last Modified: Fri, 03 Apr 2026 17:35:16 GMT  
		Size: 29.4 KB (29361 bytes)  
		MIME: application/vnd.in-toto+json
