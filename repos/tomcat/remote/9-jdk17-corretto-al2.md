## `tomcat:9-jdk17-corretto-al2`

```console
$ docker pull tomcat@sha256:c6d5415984c6a819ee860a5fadd079201376c536fbd1a7b0a8fa1c042e7f4e0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk17-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:fe710b41d21033dbed3074e6ce25c78e5815274f30a5d899276310976c79ad84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234862547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fce2a599156db4f94e8dd9fed7a9cecbd03e5010909acf8319cd80e9e761ff`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54610b144fbb3d5efb39086466a12b891cc9606edc918f38a19d514baa0cd423`  
		Last Modified: Mon, 25 Aug 2025 20:55:08 GMT  
		Size: 151.9 MB (151886313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb72371a2b1a4f3af9d56cc2d7d017cfd243685f2b112b2af7e41f2a2257450a`  
		Last Modified: Fri, 05 Sep 2025 21:44:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc21fd1d349d297e80debd8511a2f6843dcc64814e2011780b4345cd52cb59f`  
		Last Modified: Fri, 05 Sep 2025 21:44:47 GMT  
		Size: 20.0 MB (19997906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:4e995af8075e1f670d63fa9132184c628275b8913d0da5921f9cd2d51b40863b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa58a9468f76356540ba0ec2ad79b6db65e28b7ebff244137245da054f9d748`

```dockerfile
```

-	Layers:
	-	`sha256:6af3b83f7f0e3bb028df88f5409a55fd668b79ae9e3721284ccf56e3a5f02bd0`  
		Last Modified: Fri, 05 Sep 2025 23:34:25 GMT  
		Size: 5.6 MB (5599277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5858125e3e5679e75e99752d7ba0f28df45a65ad1449ff42d868d1fe4b133852`  
		Last Modified: Fri, 05 Sep 2025 23:34:26 GMT  
		Size: 29.2 KB (29246 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk17-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9a1ca06b6314ce480b2e48d0d6f96d45c3fd5a016cf97d50c8df1fedc62022a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235282369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e026513cb22ecaa57d23ab17e7a49379ec3fe7598230bbf6f8a6f6898d5e739`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a3bec375112fa06818025bf7b6ee4b903edf4e301e27d2464f104b8aabf964f3`  
		Last Modified: Fri, 22 Aug 2025 17:35:51 GMT  
		Size: 64.8 MB (64801350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a245a5fdaaeee3d9f0178309826d43dc906a8f20e3d3c56081666f32a62e445`  
		Last Modified: Mon, 25 Aug 2025 23:39:07 GMT  
		Size: 150.4 MB (150402390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eedba436fcead515fbd2cf751a2356388217be542cbcbe522126ce5339a3dc`  
		Last Modified: Fri, 05 Sep 2025 21:53:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493ee2f95193f64d0faa57e215fca9312c3d9778212c2b389a7aad1a5a993eca`  
		Last Modified: Fri, 05 Sep 2025 21:53:51 GMT  
		Size: 20.1 MB (20078426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:d68d1e3dc42cb9372fa81708e0f001669bcf41183760aaa61324aa5ec80cf90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5627346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1664d644dfed8df6c9b1ddd73d47324351a67249796351cd1f3fe953615afc`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3739467412f988ea75b81231f94676d4e07975b0af60fb189edcecfd79fd9`  
		Last Modified: Fri, 05 Sep 2025 23:34:30 GMT  
		Size: 5.6 MB (5597942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad37ab00db43d05f1acabc9fee4b28b1ae76ac468d041675d1f6e95b73a0a10`  
		Last Modified: Fri, 05 Sep 2025 23:34:31 GMT  
		Size: 29.4 KB (29404 bytes)  
		MIME: application/vnd.in-toto+json
