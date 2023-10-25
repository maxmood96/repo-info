## `tomcat:9-jdk21-corretto-al2`

```console
$ docker pull tomcat@sha256:2a88e52a2a87ce5d2c54b7f3690423dde7146ad1d5c79e98e641ba7291fc2e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jdk21-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:b3a3a834eee47cbb68c43ac17d43e981c9ba0d24ec805b6d13fc1eda7e2f0d52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244810565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52798c9f94642515bd9291bed842b19c1fe1877ccdc86b6bdd7b0bca673556a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 25 Oct 2023 01:19:53 GMT
COPY dir:fdcfaddab7ba123e1840e939ec5f9c668c54d167449dc297fea5669f294f7222 in / 
# Wed, 25 Oct 2023 01:19:54 GMT
CMD ["/bin/bash"]
# Wed, 25 Oct 2023 01:48:51 GMT
ARG version=21.0.1.12-1
# Wed, 25 Oct 2023 01:49:16 GMT
# ARGS: version=21.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 25 Oct 2023 01:49:17 GMT
ENV LANG=C.UTF-8
# Wed, 25 Oct 2023 01:49:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 25 Oct 2023 03:00:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Oct 2023 03:00:20 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Oct 2023 03:00:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Oct 2023 03:00:20 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Oct 2023 03:00:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Oct 2023 03:00:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Oct 2023 03:00:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 25 Oct 2023 03:00:20 GMT
ENV TOMCAT_MAJOR=9
# Wed, 25 Oct 2023 03:00:21 GMT
ENV TOMCAT_VERSION=9.0.82
# Wed, 25 Oct 2023 03:00:21 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Wed, 25 Oct 2023 03:00:57 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 25 Oct 2023 03:00:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Oct 2023 03:00:59 GMT
EXPOSE 8080
# Wed, 25 Oct 2023 03:00:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e6a2a106da1df9b5d4bfa74686415ac760f9d9999604e3784820d596e0983e27`  
		Last Modified: Wed, 25 Oct 2023 01:11:13 GMT  
		Size: 62.5 MB (62492148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97273e99f2366ab32f923403643970dd37c76841482954a7acc6d25712ee816`  
		Last Modified: Wed, 25 Oct 2023 01:59:42 GMT  
		Size: 165.5 MB (165461211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4104fbb0e332fec1f2cf8da06cd9055fb00ecfaaf4df52f799c03cdd250b11`  
		Last Modified: Wed, 25 Oct 2023 03:10:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d83e3b2ce07bb8b1fce2a68876a24d785ded17175d9d0e490dbceb1941f64f`  
		Last Modified: Wed, 25 Oct 2023 03:10:55 GMT  
		Size: 16.9 MB (16856903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02cb2e9161ed13aa37f198d4089ea15b930fd59ad17eac59f8e7b7d998c4de6`  
		Last Modified: Wed, 25 Oct 2023 03:10:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk21-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9d2b4538651d811e622cb512100f9525925b4fdc5466fb22daee7053a4f687aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244523775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059e2b2882c4706789734b1c668ce8972a76fa4cc86366f1696239a75f9320b9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 25 Oct 2023 00:39:44 GMT
COPY dir:8cce6e6a6abbbd299b12dd9d8f9974415975c25f4170a182c4d6addd8ba9d101 in / 
# Wed, 25 Oct 2023 00:39:45 GMT
CMD ["/bin/bash"]
# Wed, 25 Oct 2023 01:24:48 GMT
ARG version=21.0.1.12-1
# Wed, 25 Oct 2023 01:25:06 GMT
# ARGS: version=21.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 25 Oct 2023 01:25:08 GMT
ENV LANG=C.UTF-8
# Wed, 25 Oct 2023 01:25:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 25 Oct 2023 01:57:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Oct 2023 01:57:27 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Oct 2023 01:57:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Oct 2023 01:57:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Oct 2023 01:57:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Oct 2023 01:57:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Oct 2023 01:57:27 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 25 Oct 2023 01:57:27 GMT
ENV TOMCAT_MAJOR=9
# Wed, 25 Oct 2023 01:57:27 GMT
ENV TOMCAT_VERSION=9.0.82
# Wed, 25 Oct 2023 01:57:28 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Wed, 25 Oct 2023 01:57:58 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 25 Oct 2023 01:57:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Oct 2023 01:57:59 GMT
EXPOSE 8080
# Wed, 25 Oct 2023 01:57:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bceed9d4335ecd25da3cee660b39ab03c762b3e6bc197470f6eeeaad4c7f3db4`  
		Last Modified: Wed, 25 Oct 2023 00:40:19 GMT  
		Size: 64.2 MB (64228438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c00fbca101d9eaaf3e5a2219fb7a85bc4d92cceac02eb010191f73d4cb9f852`  
		Last Modified: Wed, 25 Oct 2023 01:33:53 GMT  
		Size: 163.5 MB (163461304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1b9aa838e2c058c0eab86e2de9f6d80507ca77e6e357fcdd057ce8feb4c6eb`  
		Last Modified: Wed, 25 Oct 2023 02:06:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa9fb4724c0b25b7eabe14b3f644be6fef3b8668f2ef666f9053248050b6f2`  
		Last Modified: Wed, 25 Oct 2023 02:06:13 GMT  
		Size: 16.8 MB (16833730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc2b80295ce471065c216fb5a483bbe4efa7db3a4ee0bb8ef864e8a835a4611`  
		Last Modified: Wed, 25 Oct 2023 02:06:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
