## `tomcat:10-jdk16-corretto`

```console
$ docker pull tomcat@sha256:0e4bf3e6e61a98ad87f11d1d88dbb76a8e121a3b6e204019edc682005c7ca2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk16-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:ee46e9161c63bfb845279eba02553557d19e176ad2bc7112548d20456ecb63ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237513520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718eff31fce23739ec4685c8b8d14d10c581be808c51d7072bf03f67b417cac2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:39:48 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:49 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Mon, 14 Jun 2021 23:07:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Jun 2021 23:07:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 23:07:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Jun 2021 23:07:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Jun 2021 23:07:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Jun 2021 23:07:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Jun 2021 23:07:39 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 14 Jun 2021 23:07:39 GMT
ENV TOMCAT_MAJOR=10
# Thu, 17 Jun 2021 00:22:37 GMT
ENV TOMCAT_VERSION=10.0.7
# Thu, 17 Jun 2021 00:22:37 GMT
ENV TOMCAT_SHA512=aee019d70807b6fe25e6f4e2a36a495337c8010992af7bdeedce1bc7f6affa12899257265ecb71a46e86c20f4bd6635d4dd4c014deb3e80c518c041b3e53376b
# Thu, 17 Jun 2021 00:23:22 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 17 Jun 2021 00:23:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 17 Jun 2021 00:23:24 GMT
EXPOSE 8080
# Thu, 17 Jun 2021 00:23:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d47f3a5aebc9df1b6beb67ad88ecf895637897682242d0cefb068414e38e606`  
		Last Modified: Mon, 14 Jun 2021 22:41:42 GMT  
		Size: 159.9 MB (159943483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1f0870dab29498903db5374da4c47ab4f583ebdc9cd6d6bcf1c2e267462fe`  
		Last Modified: Mon, 14 Jun 2021 23:20:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab56bfa6a4a81f9b2dbd8fe50e529f693e9ae31e6a2d842b08f519c0d3b5e91`  
		Last Modified: Thu, 17 Jun 2021 00:54:03 GMT  
		Size: 15.6 MB (15620674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe48a3dfc836a6f3d4fb87b176a45f2fc2e1307f892eec71a92b13c20d07a8`  
		Last Modified: Thu, 17 Jun 2021 00:54:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk16-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2885f653bd5308b8847a978e183db7d9aec39252a6affa4cfc2387f8c0730d98
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239007557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82c65c04a2e3e1b987e6337656e7430147072f34d02d911b490662c98cafe48`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:57:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:57:47 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Mon, 14 Jun 2021 23:24:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Jun 2021 23:24:12 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 23:24:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Jun 2021 23:24:13 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Jun 2021 23:24:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Jun 2021 23:24:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Jun 2021 23:24:13 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 14 Jun 2021 23:24:13 GMT
ENV TOMCAT_MAJOR=10
# Thu, 17 Jun 2021 00:06:02 GMT
ENV TOMCAT_VERSION=10.0.7
# Thu, 17 Jun 2021 00:06:02 GMT
ENV TOMCAT_SHA512=aee019d70807b6fe25e6f4e2a36a495337c8010992af7bdeedce1bc7f6affa12899257265ecb71a46e86c20f4bd6635d4dd4c014deb3e80c518c041b3e53376b
# Thu, 17 Jun 2021 00:06:50 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 17 Jun 2021 00:06:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 17 Jun 2021 00:06:52 GMT
EXPOSE 8080
# Thu, 17 Jun 2021 00:06:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b510dae9b488c119034982e25017574f0769cd7d8b9c193e8981a7646541d`  
		Last Modified: Mon, 14 Jun 2021 22:59:55 GMT  
		Size: 159.9 MB (159927765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a1651828373c9d4b111771d54449e54b638d20c14fe1cc251071e94f149d16`  
		Last Modified: Mon, 14 Jun 2021 23:42:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d993fd72468618d9cbbb0e5cfb12d0cc1e7caa25d59c559fa54d4cc731c22c45`  
		Last Modified: Thu, 17 Jun 2021 00:38:20 GMT  
		Size: 15.6 MB (15630959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ddd0cc07f767faf9dc6d0a9aaab9f693cfc888ace9660474321f6e580330d`  
		Last Modified: Thu, 17 Jun 2021 00:38:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
