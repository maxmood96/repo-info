## `tomcat:10-jdk17-corretto`

```console
$ docker pull tomcat@sha256:ada4f006e3d075395978ac94708e505a69fb904375d361f80bbe292a9655adf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk17-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:f1edd18789aa42147cfc72ccd1ddefdbd3187982be8865832d69b7fcc9dfcbb7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230394344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c1d917def8227850e3beefcf0074ea338b8e3f035095b40377be94c2b4a674`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 02 Dec 2021 23:20:03 GMT
ADD file:4eca58da351122eac20ffd87e3af2c0313089cb81650bdd4c2ef95a556fb842a in / 
# Thu, 02 Dec 2021 23:20:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 21:52:54 GMT
ARG version=17.0.1.12-1
# Fri, 03 Dec 2021 21:53:16 GMT
# ARGS: version=17.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Dec 2021 21:53:17 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 21:53:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Dec 2021 22:59:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 22:59:00 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 22:59:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 22:59:01 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 22:59:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 22:59:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 22:59:02 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 03 Dec 2021 22:59:02 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Dec 2021 23:01:33 GMT
ENV TOMCAT_VERSION=10.0.13
# Fri, 03 Dec 2021 23:01:33 GMT
ENV TOMCAT_SHA512=fecfe06f38ff31e31fa43c15f2566f6fcd26bb874a9b7c0533087be81d1decd97f81eefeaca7ecb5ab2b79a3ea69ed0459adff5f9d55c05f5af45f69b0725608
# Fri, 03 Dec 2021 23:02:14 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 23:02:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 23:02:17 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 23:02:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8b8a142162d22658bdf0283afcd00a9dd216c6637943ffe5f2ba53c4e3da0bd9`  
		Last Modified: Thu, 02 Dec 2021 06:01:08 GMT  
		Size: 62.1 MB (62090346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe03da6c601647ea7971247cde273c315f9a87637e184abace3a77b9e25464e`  
		Last Modified: Fri, 03 Dec 2021 21:56:17 GMT  
		Size: 151.5 MB (151540933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f5c44e0966a200018fe3654c220c47890c5e3312b18bbb5ba40e42fb0f7c58`  
		Last Modified: Fri, 03 Dec 2021 23:21:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509658da0c85a3988e1a2b47cf7add7fd5f71f5d8b86f3a26f5af7f747b0aefa`  
		Last Modified: Fri, 03 Dec 2021 23:22:08 GMT  
		Size: 16.8 MB (16762760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d675953602a145d8039c08d727f9504ef4db4023598a346c9d24371134e6888`  
		Last Modified: Fri, 03 Dec 2021 23:22:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:866d8da162e227b90ca1ea7609ff9f341ecad595bbeaee399584f71ba1fc4c87
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230419283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e5f6eb465a21c7516fd839938aa686e522c6c7ef8f3bb8fde09516fb3564e4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 16:54:30 GMT
ARG version=17.0.1.12-1
# Fri, 03 Dec 2021 16:54:47 GMT
# ARGS: version=17.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Dec 2021 16:54:47 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 16:54:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Dec 2021 20:55:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 20:55:01 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 20:55:02 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 20:55:03 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 20:55:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 20:55:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 20:55:06 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 03 Dec 2021 20:55:07 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Dec 2021 20:58:15 GMT
ENV TOMCAT_VERSION=10.0.13
# Fri, 03 Dec 2021 20:58:15 GMT
ENV TOMCAT_SHA512=fecfe06f38ff31e31fa43c15f2566f6fcd26bb874a9b7c0533087be81d1decd97f81eefeaca7ecb5ab2b79a3ea69ed0459adff5f9d55c05f5af45f69b0725608
# Fri, 03 Dec 2021 20:58:39 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 20:58:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 20:58:41 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 20:58:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca22289d3bc8d639ce9c21bc5edc611c4a87f936cdb6557abb4af42a1d431143`  
		Last Modified: Fri, 03 Dec 2021 16:56:46 GMT  
		Size: 150.1 MB (150051510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacf78240f007d46726355107f182930ea776893398059eeec3b71f5ac4faa2`  
		Last Modified: Fri, 03 Dec 2021 21:27:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebeb4fdded030adf92dd521abe621927e5cb4bdac4a5d09e9ff540c4c8c65de0`  
		Last Modified: Fri, 03 Dec 2021 21:29:25 GMT  
		Size: 16.7 MB (16675088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
