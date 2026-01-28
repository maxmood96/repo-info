## `tomcat:9-jdk17-corretto-al2`

```console
$ docker pull tomcat@sha256:97cfc075dcd802fd5587b7967e7f095c0807e28d0f163f20baa47046be9f7bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk17-corretto-al2` - linux; amd64

```console
$ docker pull tomcat@sha256:e04e980b0d7b83561141bedce7ad806d405a6be938647c66a8396875eb80950c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233808308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a81a37692a9922f163f46bb60dfd8eb046ad704dfcc1e687c88b59f6bb105aa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:01 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:13:01 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:13:01 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Jan 2026 23:14:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 27 Jan 2026 23:14:11 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:14:11 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 27 Jan 2026 23:14:11 GMT
WORKDIR /usr/local/tomcat
# Tue, 27 Jan 2026 23:14:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 27 Jan 2026 23:14:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 27 Jan 2026 23:14:11 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Jan 2026 23:14:11 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 27 Jan 2026 23:14:11 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 27 Jan 2026 23:14:33 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 27 Jan 2026 23:14:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 27 Jan 2026 23:14:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:14:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7714698ec291fac5fff300229442feb97cb1eeeb2bb977f35f7e11cef7892537`  
		Last Modified: Tue, 27 Jan 2026 22:13:21 GMT  
		Size: 152.5 MB (152466864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42f247d3059b6758fc36c18b559399502a7a62a5d97de05ba059843ddc1f46`  
		Last Modified: Tue, 27 Jan 2026 23:14:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c9dbff05010035efd71b5b4e2705e2f5b9d68ef743740ca3d9c144bf1536c`  
		Last Modified: Tue, 27 Jan 2026 23:14:46 GMT  
		Size: 18.4 MB (18377533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:3ccf35c6f95dd2b2e156da001925e245888411e08809a0fa5d1828021eca1a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5631711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2119cf4cce709ef3062f73111eac18694e2a1d08ccbb8bd74aaa826a71a1c09`

```dockerfile
```

-	Layers:
	-	`sha256:b3da894fba27e2f95308606d1fa95a2eda6ae20663f02397f3b225b7b0359695`  
		Last Modified: Tue, 27 Jan 2026 23:14:46 GMT  
		Size: 5.6 MB (5602508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9886d761479451a5a652675cdd91051d00bd2a2e2b88aea565a799c54c49a948`  
		Last Modified: Tue, 27 Jan 2026 23:14:45 GMT  
		Size: 29.2 KB (29203 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk17-corretto-al2` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:fe0e1df748061688d2114bb4c43e0c0ec273fabcace9f586820f2a433d97d4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234096113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38245e8e34674c6f8851f241617bebeaf012c1f231850af8f120e6546facbb38`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:13 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:12:13 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:12:13 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Jan 2026 23:14:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 27 Jan 2026 23:14:10 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:14:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 27 Jan 2026 23:14:10 GMT
WORKDIR /usr/local/tomcat
# Tue, 27 Jan 2026 23:14:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 27 Jan 2026 23:14:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 27 Jan 2026 23:14:10 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Jan 2026 23:14:10 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 27 Jan 2026 23:14:10 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 27 Jan 2026 23:14:30 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 27 Jan 2026 23:14:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 27 Jan 2026 23:14:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:14:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefcca91c46c186fe23ce434b50d9455a9fcceed3632768e2013f9ac8703212e`  
		Last Modified: Tue, 27 Jan 2026 22:12:33 GMT  
		Size: 151.0 MB (150977605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d724c02d7c92965432a9c5a3c2cc808a39387fc0d824af4fd644184644e830a8`  
		Last Modified: Tue, 27 Jan 2026 23:14:40 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58043abf24f3a8c51221bed769339951334883173b3e8c905d838d0d34d7c0d0`  
		Last Modified: Tue, 27 Jan 2026 23:14:41 GMT  
		Size: 18.3 MB (18319418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto-al2` - unknown; unknown

```console
$ docker pull tomcat@sha256:42c6efa649bfc6fb126e860822ecf5f316c9d5e6905235544fd8f9e812510d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15793ae00571e47cf5d8c356736a116e1adbeb6ff7fef97bab9d774ce83d0f6c`

```dockerfile
```

-	Layers:
	-	`sha256:903ff8b9a23cbd3217f9e87f18a1a8567fb1909eaa65991176ec26cf1bc778ba`  
		Last Modified: Tue, 27 Jan 2026 23:14:41 GMT  
		Size: 5.6 MB (5601173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e109915a959f4efcb4578f84b5329a7916d27b84f1706a654e2a9d9702ff9588`  
		Last Modified: Tue, 27 Jan 2026 23:14:40 GMT  
		Size: 29.4 KB (29358 bytes)  
		MIME: application/vnd.in-toto+json
