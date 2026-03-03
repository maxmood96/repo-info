## `tomcat:9-jdk17-corretto-al2`

```console
$ docker pull tomcat@sha256:229f6f862313a04788c0e0fdaf9d50cd65ea3b66667bc3a90e5daf58e3e5d3a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk17-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:8725ca99aee52d662483577dfb7bdf80e535d15b89207564e286a1b7179f990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233783831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb918ae17251b2f7d3d7b6016aad6faf662201bb6cb8a05e3e90ff641af42b2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:12:50 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:12:50 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:12:50 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:12:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:13:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Mar 2026 00:13:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 00:13:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Mar 2026 00:13:40 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Mar 2026 00:13:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:13:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:13:40 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Mar 2026 00:13:40 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 03 Mar 2026 00:13:40 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 03 Mar 2026 00:13:59 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 03 Mar 2026 00:14:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Mar 2026 00:14:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Mar 2026 00:14:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89257e0640a148754b27ea19438c565af935054d2354ace1f7ecc2c7e2d9b538`  
		Last Modified: Mon, 02 Mar 2026 23:13:08 GMT  
		Size: 152.5 MB (152455379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665506b32550da3ea1b25dae760f7b229ef2d56ce78ee5ab88b854e832af0e4e`  
		Last Modified: Tue, 03 Mar 2026 00:14:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ec0b8ed9ec8309558096a91aa76e37cc3cf1a0b970b87536a10dc33e097e63`  
		Last Modified: Tue, 03 Mar 2026 00:14:11 GMT  
		Size: 18.4 MB (18368020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:a789ec9067f50287122e96f8be6fa209877651e8cf5c916fd40fce76acd91a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5631711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2204f540b728ed35263da385117e3abf647f393e0f291fcfcc95ad637e1b1e`

```dockerfile
```

-	Layers:
	-	`sha256:d3ec608d0405bde606f773c2b2835609f36fcb2bd1a3bf5702bd90103590864a`  
		Last Modified: Tue, 03 Mar 2026 00:14:10 GMT  
		Size: 5.6 MB (5602508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3c4cfe7ab14136c276326156d71e5649637bbf71df63d3aea264bc4a4ae6d1`  
		Last Modified: Tue, 03 Mar 2026 00:14:10 GMT  
		Size: 29.2 KB (29203 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk17-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:90423d41bf48ea51bfae83e6a35628dc9dedb8d392196a9795e28e317749c19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234132390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f0d4811343d8925444a9c1927c81c459ab9881d910057a0be57a5388382706`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:46 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:46 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:14:46 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:14:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Mar 2026 00:14:12 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 00:14:12 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Mar 2026 00:14:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Mar 2026 00:14:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:14:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:14:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Mar 2026 00:14:12 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 03 Mar 2026 00:14:12 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 03 Mar 2026 00:14:32 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 03 Mar 2026 00:14:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Mar 2026 00:14:32 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Mar 2026 00:14:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a6f64c6c904e9ef9b020d55ef2c8e5977ab0ae43c95f0454e34c21342702b`  
		Last Modified: Mon, 02 Mar 2026 23:15:09 GMT  
		Size: 151.0 MB (150975227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9092c70b640be6292f69f0c40297e42138c4878abbe499b723fc71083d237581`  
		Last Modified: Tue, 03 Mar 2026 00:14:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418cab124493ea569a74e3a4b8bfdc13cab79d925408d18e8a7b7d8dcaa04184`  
		Last Modified: Tue, 03 Mar 2026 00:14:44 GMT  
		Size: 18.3 MB (18345549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:c976372bbdfbed0488794164e1d146582609e5999c94a25e3e395afd6a1e635b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60ad3b792f648d7ca1f150f7c190d4090b19ad98fcf3b9ff70c3b3e87138727`

```dockerfile
```

-	Layers:
	-	`sha256:1274f94648f3ff38507686f49400f3e91d56876a1f1e633edc5b0a4a3b0b500b`  
		Last Modified: Tue, 03 Mar 2026 00:14:44 GMT  
		Size: 5.6 MB (5601173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96135999244a969a008c1014430f33ee2df7e896c5ceee03d8cad59331781cf`  
		Last Modified: Tue, 03 Mar 2026 00:14:43 GMT  
		Size: 29.4 KB (29361 bytes)  
		MIME: application/vnd.in-toto+json
