## `tomcat:9-jdk8-corretto`

```console
$ docker pull tomcat@sha256:c4b29c2a0ee6fe8c8603f38bfd45588a5f05cf795c536d0ce846303fb954c0f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:5b3692e103f5eaf023fa147d95cc8a3b8e5e8e01a617b144d2b1dc231b6ffaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157451113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc19459eae47036af11b6e453a9602295bb9033628316b5abc839e5fe461c401`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:31:58 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:31:58 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:31:58 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 11 Mar 2026 19:15:36 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Mar 2026 19:15:36 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 19:15:36 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Mar 2026 19:15:36 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Mar 2026 19:15:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Mar 2026 19:15:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Mar 2026 19:15:36 GMT
ENV TOMCAT_MAJOR=9
# Wed, 11 Mar 2026 19:15:36 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 11 Mar 2026 19:15:36 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 11 Mar 2026 19:15:54 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 11 Mar 2026 19:15:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Mar 2026 19:15:54 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Mar 2026 19:15:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4d53067f2cc3fbfbaaff55c5e004564933e732b39179727b563000bbd60805`  
		Last Modified: Wed, 11 Mar 2026 18:32:14 GMT  
		Size: 76.1 MB (76123376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b223173d1a52abe4b527e38db94ef5fa9510857f21a7295510a759c407be5a`  
		Last Modified: Wed, 11 Mar 2026 19:16:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9877d460ca17bf6a9266fe0d4b9048376b565a5c61fd566c3c52ebdafbec625`  
		Last Modified: Wed, 11 Mar 2026 19:16:04 GMT  
		Size: 18.4 MB (18371024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:4f348b0f4f98b678bb9eecf31b1fedb59acaf412853d15886fbae5bbf3977349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af88dc9dfce7898aad052a5ccf01165a50508585fe247a3621f5218dc489dd3`

```dockerfile
```

-	Layers:
	-	`sha256:e954d32a9e80f7e1ba40280075e1244e321cc1593fadcb455cab53c8154faf05`  
		Last Modified: Wed, 11 Mar 2026 19:16:04 GMT  
		Size: 5.4 MB (5443858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67409a5f97b564ae441d6d02e22b5d06b156651203494532f263ca9806265ef`  
		Last Modified: Wed, 11 Mar 2026 19:16:03 GMT  
		Size: 29.2 KB (29192 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9b0d59039b65f4601e5c06b5da21b840c43f0c66b397d05518dcef217aeafe29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143053502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4edbc22b1b7c642ca9712663ebebe9a363a20ee3dd7d1a68cce1199e4c2a94d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:11 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:32:11 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 11 Mar 2026 19:15:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Mar 2026 19:15:46 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 19:15:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Mar 2026 19:15:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Mar 2026 19:15:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Mar 2026 19:15:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Mar 2026 19:15:46 GMT
ENV TOMCAT_MAJOR=9
# Wed, 11 Mar 2026 19:15:46 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 11 Mar 2026 19:15:46 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 11 Mar 2026 19:16:06 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 11 Mar 2026 19:16:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Mar 2026 19:16:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Mar 2026 19:16:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b141cbb1d71a90eb891797bf83c37fa38a55434ccedfc7752216e35e69bfb`  
		Last Modified: Wed, 11 Mar 2026 18:32:28 GMT  
		Size: 59.9 MB (59923077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ee758be0b0873a8bb9b133896d3d37932bc374c41d7ed5da5a37558975cbbd`  
		Last Modified: Wed, 11 Mar 2026 19:16:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb4c359140a2f9533fdf8097379701a5832ee7228a0a59d5879a504427e52a`  
		Last Modified: Wed, 11 Mar 2026 19:16:17 GMT  
		Size: 18.3 MB (18327073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:4e224da64b8dd166aa324c1f26f196182688402dce779d8a13a9687981779d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497d1024b9ca46991568d5e142dd9b909a4ee89d8b63d44cb65aa0b87824ba02`

```dockerfile
```

-	Layers:
	-	`sha256:c5e5b9f8648bf173685fd0e21fb491be26238c0bdfdeaa194b28fd30f7e44a85`  
		Last Modified: Wed, 11 Mar 2026 19:16:16 GMT  
		Size: 5.4 MB (5422321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e7ba586aaa631793b83ef0485b11b9cd25fd14da2246facf9062fd4136d6885`  
		Last Modified: Wed, 11 Mar 2026 19:16:16 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.in-toto+json
