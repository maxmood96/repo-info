## `tomcat:8-jdk11-corretto`

```console
$ docker pull tomcat@sha256:dc81d6f3d2748aea06c87b5208b1483b90a7ca104a63cbad5d374c5fcf8097d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:248bc13a886a42ea590e822135dc51b9ec983052e76b20fd900673ecdf23000a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226125211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c41295c992ab4273108205614494062cb17f9d223731763abb77e82c62fb7da`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:59:12 GMT
COPY dir:a1cfeec8f9b5a4b857222f4bbc7f5fb80ef351168a5f48841d4545523a0a3e1c in / 
# Mon, 07 Aug 2023 19:59:13 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:52:28 GMT
ARG version=11.0.20.8-1
# Mon, 07 Aug 2023 20:52:50 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:52:51 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:52:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 07 Aug 2023 22:18:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 07 Aug 2023 22:18:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 22:18:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 07 Aug 2023 22:18:52 GMT
WORKDIR /usr/local/tomcat
# Mon, 07 Aug 2023 22:18:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 22:18:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 22:21:48 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 07 Aug 2023 22:21:48 GMT
ENV TOMCAT_MAJOR=8
# Wed, 16 Aug 2023 00:04:08 GMT
ENV TOMCAT_VERSION=8.5.92
# Wed, 16 Aug 2023 00:04:08 GMT
ENV TOMCAT_SHA512=faab13a29531a800d38b2602ff76c0041277ffbfb25b938bbefb84ef6ad3ffa26d2c2645cd233eb0d819bcca9887aaeb44df6c044852160d000e5084b1addc2f
# Wed, 16 Aug 2023 00:04:50 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 16 Aug 2023 00:04:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 16 Aug 2023 00:04:52 GMT
EXPOSE 8080
# Wed, 16 Aug 2023 00:04:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c0184eb4a5d5dddba3605f9adcde7e4af58050e9e4ed44751e74957c2ad0f1b4`  
		Last Modified: Tue, 01 Aug 2023 21:03:56 GMT  
		Size: 62.5 MB (62467383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2479941f1565ecbb6cb9f7e72f6162f0f8a143fd3413e39c4f97636588d2a672`  
		Last Modified: Mon, 07 Aug 2023 21:04:23 GMT  
		Size: 147.8 MB (147800657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08f03ace44446ee1a1760f33aeafb540c69d57cc88dc6a993f2f741f8011ce8`  
		Last Modified: Mon, 07 Aug 2023 22:27:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf1bb92db70cf37765ded30e58d09198d9a81ad78fddbe82e45492dc7a1aa18`  
		Last Modified: Wed, 16 Aug 2023 00:23:50 GMT  
		Size: 15.9 MB (15856868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530a8ac2102a657c0bc77e756e9d6e04ab2913a7c4df87a01d1bfe7f097aafd7`  
		Last Modified: Wed, 16 Aug 2023 00:23:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:4ed0fabf8d8f9c12f332025cf45a8895f6a5185b9c104e0c753f2ed5468ea732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224881778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c32e6efb1e8afe6e2f4ec8e94caf06ce247112ae5e25f2fa2c0ffbb7c3b8df`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:40:56 GMT
COPY dir:95dabd7a234aac70a826a1e3c0eafa3928b0be72717af1dea469f66b7db891d5 in / 
# Mon, 07 Aug 2023 19:40:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:23:42 GMT
ARG version=11.0.20.8-1
# Mon, 07 Aug 2023 20:24:00 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:24:01 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:24:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 07 Aug 2023 21:43:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 07 Aug 2023 21:43:52 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 21:43:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 07 Aug 2023 21:43:53 GMT
WORKDIR /usr/local/tomcat
# Mon, 07 Aug 2023 21:43:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 21:43:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 07 Aug 2023 21:46:04 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 07 Aug 2023 21:46:04 GMT
ENV TOMCAT_MAJOR=8
# Wed, 16 Aug 2023 00:43:55 GMT
ENV TOMCAT_VERSION=8.5.92
# Wed, 16 Aug 2023 00:43:55 GMT
ENV TOMCAT_SHA512=faab13a29531a800d38b2602ff76c0041277ffbfb25b938bbefb84ef6ad3ffa26d2c2645cd233eb0d819bcca9887aaeb44df6c044852160d000e5084b1addc2f
# Wed, 16 Aug 2023 00:44:29 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 16 Aug 2023 00:44:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 16 Aug 2023 00:44:30 GMT
EXPOSE 8080
# Wed, 16 Aug 2023 00:44:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c3b5a1e75067e9d540ad8d844cad5a291a8cce89e1a3ed8e0f362a5736d3030c`  
		Last Modified: Wed, 02 Aug 2023 19:26:38 GMT  
		Size: 64.1 MB (64129548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3a0d07b4307c3095a31a5157ca518dac44b2308ce7275f0882fb067b50449`  
		Last Modified: Mon, 07 Aug 2023 20:37:14 GMT  
		Size: 144.9 MB (144929977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36a8010abd7ca86ff95c92279194d02564b8e5ad9751b45ba5eaa98344f293`  
		Last Modified: Mon, 07 Aug 2023 21:50:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74927a4dbf7725af4f750065bcc507723bdac362bce904f4f818f1f6e68da8d`  
		Last Modified: Wed, 16 Aug 2023 01:01:59 GMT  
		Size: 15.8 MB (15821949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b03fe87eb2377263768c0939d279f1846d9bee01e2937925563fafa04e3d941`  
		Last Modified: Wed, 16 Aug 2023 01:01:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
