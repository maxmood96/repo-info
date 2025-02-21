## `tomcat:9-jdk21-corretto`

```console
$ docker pull tomcat@sha256:6cf12c2ab4d7032cf2fa0371977ecfd0054da95651986fb82f9a0000edb7347e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:9-jdk21-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:50acf4856a9ace8a4da8a17297ee6f9b01888fdefc7f001cbc6e0eb09bea2647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245387312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2946399330b8354d207b19487acab9fa0a62f17daf862ebc44df8c3569f8cc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 12:06:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 12:06:03 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:06:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 12:06:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 12:06:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_VERSION=9.0.100
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_SHA512=e0b1379866d09b54f2743afb382c32a33bca9652c379467c1fa0a5b15a1b98830ae23fb1d8f96c43148844ce95b6c1d22a66db3f8efaf41f225b158c3cb71c92
# Tue, 18 Feb 2025 12:06:03 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 18 Feb 2025 12:06:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 12:06:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 12:06:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:43fdf45428917f1f386fbfe0eba1ccfdadae7696a4cce30a96cca587ab25ab90`  
		Last Modified: Wed, 05 Feb 2025 10:24:14 GMT  
		Size: 62.7 MB (62665244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c721c8165600a737cac934832d0acdb99188f39c5d9a453682c0f8876c859b2e`  
		Last Modified: Mon, 10 Feb 2025 20:08:45 GMT  
		Size: 164.7 MB (164730035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0bbddb3ae889dffb3a04ba3105f563b7c36fd93219f6494ebbc45170e6017d`  
		Last Modified: Wed, 19 Feb 2025 00:29:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a5b8866d2aeec4f4934445266b18c46535794ecb4344fe23ed12f9764de9f9`  
		Last Modified: Wed, 19 Feb 2025 00:29:29 GMT  
		Size: 18.0 MB (17991830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:35230eeceac269de6e5b4e2f90ceaafec50f325010cff9353330351a49af4afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f82418d4ecde3e9894bbdbab8dabc8ad21acbd33e1b694505837b244e8a582d`

```dockerfile
```

-	Layers:
	-	`sha256:98e1be49d18d9a86d918a41b43b6d481c468c6fd72bdfd95796d49b2a3388f9b`  
		Last Modified: Wed, 19 Feb 2025 00:29:29 GMT  
		Size: 5.6 MB (5583630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b67b02f8efac4396ba217070004f95bd782f704229e3af4ca1a03e76abb47e9`  
		Last Modified: Wed, 19 Feb 2025 00:29:28 GMT  
		Size: 29.2 KB (29245 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:72e9c50f5112d615d0d5b10f2f5bc35342ee08ec70643dce9a0a459ffb44b665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245507428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7917ec5d05fb9e89823222f6ecd527d2fb04dc1e58ca88aab08d87f94ee4fec`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 12:06:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 12:06:03 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:06:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 12:06:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 12:06:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_VERSION=9.0.100
# Tue, 18 Feb 2025 12:06:03 GMT
ENV TOMCAT_SHA512=e0b1379866d09b54f2743afb382c32a33bca9652c379467c1fa0a5b15a1b98830ae23fb1d8f96c43148844ce95b6c1d22a66db3f8efaf41f225b158c3cb71c92
# Tue, 18 Feb 2025 12:06:03 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y --setopt=skip_missing_names_on_install=False yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y --setopt=skip_missing_names_on_install=False $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt rpm --query --whatprovides 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r yumdb set reason user 	; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 18 Feb 2025 12:06:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 12:06:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 12:06:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8928a0cb9d9723d240d99fc6bc7655b62ddf218a866232a1b3789a41992e6757`  
		Last Modified: Mon, 10 Feb 2025 20:26:15 GMT  
		Size: 162.9 MB (162862315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5565d067afed55afcc5546b48788310c48379f3dbdd2eca51b5d7d09987de`  
		Last Modified: Mon, 10 Feb 2025 21:25:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750ac2c3e92d9ab6972bbedcdcc3760444081ced243b2de0a083281efe2087e8`  
		Last Modified: Wed, 19 Feb 2025 01:15:53 GMT  
		Size: 18.1 MB (18066687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull tomcat@sha256:3ec02c48999e7949f6374e7bdac91314d3fdc3470ea39d53e3e407ab28db2cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce88a87d6318f939058b904041ef26c043320c28ff5f510105c9e0367d3a2a8`

```dockerfile
```

-	Layers:
	-	`sha256:61bc16a2f6a31dfd4488bde193d7cee5494ef44e4fd8ee80d7bdf161b94b5eb3`  
		Last Modified: Wed, 19 Feb 2025 01:15:52 GMT  
		Size: 5.6 MB (5582295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1f8d6d78c4c194f997873c31d51d3bec3c4b8b2d9e7b20a871b71dd221a6731`  
		Last Modified: Wed, 19 Feb 2025 01:15:51 GMT  
		Size: 29.4 KB (29404 bytes)  
		MIME: application/vnd.in-toto+json
