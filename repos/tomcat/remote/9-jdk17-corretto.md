## `tomcat:9-jdk17-corretto`

```console
$ docker pull tomcat@sha256:c1b379191f5d5544ddd28aae25a014f198be51ffcbf16900f98387b42f1015c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk17-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:58233b0f1b6676a3ec2dd0a567577803ff22c6e0144b30fe2e5aca665dbad7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232727980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7693b339aa01c3edb5e129414b9589ec936418806958d8ad8c616500e2ccd51`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 08:03:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ARG version=17.0.12.7-1
# Mon, 08 Jul 2024 08:03:40 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 08 Jul 2024 08:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_VERSION=9.0.91
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e71b596f90da2b1c3adf4fa69754acd74bd35369b6791c2f12a68d3b1f9925`  
		Last Modified: Tue, 23 Jul 2024 00:07:47 GMT  
		Size: 152.2 MB (152214452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e4a63e88fb098a0ddd3d06da2f0cabd47e7651724d8aabe786b5a6d9af04f9`  
		Last Modified: Tue, 23 Jul 2024 00:59:40 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c421013195137ed48bca22d967cded3a5702ff176847d237b16fc43fcd08ec`  
		Last Modified: Tue, 23 Jul 2024 00:59:41 GMT  
		Size: 17.9 MB (17863920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:a0b3daef87ca649e93a5fed77076ee656dd813a82f310bb61b9da572021e4407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ded7ccb6d0e199f637b382cb54bc874e1383140610b5b453264d9288934f26`

```dockerfile
```

-	Layers:
	-	`sha256:69831050ca674f6eb6d1576fe332c67f92a57555e2d89d97c6b97db7952f6c1b`  
		Last Modified: Tue, 23 Jul 2024 00:59:40 GMT  
		Size: 5.6 MB (5588348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a06cd09216b485da807833acafdf0941e42550065f3910f4505e33584dada5d7`  
		Last Modified: Tue, 23 Jul 2024 00:59:40 GMT  
		Size: 28.1 KB (28125 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b1e10dfff3c88274b5e6c073583478e254d025da133888840d5f2e071b068707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232426670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63446e1a77a7cef19ba73cc4828c63537f214996c0d7e51f124ccc2ef56780c2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 08:03:40 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ARG version=17.0.12.7-1
# Mon, 08 Jul 2024 08:03:40 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 08 Jul 2024 08:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_VERSION=9.0.91
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7670e0f13dba13cacf8a72508b2840f1c1d5b318edb811accb584aab4d61a118`  
		Last Modified: Thu, 18 Jul 2024 22:55:17 GMT  
		Size: 150.9 MB (150866532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022a8272e8b7ba2e8dceafd82df5223b7a623b827db8eff0e12299f304ef456d`  
		Last Modified: Thu, 18 Jul 2024 23:58:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc26aaf9ba40a61fccc5c8ac56ef6f529a0e29f12dad6ec12665f860cf8b7c3f`  
		Last Modified: Thu, 18 Jul 2024 23:58:55 GMT  
		Size: 17.0 MB (16984625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:206c8b17d0647f63fc329298f12831bb62f6b39336e2f06aad9320e6dbafa511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5615575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575b1f875b94bfc38f8965e7b8b8fc7de1fb92eaa2a7bb87944230689d0cb5d9`

```dockerfile
```

-	Layers:
	-	`sha256:77fbc4ab947bec39a678d86fb383cc24c85b10b98e2a151355a9c2e29c78bad9`  
		Last Modified: Thu, 18 Jul 2024 23:58:54 GMT  
		Size: 5.6 MB (5587011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546685b59432f8a203e046ecd28df7612e7924b57493b0cc75f62ca50f6dea88`  
		Last Modified: Thu, 18 Jul 2024 23:58:54 GMT  
		Size: 28.6 KB (28564 bytes)  
		MIME: application/vnd.in-toto+json
