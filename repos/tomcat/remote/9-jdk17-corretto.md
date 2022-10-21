## `tomcat:9-jdk17-corretto`

```console
$ docker pull tomcat@sha256:7b40aad051e80e14e916e3ba07b496baff31eb41a94e55a34c7f0f512801b39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk17-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:f709d1f0d8bdd0c01af3d19ad6481b1a35664ba4e0158f8319ef25ef357334cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231495361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97ca387e8d2d3af01a3c29929e1023663337bced6ca2749504824bfd48ce04b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Oct 2022 23:39:17 GMT
ARG version=17.0.5.8-1
# Tue, 18 Oct 2022 23:39:41 GMT
# ARGS: version=17.0.5.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 18 Oct 2022 23:39:42 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:39:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 19 Oct 2022 00:15:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Oct 2022 00:15:56 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Oct 2022 00:15:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 19 Oct 2022 00:15:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Oct 2022 00:15:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Oct 2022 00:15:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Oct 2022 00:18:27 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Oct 2022 00:18:27 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Oct 2022 00:18:27 GMT
ENV TOMCAT_VERSION=9.0.68
# Wed, 19 Oct 2022 00:18:27 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Wed, 19 Oct 2022 00:19:01 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 19 Oct 2022 00:19:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 19 Oct 2022 00:19:02 GMT
EXPOSE 8080
# Wed, 19 Oct 2022 00:19:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486602f99185d0011bd962a8c14ef9d91283e5d01bb405bdd2817f7245c9fd00`  
		Last Modified: Tue, 18 Oct 2022 23:49:29 GMT  
		Size: 151.9 MB (151908568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d5d3027c84944d77bac8bbb1f519b9797e763ecf9c8ce438c7bb618770654b`  
		Last Modified: Wed, 19 Oct 2022 00:28:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afaffcf8afb9ba38c160bd652bb1f464538c5110e980ac98b0b09a6f0e27f62e`  
		Last Modified: Wed, 19 Oct 2022 00:29:39 GMT  
		Size: 17.3 MB (17283219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcf96c81b383fd09b96b66e1352120d6712c5da78ff84ada43a59d52ac6be57`  
		Last Modified: Wed, 19 Oct 2022 00:29:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:8a7e76f18cb3a93b9a2ec41b3dc703c3377a54d9a839ebe800b33e1a11a2c8d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230763540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb54140bee5402d0d569867fe9b900ad5d1ac2b9df9a18091b611affcd97afe6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 20 Oct 2022 23:39:31 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Thu, 20 Oct 2022 23:39:32 GMT
CMD ["/bin/bash"]
# Thu, 20 Oct 2022 23:57:31 GMT
ARG version=17.0.5.8-1
# Thu, 20 Oct 2022 23:57:44 GMT
# ARGS: version=17.0.5.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Oct 2022 23:57:44 GMT
ENV LANG=C.UTF-8
# Thu, 20 Oct 2022 23:57:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 21 Oct 2022 00:19:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 21 Oct 2022 00:19:09 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 00:19:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 21 Oct 2022 00:19:11 GMT
WORKDIR /usr/local/tomcat
# Fri, 21 Oct 2022 00:19:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 21 Oct 2022 00:19:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 21 Oct 2022 00:22:15 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 21 Oct 2022 00:22:15 GMT
ENV TOMCAT_MAJOR=9
# Fri, 21 Oct 2022 00:22:16 GMT
ENV TOMCAT_VERSION=9.0.68
# Fri, 21 Oct 2022 00:22:17 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Fri, 21 Oct 2022 00:22:39 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 21 Oct 2022 00:22:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 21 Oct 2022 00:22:41 GMT
EXPOSE 8080
# Fri, 21 Oct 2022 00:22:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4b86a67353b4b65e18bc95d2367be3609d9232f9e4c9ab74c8b5279c04d6c2`  
		Last Modified: Fri, 21 Oct 2022 00:00:44 GMT  
		Size: 150.4 MB (150442266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9119b338e732ce98fdcba6aba065d6a02d06876458a8b3a7bd86ec3c2acc5a`  
		Last Modified: Fri, 21 Oct 2022 00:37:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7db21806d611ea6c27dca6aba19a3d5e0855077c13cb35260fe35df3da6e0a`  
		Last Modified: Fri, 21 Oct 2022 00:38:41 GMT  
		Size: 16.4 MB (16401267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
