## `tomcat:9-jdk8-corretto`

```console
$ docker pull tomcat@sha256:f47bd471f2d975f5be3eb7116b17faacce79f2adfd2f7e16b68a8493f5b13c37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:3a16822beb32da0d30f32ed0c366eea7c6adacc0503a564144b4cacc447d7ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157475463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a949c70a705d5a6994748d02ca844e0fd5ee65c233b52aa4d8566a8f26c851`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:08:53 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:08:53 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:08:53 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:08:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 03 Mar 2026 00:13:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Mar 2026 00:13:41 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 00:13:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Mar 2026 00:13:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Mar 2026 00:13:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:13:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:13:41 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Mar 2026 00:13:41 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 03 Mar 2026 00:13:41 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 03 Mar 2026 00:14:02 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 03 Mar 2026 00:14:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Mar 2026 00:14:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Mar 2026 00:14:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8671a46cd97cb565ae682f62b0c2f1c346eb6aa7a6c1b32d27ef14bee0510a9`  
		Last Modified: Mon, 02 Mar 2026 23:09:08 GMT  
		Size: 76.1 MB (76136766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b848412e78e226e6c903decb0a26935da9a10c022db1751f2a19b37435b5b8`  
		Last Modified: Tue, 03 Mar 2026 00:14:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abca2070f33baceb846780e7f5ca2f882c1cc67aae09e5dda536f74982d2eaf`  
		Last Modified: Tue, 03 Mar 2026 00:14:14 GMT  
		Size: 18.4 MB (18378265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:43518351493f8ff25c0c9b6d1e553a64031d5a826a55a6245768d385e03f067c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8569d5aa3bcdcefe5793feb3347b050157b73fa0aa73c94a08379a9decd864b9`

```dockerfile
```

-	Layers:
	-	`sha256:b6c026f4d130ef1d560a90e92fd0c6add9c112bd0c2fc24d4e32a42a9fd668a6`  
		Last Modified: Tue, 03 Mar 2026 00:14:14 GMT  
		Size: 5.4 MB (5443858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d6f34aee945db6290bcaa36a1d8260655701dcb736bba219dc5e53be0e259e`  
		Last Modified: Tue, 03 Mar 2026 00:14:13 GMT  
		Size: 29.2 KB (29192 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b608d28f1e878beb5ab2f0f7b7394437aa5f010580c9fda0a8f3da496e639d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143078730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d27a00f274f3f93df721321a83fc41aa125a655aa98adbdce66b8efb0e186a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:09:16 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:09:16 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:09:16 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:09:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 03 Mar 2026 00:14:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Mar 2026 00:14:18 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 00:14:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Mar 2026 00:14:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Mar 2026 00:14:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:14:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Mar 2026 00:14:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Mar 2026 00:14:18 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 03 Mar 2026 00:14:18 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 03 Mar 2026 00:14:37 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 03 Mar 2026 00:14:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Mar 2026 00:14:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Mar 2026 00:14:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb8ebfe61a3b23e04e4a22e0eed5f6ba1100ebbc43ae35b9af41c612940a6d5`  
		Last Modified: Mon, 02 Mar 2026 23:09:30 GMT  
		Size: 59.9 MB (59925205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1c10e17d19534a7519d7f20d74df3a4c204daa1a2bfaddb56f02973c9ec8b1`  
		Last Modified: Tue, 03 Mar 2026 00:14:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424421f2d9fd3a94db91a6d48a7182db9b7a2edf73bf2086272fb6aea73b6e3c`  
		Last Modified: Tue, 03 Mar 2026 00:14:48 GMT  
		Size: 18.3 MB (18341912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:ae55c219276dd3bdfc655ada837183fe6a0de8e388de093a9371268599832468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b5cfd798503cf2516f82a6e3f8a8582620c6cf7b643af8ca5e66c0bfc6e80`

```dockerfile
```

-	Layers:
	-	`sha256:2ff47b703801667e8a412615f1a108981aca373c2fb871851d3eae607ab23123`  
		Last Modified: Tue, 03 Mar 2026 00:14:47 GMT  
		Size: 5.4 MB (5422321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a64ac56416fd1943e9caaba7bd0c1a512e981a124223bdbc128eec52c7cd22`  
		Last Modified: Tue, 03 Mar 2026 00:14:47 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.in-toto+json
