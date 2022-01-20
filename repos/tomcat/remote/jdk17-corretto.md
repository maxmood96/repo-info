## `tomcat:jdk17-corretto`

```console
$ docker pull tomcat@sha256:841408c576e8558bceb4f70c4beb12084ecfa4701963ce87cae0a9fcc9a2e572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jdk17-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:e7d283065720faedf26a71d6ba9532d8fb189072ca67df3c6fe332f2b2704363
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230549564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57619b157727d3091a19c93a5de23988482fbbaf45024a4442796632f41f274e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 12 Jan 2022 02:20:04 GMT
ADD file:618cac8c5b6f6ff56ce221df12002d34997bcc996a0af3200b58db07d68be275 in / 
# Wed, 12 Jan 2022 02:20:04 GMT
CMD ["/bin/bash"]
# Wed, 19 Jan 2022 22:04:15 GMT
ARG version=17.0.2.8-1
# Wed, 19 Jan 2022 22:04:41 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 19 Jan 2022 22:04:41 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:04:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 20 Jan 2022 00:53:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 20 Jan 2022 00:53:29 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jan 2022 00:53:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 20 Jan 2022 00:53:30 GMT
WORKDIR /usr/local/tomcat
# Thu, 20 Jan 2022 00:53:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 20 Jan 2022 00:53:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 20 Jan 2022 00:53:31 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 20 Jan 2022 00:53:31 GMT
ENV TOMCAT_MAJOR=10
# Thu, 20 Jan 2022 00:57:53 GMT
ENV TOMCAT_VERSION=10.0.14
# Thu, 20 Jan 2022 00:57:53 GMT
ENV TOMCAT_SHA512=c2d2ad5ed17f7284e3aac5415774a8ef35434f14dbd9a87bc7230d8bfdbe9aa1258b97a59fa5c4030e4c973e4d93d29d20e40b6254347dbb66fae269ff4a61a5
# Thu, 20 Jan 2022 00:58:26 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 20 Jan 2022 00:58:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 20 Jan 2022 00:58:28 GMT
EXPOSE 8080
# Thu, 20 Jan 2022 00:58:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3a461b3ae562f8b6cf015b4c480a21b630a874f7fec851457680159226c81632`  
		Last Modified: Mon, 10 Jan 2022 23:29:44 GMT  
		Size: 62.2 MB (62212074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec355ba40d1bbd4a7011282af24ef6288b134d73edd7c427e6c248c1c91fd61`  
		Last Modified: Wed, 19 Jan 2022 22:14:48 GMT  
		Size: 151.6 MB (151595360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4587691b8bf8ec8bfe5f29db373d12c9cca679b1f28bd6d2674d122f47aff`  
		Last Modified: Thu, 20 Jan 2022 01:28:57 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfe5a311cbe70e97fd943b7c9636cb5553d307567484436f33e5c8e19f31af7`  
		Last Modified: Thu, 20 Jan 2022 01:32:22 GMT  
		Size: 16.7 MB (16741824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f490ac91eda7e673f84e21dc36d3ea6c82a35ce0577db069754fa9a18d001e17`  
		Last Modified: Thu, 20 Jan 2022 01:32:20 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:be19d57badf2f455a73380d91e23d4d3c12a4cfdaf889d5d5fd5fa1f9dd0db28
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230684680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c83d8acf4666d3464b3004838f471867410c1e40c6ab35bded49ca4cd95d72`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 12 Jan 2022 02:39:41 GMT
ADD file:afc90ca87d61fdaef5c9d192a5151ab745ac8b8ea4d7544c2dfdd66bdb3b7993 in / 
# Wed, 12 Jan 2022 02:39:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Jan 2022 22:30:23 GMT
ARG version=17.0.2.8-1
# Wed, 19 Jan 2022 22:30:43 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 19 Jan 2022 22:30:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:30:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 19 Jan 2022 23:33:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jan 2022 23:33:26 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jan 2022 23:33:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 19 Jan 2022 23:33:28 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jan 2022 23:33:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jan 2022 23:33:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jan 2022 23:33:31 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 19 Jan 2022 23:33:32 GMT
ENV TOMCAT_MAJOR=10
# Wed, 19 Jan 2022 23:38:24 GMT
ENV TOMCAT_VERSION=10.0.14
# Wed, 19 Jan 2022 23:38:25 GMT
ENV TOMCAT_SHA512=c2d2ad5ed17f7284e3aac5415774a8ef35434f14dbd9a87bc7230d8bfdbe9aa1258b97a59fa5c4030e4c973e4d93d29d20e40b6254347dbb66fae269ff4a61a5
# Wed, 19 Jan 2022 23:38:43 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 19 Jan 2022 23:38:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 19 Jan 2022 23:38:45 GMT
EXPOSE 8080
# Wed, 19 Jan 2022 23:38:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b2e274b2b0f90c3d6329566163244a0f2e6d97e4c010c62133388ac89652105f`  
		Last Modified: Wed, 12 Jan 2022 02:41:56 GMT  
		Size: 63.8 MB (63836908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e469f8ce35ae3203f14a806e3dbb74ac249cb0233c4fceab246f3123ffef25`  
		Last Modified: Wed, 19 Jan 2022 22:32:46 GMT  
		Size: 150.2 MB (150170380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1b31b0ea6db7aced84e459f37fdd5379ef755149331b44e5bc390a0816787`  
		Last Modified: Thu, 20 Jan 2022 00:15:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6d16ba011bb81fb7b8b68ad273b7d953ef090a57ccff5e12763555aa42e693`  
		Last Modified: Thu, 20 Jan 2022 00:18:41 GMT  
		Size: 16.7 MB (16677253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
