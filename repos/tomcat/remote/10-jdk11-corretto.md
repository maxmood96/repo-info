## `tomcat:10-jdk11-corretto`

```console
$ docker pull tomcat@sha256:9774b32a120339632ee0d12d274890a085d75181b5499197acd5098e280994cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:c05883fcf28a3283239a701b341221717b5d5df258f535b9357db6e1096c4ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224237246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c432bea137f23384a49336120f0ffb8335d824304294c5160d2cb816acfba5e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:20 GMT
ADD file:3b750ce7e7425c1cb02261d65b1e301d5818cda51a80dc8ab3b915ee5ca37d4e in / 
# Tue, 30 Mar 2021 21:59:21 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 23:19:46 GMT
ARG version=11.0.11.9-1
# Tue, 20 Apr 2021 23:20:07 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Apr 2021 23:20:07 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Apr 2021 00:02:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Apr 2021 00:02:41 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Apr 2021 00:02:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Apr 2021 00:02:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Apr 2021 00:02:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:02:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:02:43 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 21 Apr 2021 00:02:43 GMT
ENV TOMCAT_MAJOR=10
# Wed, 21 Apr 2021 00:02:43 GMT
ENV TOMCAT_VERSION=10.0.5
# Wed, 21 Apr 2021 00:02:44 GMT
ENV TOMCAT_SHA512=27271e17c8daf52503490c6657c992cc150cf2942e1b0179b738f34e9aa5e1aac3c7b947c67441d17294a8f1e772a00e38e30b2135372d6ee9d71207ac7261c3
# Wed, 21 Apr 2021 00:03:18 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 21 Apr 2021 00:03:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Apr 2021 00:03:20 GMT
EXPOSE 8080
# Wed, 21 Apr 2021 00:03:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:99a21848b482c10fd4b103b7ab95e1446142e76e3dfa673efd0a23fb264ec5e5`  
		Last Modified: Tue, 30 Mar 2021 13:54:37 GMT  
		Size: 61.9 MB (61946585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdd31bd043e6363617df60f067ba94899a198403d14f6dfea1b534afdebf768`  
		Last Modified: Tue, 20 Apr 2021 23:21:57 GMT  
		Size: 146.7 MB (146668858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d1c3e814e1775a84f5270e9d7a82f279270b5d7d2272bae92641fd34ef36a4`  
		Last Modified: Wed, 21 Apr 2021 00:18:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48553ada3eb9f001435f0c55351bc286a4efdfb0ddac2cdea5d8782fa64586f1`  
		Last Modified: Wed, 21 Apr 2021 00:18:28 GMT  
		Size: 15.6 MB (15621500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc93282ead83927ea879cbedbd34f5a7ea04137d6e1e4911c1c4e474108b499`  
		Last Modified: Wed, 21 Apr 2021 00:18:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:55fc334b875e4c5b5368b7b767f5bf8897e987a68185461525cea72db68350e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224010659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66906c092b2389e06781cf9b10148d702e4613409284e816ab9b7d2b48d17f3a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:58 GMT
ADD file:540e42c4903b87925bc490b00820f555e531041d1b1fcea6ee56f4cc3bbc895d in / 
# Tue, 30 Mar 2021 22:00:02 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 23:44:08 GMT
ARG version=11.0.11.9-1
# Tue, 20 Apr 2021 23:44:36 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Apr 2021 23:44:38 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:44:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Apr 2021 00:22:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Apr 2021 00:22:30 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Apr 2021 00:22:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Apr 2021 00:22:33 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Apr 2021 00:22:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:22:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Apr 2021 00:22:35 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 21 Apr 2021 00:22:36 GMT
ENV TOMCAT_MAJOR=10
# Wed, 21 Apr 2021 00:22:37 GMT
ENV TOMCAT_VERSION=10.0.5
# Wed, 21 Apr 2021 00:22:38 GMT
ENV TOMCAT_SHA512=27271e17c8daf52503490c6657c992cc150cf2942e1b0179b738f34e9aa5e1aac3c7b947c67441d17294a8f1e772a00e38e30b2135372d6ee9d71207ac7261c3
# Wed, 21 Apr 2021 00:23:42 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 21 Apr 2021 00:23:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Apr 2021 00:23:48 GMT
EXPOSE 8080
# Wed, 21 Apr 2021 00:23:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7d8296f22a3c3f786ce15fb5be7dce44af09932e617f9a981183619985014031`  
		Last Modified: Tue, 30 Mar 2021 22:01:09 GMT  
		Size: 63.7 MB (63660038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e32310ed216770786ba120656186e1881af266bd3e84c7a7603a5dcb62fb0f`  
		Last Modified: Tue, 20 Apr 2021 23:45:58 GMT  
		Size: 144.7 MB (144746347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f47f8411de2541d4a3fa6ed46ca02df2ed23241532849ed8249af7e9f99065`  
		Last Modified: Wed, 21 Apr 2021 00:44:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e242779ae21790ec30b858e4e4f5817a33bdbda1f87f648f1f04ea5204a15db`  
		Last Modified: Wed, 21 Apr 2021 00:44:14 GMT  
		Size: 15.6 MB (15603970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79313e8d3ee67768752b1504d6a5c5361d7f01b36ef8ba2904510b1379dc9ae9`  
		Last Modified: Wed, 21 Apr 2021 00:44:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
