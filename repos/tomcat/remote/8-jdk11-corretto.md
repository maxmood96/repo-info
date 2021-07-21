## `tomcat:8-jdk11-corretto`

```console
$ docker pull tomcat@sha256:11b6a3f06eae850c11b53f8cb9cf6899b545ea8a684ac8e8ebe97c4ec91a76f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:c7e6bf785d266e0e0bb6626ca8b943516816602926fd51cf88de35e6d45d4ae3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224715265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97692267830bda2890c6ec93c97d6b3f36b0e79563c2668ecd56b1a27bef333`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jul 2021 00:20:24 GMT
ARG version=11.0.12.7-1
# Wed, 21 Jul 2021 00:20:47 GMT
# ARGS: version=11.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 21 Jul 2021 00:20:47 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jul 2021 00:20:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jul 2021 00:42:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Jul 2021 00:42:18 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Jul 2021 00:42:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Jul 2021 00:42:20 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Jul 2021 00:42:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jul 2021 00:42:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jul 2021 00:52:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 21 Jul 2021 00:52:33 GMT
ENV TOMCAT_MAJOR=8
# Wed, 21 Jul 2021 00:52:34 GMT
ENV TOMCAT_VERSION=8.5.69
# Wed, 21 Jul 2021 00:52:34 GMT
ENV TOMCAT_SHA512=3ce092c7b89a12904681f23c9c8a2517c13305b4beb783f7b1e85e947aaba4d2bfe8f954f9cefbe009f678557eeb552995f214d9e98c3f1be395822eb2582a1c
# Wed, 21 Jul 2021 00:53:29 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 21 Jul 2021 00:53:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Jul 2021 00:53:32 GMT
EXPOSE 8080
# Wed, 21 Jul 2021 00:53:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac426d7253aaa8ec4b49b208798a7d7c8cda86ffb0cc7d02bc61a1fabfb0518`  
		Last Modified: Wed, 21 Jul 2021 00:22:44 GMT  
		Size: 146.8 MB (146787358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0b6411bed82975a8fb043e1f23addc5b3683c456f78272eb2d085982c90245`  
		Last Modified: Wed, 21 Jul 2021 00:59:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09331d61a39ee52517391d506bd7b3027d7a0092dea01dbd8fdaeb8ce9f0865`  
		Last Modified: Wed, 21 Jul 2021 01:03:03 GMT  
		Size: 16.0 MB (15961599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d8510458610736938ac2082624311fe81fd908dce8ac890a3dc75ca3ec516a`  
		Last Modified: Wed, 21 Jul 2021 01:03:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e91711d19a581f2fa5155b2a1902b1a7e64c12d9c2c698856b9d3dcab4aeff94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223418986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aad62c0b76fd8fa7c3781259301a77d2e46b5233f534982b9e3cfa25ea7b76c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Wed, 21 Jul 2021 00:39:45 GMT
ARG version=11.0.12.7-1
# Wed, 21 Jul 2021 00:40:04 GMT
# ARGS: version=11.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 21 Jul 2021 00:40:04 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jul 2021 00:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jul 2021 01:34:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Jul 2021 01:34:24 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Jul 2021 01:34:24 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Jul 2021 01:34:25 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Jul 2021 01:34:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jul 2021 01:34:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jul 2021 01:42:50 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 21 Jul 2021 01:42:51 GMT
ENV TOMCAT_MAJOR=8
# Wed, 21 Jul 2021 01:42:51 GMT
ENV TOMCAT_VERSION=8.5.69
# Wed, 21 Jul 2021 01:42:51 GMT
ENV TOMCAT_SHA512=3ce092c7b89a12904681f23c9c8a2517c13305b4beb783f7b1e85e947aaba4d2bfe8f954f9cefbe009f678557eeb552995f214d9e98c3f1be395822eb2582a1c
# Wed, 21 Jul 2021 01:43:35 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 21 Jul 2021 01:43:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Jul 2021 01:43:37 GMT
EXPOSE 8080
# Wed, 21 Jul 2021 01:43:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea41d3967e6fc72ca7a70b8846afd61f0043fcb846c06d06eedc019d004bf92e`  
		Last Modified: Wed, 21 Jul 2021 00:41:40 GMT  
		Size: 143.9 MB (143933851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0bc191fe1c655625647b5f03d868b15bcb85c03f6b757b91a09fb666f0f40f`  
		Last Modified: Wed, 21 Jul 2021 01:53:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0780da40a72434d2c77eccd861d28b0c1e95ee70ae72b4e885a23ed094d91edd`  
		Last Modified: Wed, 21 Jul 2021 01:58:18 GMT  
		Size: 15.9 MB (15916943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30feac6c1b7c036c7bfa4618b6e8b1183b0456ed1f38e94083f462c955bb324`  
		Last Modified: Wed, 21 Jul 2021 01:58:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
