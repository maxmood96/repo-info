<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `convertigo`

-	[`convertigo:8.3`](#convertigo83)
-	[`convertigo:8.3.0`](#convertigo830)
-	[`convertigo:latest`](#convertigolatest)

## `convertigo:8.3`

```console
$ docker pull convertigo@sha256:109d6a7e6540b2809af635c61f1f57471f290a9fd914b7513a598cd808a10e4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.3` - linux; amd64

```console
$ docker pull convertigo@sha256:f76cc41e9ad3dcc9efab34463b340567cd3319a3a6ad02315538af716c4852b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341899677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a7a0a827e33e77329eb85cae7120c97cfc50f1adb28fc97000a171421b9efc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Thu, 06 Jun 2024 08:12:00 GMT
ARG RELEASE
# Thu, 06 Jun 2024 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 08:12:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["jshell"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT []
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Jun 2024 08:12:00 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 06 Jun 2024 08:12:00 GMT
ENV SWT_GTK3=0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_VERSION=8.3.0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.0/convertigo-8.3.0.war
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 06 Jun 2024 08:12:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /workspace
# Thu, 06 Jun 2024 08:12:00 GMT
VOLUME [/workspace]
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106426c6b212b985064f4c4174553551ea455b2102a5d2442c1b22ff3be9e94c`  
		Last Modified: Tue, 17 Sep 2024 01:58:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9dfc0ee548f95a6225e232a8e702bde192edd49cf3e65dbc9bb074e7d2f17c`  
		Last Modified: Tue, 17 Sep 2024 01:58:39 GMT  
		Size: 13.0 MB (13028345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a3525c832c3e05792424327ce5030bf6e6704d494f569b042fd7c38838e03c`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 5.7 MB (5653002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05677f125ef7c1f6db038eecbc8463b1b42e4e45df7c987bd075009ca925e107`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 4.5 KB (4471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffde8951b7a5b114842ba097233d7e473f03a8560055320976243c3706d01a`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 27.9 KB (27935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc537376329e23cf240f358553ce3efdb064724d2426cfb88b6c307a543415b4`  
		Last Modified: Tue, 17 Sep 2024 03:03:03 GMT  
		Size: 116.7 MB (116738518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475c29447fa5937a2d16c30ba5ee15afdf9555b6a7b0d4882395893c595977d8`  
		Last Modified: Tue, 17 Sep 2024 03:03:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385b08b2297efc13f0c2a4ceec7eaedb0036afc7c917c4726edee11f5141b738`  
		Last Modified: Tue, 17 Sep 2024 03:03:02 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:64559fc98ca7f5b755e8750be8f8c5b5edd93261ea81fee44bda2db8482a6dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fc110827d21b9a20373d7742565ef947cb2d73117e7c09ca2881ab0f4e9417`

```dockerfile
```

-	Layers:
	-	`sha256:e18e4953ac888638e19f2be65904028f7c27cc74f252ebbbfeb1690f95f36f8c`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 3.9 MB (3946323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8665a7e2f4497ce67c4f1cd8994b90a7b8b6cb2e98231a4563a9db5d1481979`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 45.8 KB (45775 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.3` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:69e9cf6218da9a87292cb2c348aaf3a6b6da4baa1ccafdd1b4a70d296814e1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339253057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff201c72bd03b5254659634f915c85bbc034a11bcbdb0f7832e0d3ef19bf52e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Thu, 06 Jun 2024 08:12:00 GMT
ARG RELEASE
# Thu, 06 Jun 2024 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 08:12:00 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["jshell"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT []
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Jun 2024 08:12:00 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 06 Jun 2024 08:12:00 GMT
ENV SWT_GTK3=0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_VERSION=8.3.0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.0/convertigo-8.3.0.war
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 06 Jun 2024 08:12:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /workspace
# Thu, 06 Jun 2024 08:12:00 GMT
VOLUME [/workspace]
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437c9657963c56848a951c0006cf070f8516093c7aaed4cf7f2804a8066bb11`  
		Last Modified: Tue, 17 Sep 2024 07:29:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2fe03bb527744ee5034fdfe126146d5c50353049f141e999fecbbd9ad80273`  
		Last Modified: Tue, 17 Sep 2024 07:37:10 GMT  
		Size: 13.0 MB (13034675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9330d86212f79fc7a9e095435d3197be0bd896f54575fc9227f23479032c3417`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 5.5 MB (5460413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc7da4b0c55121f80201996194badcb26c37d18488aa4e3b13c7339e026bce2`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce038c14b4c71d1fabca19fd686ac444dde81637489689af40682f4372d4d45f`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 27.9 KB (27942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182d2c1d83c72f467952ddaa88e6bca8102816e640ebffe4a1af49bbfa4ab17`  
		Last Modified: Tue, 17 Sep 2024 10:04:21 GMT  
		Size: 116.7 MB (116738506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453f6f02e93a3a7c6f89027ee13bf0cd8c0d53135901e9d93ee5e34d90fc4e0`  
		Last Modified: Tue, 17 Sep 2024 10:04:18 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263f7c8c8cd6e3d56ada2a04fecc60cc52e95112777b55fbd866c42b477b8e1`  
		Last Modified: Tue, 17 Sep 2024 10:04:18 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:e7340c26318ddf3a062f2e5c8389031f8be1f10247e3768f0af42de0e8fd19f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e4711632fba0466bdb386bf0534f96db84394b007b2d293e84bd1dd2d61d90`

```dockerfile
```

-	Layers:
	-	`sha256:2afa42cbb4e4e538888928d3aa9fdbf0db0208b658d6cc1ac761699677f26b73`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 4.0 MB (4042523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2e05e7d147de9dcc001c46cdd7f1bfab3bbe6fc7ae3f66420a60b39997844e`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 46.4 KB (46449 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:8.3.0`

```console
$ docker pull convertigo@sha256:109d6a7e6540b2809af635c61f1f57471f290a9fd914b7513a598cd808a10e4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.3.0` - linux; amd64

```console
$ docker pull convertigo@sha256:f76cc41e9ad3dcc9efab34463b340567cd3319a3a6ad02315538af716c4852b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341899677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a7a0a827e33e77329eb85cae7120c97cfc50f1adb28fc97000a171421b9efc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Thu, 06 Jun 2024 08:12:00 GMT
ARG RELEASE
# Thu, 06 Jun 2024 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 08:12:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["jshell"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT []
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Jun 2024 08:12:00 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 06 Jun 2024 08:12:00 GMT
ENV SWT_GTK3=0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_VERSION=8.3.0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.0/convertigo-8.3.0.war
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 06 Jun 2024 08:12:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /workspace
# Thu, 06 Jun 2024 08:12:00 GMT
VOLUME [/workspace]
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106426c6b212b985064f4c4174553551ea455b2102a5d2442c1b22ff3be9e94c`  
		Last Modified: Tue, 17 Sep 2024 01:58:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9dfc0ee548f95a6225e232a8e702bde192edd49cf3e65dbc9bb074e7d2f17c`  
		Last Modified: Tue, 17 Sep 2024 01:58:39 GMT  
		Size: 13.0 MB (13028345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a3525c832c3e05792424327ce5030bf6e6704d494f569b042fd7c38838e03c`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 5.7 MB (5653002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05677f125ef7c1f6db038eecbc8463b1b42e4e45df7c987bd075009ca925e107`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 4.5 KB (4471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffde8951b7a5b114842ba097233d7e473f03a8560055320976243c3706d01a`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 27.9 KB (27935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc537376329e23cf240f358553ce3efdb064724d2426cfb88b6c307a543415b4`  
		Last Modified: Tue, 17 Sep 2024 03:03:03 GMT  
		Size: 116.7 MB (116738518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475c29447fa5937a2d16c30ba5ee15afdf9555b6a7b0d4882395893c595977d8`  
		Last Modified: Tue, 17 Sep 2024 03:03:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385b08b2297efc13f0c2a4ceec7eaedb0036afc7c917c4726edee11f5141b738`  
		Last Modified: Tue, 17 Sep 2024 03:03:02 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3.0` - unknown; unknown

```console
$ docker pull convertigo@sha256:64559fc98ca7f5b755e8750be8f8c5b5edd93261ea81fee44bda2db8482a6dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fc110827d21b9a20373d7742565ef947cb2d73117e7c09ca2881ab0f4e9417`

```dockerfile
```

-	Layers:
	-	`sha256:e18e4953ac888638e19f2be65904028f7c27cc74f252ebbbfeb1690f95f36f8c`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 3.9 MB (3946323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8665a7e2f4497ce67c4f1cd8994b90a7b8b6cb2e98231a4563a9db5d1481979`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 45.8 KB (45775 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.3.0` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:69e9cf6218da9a87292cb2c348aaf3a6b6da4baa1ccafdd1b4a70d296814e1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339253057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff201c72bd03b5254659634f915c85bbc034a11bcbdb0f7832e0d3ef19bf52e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Thu, 06 Jun 2024 08:12:00 GMT
ARG RELEASE
# Thu, 06 Jun 2024 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 08:12:00 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["jshell"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT []
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Jun 2024 08:12:00 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 06 Jun 2024 08:12:00 GMT
ENV SWT_GTK3=0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_VERSION=8.3.0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.0/convertigo-8.3.0.war
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 06 Jun 2024 08:12:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /workspace
# Thu, 06 Jun 2024 08:12:00 GMT
VOLUME [/workspace]
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437c9657963c56848a951c0006cf070f8516093c7aaed4cf7f2804a8066bb11`  
		Last Modified: Tue, 17 Sep 2024 07:29:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2fe03bb527744ee5034fdfe126146d5c50353049f141e999fecbbd9ad80273`  
		Last Modified: Tue, 17 Sep 2024 07:37:10 GMT  
		Size: 13.0 MB (13034675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9330d86212f79fc7a9e095435d3197be0bd896f54575fc9227f23479032c3417`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 5.5 MB (5460413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc7da4b0c55121f80201996194badcb26c37d18488aa4e3b13c7339e026bce2`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce038c14b4c71d1fabca19fd686ac444dde81637489689af40682f4372d4d45f`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 27.9 KB (27942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182d2c1d83c72f467952ddaa88e6bca8102816e640ebffe4a1af49bbfa4ab17`  
		Last Modified: Tue, 17 Sep 2024 10:04:21 GMT  
		Size: 116.7 MB (116738506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453f6f02e93a3a7c6f89027ee13bf0cd8c0d53135901e9d93ee5e34d90fc4e0`  
		Last Modified: Tue, 17 Sep 2024 10:04:18 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263f7c8c8cd6e3d56ada2a04fecc60cc52e95112777b55fbd866c42b477b8e1`  
		Last Modified: Tue, 17 Sep 2024 10:04:18 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3.0` - unknown; unknown

```console
$ docker pull convertigo@sha256:e7340c26318ddf3a062f2e5c8389031f8be1f10247e3768f0af42de0e8fd19f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e4711632fba0466bdb386bf0534f96db84394b007b2d293e84bd1dd2d61d90`

```dockerfile
```

-	Layers:
	-	`sha256:2afa42cbb4e4e538888928d3aa9fdbf0db0208b658d6cc1ac761699677f26b73`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 4.0 MB (4042523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2e05e7d147de9dcc001c46cdd7f1bfab3bbe6fc7ae3f66420a60b39997844e`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 46.4 KB (46449 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:latest`

```console
$ docker pull convertigo@sha256:109d6a7e6540b2809af635c61f1f57471f290a9fd914b7513a598cd808a10e4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:f76cc41e9ad3dcc9efab34463b340567cd3319a3a6ad02315538af716c4852b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341899677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a7a0a827e33e77329eb85cae7120c97cfc50f1adb28fc97000a171421b9efc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Thu, 06 Jun 2024 08:12:00 GMT
ARG RELEASE
# Thu, 06 Jun 2024 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 08:12:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["jshell"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT []
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Jun 2024 08:12:00 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 06 Jun 2024 08:12:00 GMT
ENV SWT_GTK3=0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_VERSION=8.3.0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.0/convertigo-8.3.0.war
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 06 Jun 2024 08:12:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /workspace
# Thu, 06 Jun 2024 08:12:00 GMT
VOLUME [/workspace]
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106426c6b212b985064f4c4174553551ea455b2102a5d2442c1b22ff3be9e94c`  
		Last Modified: Tue, 17 Sep 2024 01:58:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9dfc0ee548f95a6225e232a8e702bde192edd49cf3e65dbc9bb074e7d2f17c`  
		Last Modified: Tue, 17 Sep 2024 01:58:39 GMT  
		Size: 13.0 MB (13028345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a3525c832c3e05792424327ce5030bf6e6704d494f569b042fd7c38838e03c`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 5.7 MB (5653002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05677f125ef7c1f6db038eecbc8463b1b42e4e45df7c987bd075009ca925e107`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 4.5 KB (4471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffde8951b7a5b114842ba097233d7e473f03a8560055320976243c3706d01a`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 27.9 KB (27935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc537376329e23cf240f358553ce3efdb064724d2426cfb88b6c307a543415b4`  
		Last Modified: Tue, 17 Sep 2024 03:03:03 GMT  
		Size: 116.7 MB (116738518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475c29447fa5937a2d16c30ba5ee15afdf9555b6a7b0d4882395893c595977d8`  
		Last Modified: Tue, 17 Sep 2024 03:03:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385b08b2297efc13f0c2a4ceec7eaedb0036afc7c917c4726edee11f5141b738`  
		Last Modified: Tue, 17 Sep 2024 03:03:02 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:64559fc98ca7f5b755e8750be8f8c5b5edd93261ea81fee44bda2db8482a6dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fc110827d21b9a20373d7742565ef947cb2d73117e7c09ca2881ab0f4e9417`

```dockerfile
```

-	Layers:
	-	`sha256:e18e4953ac888638e19f2be65904028f7c27cc74f252ebbbfeb1690f95f36f8c`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 3.9 MB (3946323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8665a7e2f4497ce67c4f1cd8994b90a7b8b6cb2e98231a4563a9db5d1481979`  
		Last Modified: Tue, 17 Sep 2024 03:03:01 GMT  
		Size: 45.8 KB (45775 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:latest` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:69e9cf6218da9a87292cb2c348aaf3a6b6da4baa1ccafdd1b4a70d296814e1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339253057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff201c72bd03b5254659634f915c85bbc034a11bcbdb0f7832e0d3ef19bf52e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Thu, 06 Jun 2024 08:12:00 GMT
ARG RELEASE
# Thu, 06 Jun 2024 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 08:12:00 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["jshell"]
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Jun 2024 08:12:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT []
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Jun 2024 08:12:00 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 06 Jun 2024 08:12:00 GMT
ENV SWT_GTK3=0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Jun 2024 08:12:00 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_VERSION=8.3.0
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.0/convertigo-8.3.0.war
# Thu, 06 Jun 2024 08:12:00 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 06 Jun 2024 08:12:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
WORKDIR /workspace
# Thu, 06 Jun 2024 08:12:00 GMT
VOLUME [/workspace]
# Thu, 06 Jun 2024 08:12:00 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 06 Jun 2024 08:12:00 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437c9657963c56848a951c0006cf070f8516093c7aaed4cf7f2804a8066bb11`  
		Last Modified: Tue, 17 Sep 2024 07:29:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2fe03bb527744ee5034fdfe126146d5c50353049f141e999fecbbd9ad80273`  
		Last Modified: Tue, 17 Sep 2024 07:37:10 GMT  
		Size: 13.0 MB (13034675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9330d86212f79fc7a9e095435d3197be0bd896f54575fc9227f23479032c3417`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 5.5 MB (5460413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc7da4b0c55121f80201996194badcb26c37d18488aa4e3b13c7339e026bce2`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce038c14b4c71d1fabca19fd686ac444dde81637489689af40682f4372d4d45f`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 27.9 KB (27942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182d2c1d83c72f467952ddaa88e6bca8102816e640ebffe4a1af49bbfa4ab17`  
		Last Modified: Tue, 17 Sep 2024 10:04:21 GMT  
		Size: 116.7 MB (116738506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453f6f02e93a3a7c6f89027ee13bf0cd8c0d53135901e9d93ee5e34d90fc4e0`  
		Last Modified: Tue, 17 Sep 2024 10:04:18 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263f7c8c8cd6e3d56ada2a04fecc60cc52e95112777b55fbd866c42b477b8e1`  
		Last Modified: Tue, 17 Sep 2024 10:04:18 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:e7340c26318ddf3a062f2e5c8389031f8be1f10247e3768f0af42de0e8fd19f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e4711632fba0466bdb386bf0534f96db84394b007b2d293e84bd1dd2d61d90`

```dockerfile
```

-	Layers:
	-	`sha256:2afa42cbb4e4e538888928d3aa9fdbf0db0208b658d6cc1ac761699677f26b73`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 4.0 MB (4042523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2e05e7d147de9dcc001c46cdd7f1bfab3bbe6fc7ae3f66420a60b39997844e`  
		Last Modified: Tue, 17 Sep 2024 10:04:17 GMT  
		Size: 46.4 KB (46449 bytes)  
		MIME: application/vnd.in-toto+json
