## `tomcat:9-jdk8-corretto`

```console
$ docker pull tomcat@sha256:6565c0586dc0ba44e2077db589cebf84dc77872a6a043ca54a20b4eaaca6d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:119c32a2433bfab276de501b8f024843d9f994110cd160ac389816b3c440dbdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155134204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b77044f21036e92c1cee5337e17a5f84386e32e594e89078a817b944c4a0c80`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 21 Nov 2023 03:21:54 GMT
COPY dir:ddf8ce4c235ebf92718d40c0041035b283a61cbd94b49610e57999ebc78d3ec6 in / 
# Tue, 21 Nov 2023 03:21:55 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 04:13:06 GMT
ARG version=1.8.0_392.b08-1
# Tue, 21 Nov 2023 04:13:26 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 21 Nov 2023 04:13:26 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 04:13:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 21 Nov 2023 04:52:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 21 Nov 2023 04:52:56 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 04:52:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 21 Nov 2023 04:52:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 21 Nov 2023 04:52:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 21 Nov 2023 04:52:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 21 Nov 2023 04:52:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 21 Nov 2023 04:52:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 13 Dec 2023 02:10:05 GMT
ENV TOMCAT_VERSION=9.0.84
# Wed, 13 Dec 2023 02:10:05 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Wed, 13 Dec 2023 02:10:42 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 13 Dec 2023 02:10:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:10:44 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:10:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0b4a6f011995244a95bff79a1298e83d230bc0aa22871a9c510745cafebec227`  
		Last Modified: Sun, 19 Nov 2023 03:18:53 GMT  
		Size: 62.6 MB (62641917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae07246600142ccbbcc800cb9ff3d5e4aacfeeaee4985a2a51b0d5701e949add`  
		Last Modified: Tue, 21 Nov 2023 04:25:47 GMT  
		Size: 75.6 MB (75565497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc315ec11257be260093e8d2ffa1a99b64865b58e79d59bd4e20f719b03e226d`  
		Last Modified: Tue, 21 Nov 2023 05:01:27 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3262d3c8c1d13613390bbe9c79bcb85c141ca0354ba2fcfdfcc1776f1363456`  
		Last Modified: Wed, 13 Dec 2023 02:33:27 GMT  
		Size: 16.9 MB (16926485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697bfbe55dd166c8a3d18dc4dec1d7914e3e04381f5feae093086704cba61709`  
		Last Modified: Wed, 13 Dec 2023 02:33:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2c6ec82a64abdf5ab1efb123fc7677071e72b1dc8bc7684b82edd0dfd51845ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140950367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0894b4d9dfc1bbd746185ffb5938488f318adf707f39a6a5df54d52096c1cd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 21 Nov 2023 03:39:49 GMT
COPY dir:21fc61c0ea1d6a14f556bdbd5029389644807e82a8de54f60438fc773e3e2465 in / 
# Tue, 21 Nov 2023 03:39:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 05:07:17 GMT
ARG version=1.8.0_392.b08-1
# Tue, 21 Nov 2023 05:07:33 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 21 Nov 2023 05:07:34 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 05:07:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 21 Nov 2023 06:05:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 21 Nov 2023 06:05:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 06:05:37 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 21 Nov 2023 06:05:37 GMT
WORKDIR /usr/local/tomcat
# Tue, 21 Nov 2023 06:05:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 21 Nov 2023 06:05:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 21 Nov 2023 06:05:38 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 21 Nov 2023 06:05:38 GMT
ENV TOMCAT_MAJOR=9
# Wed, 13 Dec 2023 02:01:28 GMT
ENV TOMCAT_VERSION=9.0.84
# Wed, 13 Dec 2023 02:01:28 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Wed, 13 Dec 2023 02:01:57 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 13 Dec 2023 02:01:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:01:58 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:01:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ae50e077554aa1fe734206cc35e32dc0b0389a0ff7aa8d08626157b225100b42`  
		Last Modified: Mon, 20 Nov 2023 21:52:59 GMT  
		Size: 64.4 MB (64424056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160dfbe52864e04eeb262b852654036b29f9f36f0539a0445f6a74ac7f07b93e`  
		Last Modified: Tue, 21 Nov 2023 05:16:54 GMT  
		Size: 59.6 MB (59615560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703505077a886d5f14452eddf7d9d0253b40c5114609f756ec5575f31b19cb51`  
		Last Modified: Tue, 21 Nov 2023 06:12:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbd5791ab3f909b9c2f48ac4b658e2c6d7ac374566679f43dfe32b057c1973d`  
		Last Modified: Wed, 13 Dec 2023 02:23:18 GMT  
		Size: 16.9 MB (16910446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7bbea0b478e0bc8c4705f6f9dccf01139f3724779b651d95433bf2c8eb7045`  
		Last Modified: Wed, 13 Dec 2023 02:23:17 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
