<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `convertigo`

-	[`convertigo:8.3`](#convertigo83)
-	[`convertigo:8.3.0`](#convertigo830)
-	[`convertigo:latest`](#convertigolatest)

## `convertigo:8.3`

```console
$ docker pull convertigo@sha256:f53e3698fb5c2fd893fb3b75f52e393a16ad8e2fba674804254993451947c11d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.3` - linux; amd64

```console
$ docker pull convertigo@sha256:c140bccaf23de56e1d940b09d071b7b58556d0fe293a7153729477e20346a4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345133694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c332245a08978d4a8afccf39fd83c7fca59ddb865e211106a80bbea14422ef4`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
ENV TOMCAT_VERSION=9.0.93
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff50609e3ed14c7c3740b327b78aacfe1ea1ee52420196ee57d2b4319ae0936`  
		Last Modified: Tue, 02 Jul 2024 06:01:53 GMT  
		Size: 17.4 MB (17414986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb7392271a97e97ea73ccfd39a06b4c83857ad79f4268a59103857b0fb6cd7f`  
		Last Modified: Tue, 23 Jul 2024 01:10:00 GMT  
		Size: 158.6 MB (158586978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bdd092a67162b7a31654a479d0354e1a6bbc07290915a3afe4841c03e0d8b3`  
		Last Modified: Tue, 23 Jul 2024 01:09:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10084474a2eb75fd61510f583fe2f83d3520beeae318672023e43f531853a81c`  
		Last Modified: Thu, 25 Jul 2024 17:31:19 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befb98abccf530a5f19c42568a2da1a03a6ef2a43480e6a821eb550839222b45`  
		Last Modified: Tue, 06 Aug 2024 23:58:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83a50ff2b4162252d46da200811d3c73c60c38f15cf6fa4675fcd56cbdf293b`  
		Last Modified: Tue, 06 Aug 2024 23:58:35 GMT  
		Size: 16.3 MB (16262272 bytes)  
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
	-	`sha256:e1a9aade01ffce113d7cfda08bf474a730c4680118210ab12ddcbaa80408380c`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 5.7 MB (5653605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0642c82406e088e9b87dc2ccdfa9c739ac138b588f1f8803253baba4f758a6`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 4.5 KB (4466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77fc38010fe2ab96a79be769f8cbbe12e94051efe1f2aae63d92b37edfcbf75`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 28.0 KB (27967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d079d3a3549bbd499c16c9a21f7f5167bf8c9e3fc335bed1be811431253912`  
		Last Modified: Wed, 07 Aug 2024 00:53:09 GMT  
		Size: 116.7 MB (116738519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd71bf851100b4d4e5fa6d6d53b28e3a867f13576477d343bd62c99614882cf`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0e9274cc3b270cc1cc5033d5205d77adfa053f76107b3f203fd0c3fcfcc79`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:75b617780493693ee3d957d7736bece06fbed7aba0d8f845f624cd6c5b72e0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7496aa7772d0ef05407248c5d1243a69bb9b3956df177155c541ea0c6cc5126f`

```dockerfile
```

-	Layers:
	-	`sha256:11171ad98afc6b01ec8809097576a5f78208e51b1e0489df4b32d2fc95008a16`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 3.9 MB (3948207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6cc0704f5a0914b87b343e3e108ead9c1411f501c0c619aba4dafb1b510d6c`  
		Last Modified: Wed, 07 Aug 2024 00:53:05 GMT  
		Size: 45.8 KB (45776 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.3` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:732d477b2fe7e363563b236927d20a40306185762f292948a1694766514a4911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342319662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcb9fc4eb5e451ef19646ed7a7c4e72a9afb26659608eb842d24ae92a8d5fb`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
ENV TOMCAT_VERSION=9.0.93
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672595a5d127b59ecf75423f0ef5367642a9d021fe56a7d618121f1c21d2fd7`  
		Last Modified: Tue, 02 Jul 2024 04:35:30 GMT  
		Size: 18.8 MB (18827827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c225f5a6552449ce207f5bfbd85f6ed1a26a3b52f2a3e7270b29af2ee771cad`  
		Last Modified: Tue, 23 Jul 2024 04:15:08 GMT  
		Size: 156.8 MB (156756723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ec6fdf43db04c2e6133f92c02f91fe54d3123e5a1cabb3d0368f92a4d26831`  
		Last Modified: Tue, 23 Jul 2024 04:14:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af142f8f7ec876d457a54ad62e2b413df48ec349e9dfbbfddbc3c71251042def`  
		Last Modified: Thu, 25 Jul 2024 17:46:59 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe795db3b36027d6ee12de031961432002225529dc34c548be9607c00db2ad7`  
		Last Modified: Thu, 25 Jul 2024 23:53:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b592a45f2d3d804089c2a453c04ade3641e997d27b2d0312c806e3d7dbc66`  
		Last Modified: Wed, 07 Aug 2024 00:12:55 GMT  
		Size: 16.1 MB (16097058 bytes)  
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
	-	`sha256:d9535a6a2a5f4ad24e8a5fbf1bf5e984e456c5a2fca84053a69a979e67902f7a`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 5.5 MB (5460934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457e9fb4d96a28714651e527f7451da4029af137233074445a09357d1d7fd1d`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95114e5fea9832051ace17904eb9e9e3f9f7ef4748a7811d1398aa117998da63`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 28.0 KB (27968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa992f9162c825e211f68ca2b52a528167d86370e7aadc1c12b0311891a4360`  
		Last Modified: Wed, 07 Aug 2024 01:00:05 GMT  
		Size: 116.7 MB (116738516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0aa69208031a051249fa19626df1606e666c820ee333604c1eef006324e42`  
		Last Modified: Wed, 07 Aug 2024 01:00:03 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318d70f731a356b38ce6bcd1e0f5144080a83762c024d5367e0b04dcbbdd6574`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:ba878db6d7276d5e256a60beccc893c919a3e14bde5fa590f9374b77157add1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e58610306ca15c9862d40ac462815f683f93cdb2d270443f431a669d6b93bb`

```dockerfile
```

-	Layers:
	-	`sha256:7eef595b21fa6dbdbd3a95381a2b3351ec321709c1e08220ec57db19c7a6d28a`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 4.0 MB (4044407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b014df6d2255ff1bb505dfd73da54cd7068bef34b49744f7c3752ddb4753f7`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 46.4 KB (46447 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:8.3.0`

```console
$ docker pull convertigo@sha256:f53e3698fb5c2fd893fb3b75f52e393a16ad8e2fba674804254993451947c11d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.3.0` - linux; amd64

```console
$ docker pull convertigo@sha256:c140bccaf23de56e1d940b09d071b7b58556d0fe293a7153729477e20346a4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345133694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c332245a08978d4a8afccf39fd83c7fca59ddb865e211106a80bbea14422ef4`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
ENV TOMCAT_VERSION=9.0.93
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff50609e3ed14c7c3740b327b78aacfe1ea1ee52420196ee57d2b4319ae0936`  
		Last Modified: Tue, 02 Jul 2024 06:01:53 GMT  
		Size: 17.4 MB (17414986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb7392271a97e97ea73ccfd39a06b4c83857ad79f4268a59103857b0fb6cd7f`  
		Last Modified: Tue, 23 Jul 2024 01:10:00 GMT  
		Size: 158.6 MB (158586978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bdd092a67162b7a31654a479d0354e1a6bbc07290915a3afe4841c03e0d8b3`  
		Last Modified: Tue, 23 Jul 2024 01:09:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10084474a2eb75fd61510f583fe2f83d3520beeae318672023e43f531853a81c`  
		Last Modified: Thu, 25 Jul 2024 17:31:19 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befb98abccf530a5f19c42568a2da1a03a6ef2a43480e6a821eb550839222b45`  
		Last Modified: Tue, 06 Aug 2024 23:58:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83a50ff2b4162252d46da200811d3c73c60c38f15cf6fa4675fcd56cbdf293b`  
		Last Modified: Tue, 06 Aug 2024 23:58:35 GMT  
		Size: 16.3 MB (16262272 bytes)  
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
	-	`sha256:e1a9aade01ffce113d7cfda08bf474a730c4680118210ab12ddcbaa80408380c`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 5.7 MB (5653605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0642c82406e088e9b87dc2ccdfa9c739ac138b588f1f8803253baba4f758a6`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 4.5 KB (4466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77fc38010fe2ab96a79be769f8cbbe12e94051efe1f2aae63d92b37edfcbf75`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 28.0 KB (27967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d079d3a3549bbd499c16c9a21f7f5167bf8c9e3fc335bed1be811431253912`  
		Last Modified: Wed, 07 Aug 2024 00:53:09 GMT  
		Size: 116.7 MB (116738519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd71bf851100b4d4e5fa6d6d53b28e3a867f13576477d343bd62c99614882cf`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0e9274cc3b270cc1cc5033d5205d77adfa053f76107b3f203fd0c3fcfcc79`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3.0` - unknown; unknown

```console
$ docker pull convertigo@sha256:75b617780493693ee3d957d7736bece06fbed7aba0d8f845f624cd6c5b72e0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7496aa7772d0ef05407248c5d1243a69bb9b3956df177155c541ea0c6cc5126f`

```dockerfile
```

-	Layers:
	-	`sha256:11171ad98afc6b01ec8809097576a5f78208e51b1e0489df4b32d2fc95008a16`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 3.9 MB (3948207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6cc0704f5a0914b87b343e3e108ead9c1411f501c0c619aba4dafb1b510d6c`  
		Last Modified: Wed, 07 Aug 2024 00:53:05 GMT  
		Size: 45.8 KB (45776 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.3.0` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:732d477b2fe7e363563b236927d20a40306185762f292948a1694766514a4911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342319662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcb9fc4eb5e451ef19646ed7a7c4e72a9afb26659608eb842d24ae92a8d5fb`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
ENV TOMCAT_VERSION=9.0.93
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672595a5d127b59ecf75423f0ef5367642a9d021fe56a7d618121f1c21d2fd7`  
		Last Modified: Tue, 02 Jul 2024 04:35:30 GMT  
		Size: 18.8 MB (18827827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c225f5a6552449ce207f5bfbd85f6ed1a26a3b52f2a3e7270b29af2ee771cad`  
		Last Modified: Tue, 23 Jul 2024 04:15:08 GMT  
		Size: 156.8 MB (156756723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ec6fdf43db04c2e6133f92c02f91fe54d3123e5a1cabb3d0368f92a4d26831`  
		Last Modified: Tue, 23 Jul 2024 04:14:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af142f8f7ec876d457a54ad62e2b413df48ec349e9dfbbfddbc3c71251042def`  
		Last Modified: Thu, 25 Jul 2024 17:46:59 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe795db3b36027d6ee12de031961432002225529dc34c548be9607c00db2ad7`  
		Last Modified: Thu, 25 Jul 2024 23:53:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b592a45f2d3d804089c2a453c04ade3641e997d27b2d0312c806e3d7dbc66`  
		Last Modified: Wed, 07 Aug 2024 00:12:55 GMT  
		Size: 16.1 MB (16097058 bytes)  
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
	-	`sha256:d9535a6a2a5f4ad24e8a5fbf1bf5e984e456c5a2fca84053a69a979e67902f7a`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 5.5 MB (5460934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457e9fb4d96a28714651e527f7451da4029af137233074445a09357d1d7fd1d`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95114e5fea9832051ace17904eb9e9e3f9f7ef4748a7811d1398aa117998da63`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 28.0 KB (27968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa992f9162c825e211f68ca2b52a528167d86370e7aadc1c12b0311891a4360`  
		Last Modified: Wed, 07 Aug 2024 01:00:05 GMT  
		Size: 116.7 MB (116738516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0aa69208031a051249fa19626df1606e666c820ee333604c1eef006324e42`  
		Last Modified: Wed, 07 Aug 2024 01:00:03 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318d70f731a356b38ce6bcd1e0f5144080a83762c024d5367e0b04dcbbdd6574`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3.0` - unknown; unknown

```console
$ docker pull convertigo@sha256:ba878db6d7276d5e256a60beccc893c919a3e14bde5fa590f9374b77157add1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e58610306ca15c9862d40ac462815f683f93cdb2d270443f431a669d6b93bb`

```dockerfile
```

-	Layers:
	-	`sha256:7eef595b21fa6dbdbd3a95381a2b3351ec321709c1e08220ec57db19c7a6d28a`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 4.0 MB (4044407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b014df6d2255ff1bb505dfd73da54cd7068bef34b49744f7c3752ddb4753f7`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 46.4 KB (46447 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:latest`

```console
$ docker pull convertigo@sha256:f53e3698fb5c2fd893fb3b75f52e393a16ad8e2fba674804254993451947c11d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:c140bccaf23de56e1d940b09d071b7b58556d0fe293a7153729477e20346a4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345133694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c332245a08978d4a8afccf39fd83c7fca59ddb865e211106a80bbea14422ef4`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
ENV TOMCAT_VERSION=9.0.93
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff50609e3ed14c7c3740b327b78aacfe1ea1ee52420196ee57d2b4319ae0936`  
		Last Modified: Tue, 02 Jul 2024 06:01:53 GMT  
		Size: 17.4 MB (17414986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb7392271a97e97ea73ccfd39a06b4c83857ad79f4268a59103857b0fb6cd7f`  
		Last Modified: Tue, 23 Jul 2024 01:10:00 GMT  
		Size: 158.6 MB (158586978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bdd092a67162b7a31654a479d0354e1a6bbc07290915a3afe4841c03e0d8b3`  
		Last Modified: Tue, 23 Jul 2024 01:09:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10084474a2eb75fd61510f583fe2f83d3520beeae318672023e43f531853a81c`  
		Last Modified: Thu, 25 Jul 2024 17:31:19 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befb98abccf530a5f19c42568a2da1a03a6ef2a43480e6a821eb550839222b45`  
		Last Modified: Tue, 06 Aug 2024 23:58:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83a50ff2b4162252d46da200811d3c73c60c38f15cf6fa4675fcd56cbdf293b`  
		Last Modified: Tue, 06 Aug 2024 23:58:35 GMT  
		Size: 16.3 MB (16262272 bytes)  
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
	-	`sha256:e1a9aade01ffce113d7cfda08bf474a730c4680118210ab12ddcbaa80408380c`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 5.7 MB (5653605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0642c82406e088e9b87dc2ccdfa9c739ac138b588f1f8803253baba4f758a6`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 4.5 KB (4466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77fc38010fe2ab96a79be769f8cbbe12e94051efe1f2aae63d92b37edfcbf75`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 28.0 KB (27967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d079d3a3549bbd499c16c9a21f7f5167bf8c9e3fc335bed1be811431253912`  
		Last Modified: Wed, 07 Aug 2024 00:53:09 GMT  
		Size: 116.7 MB (116738519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd71bf851100b4d4e5fa6d6d53b28e3a867f13576477d343bd62c99614882cf`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0e9274cc3b270cc1cc5033d5205d77adfa053f76107b3f203fd0c3fcfcc79`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:75b617780493693ee3d957d7736bece06fbed7aba0d8f845f624cd6c5b72e0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7496aa7772d0ef05407248c5d1243a69bb9b3956df177155c541ea0c6cc5126f`

```dockerfile
```

-	Layers:
	-	`sha256:11171ad98afc6b01ec8809097576a5f78208e51b1e0489df4b32d2fc95008a16`  
		Last Modified: Wed, 07 Aug 2024 00:53:06 GMT  
		Size: 3.9 MB (3948207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6cc0704f5a0914b87b343e3e108ead9c1411f501c0c619aba4dafb1b510d6c`  
		Last Modified: Wed, 07 Aug 2024 00:53:05 GMT  
		Size: 45.8 KB (45776 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:latest` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:732d477b2fe7e363563b236927d20a40306185762f292948a1694766514a4911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342319662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcb9fc4eb5e451ef19646ed7a7c4e72a9afb26659608eb842d24ae92a8d5fb`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 06 Jun 2024 08:12:00 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
ENV TOMCAT_VERSION=9.0.93
# Thu, 06 Jun 2024 08:12:00 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672595a5d127b59ecf75423f0ef5367642a9d021fe56a7d618121f1c21d2fd7`  
		Last Modified: Tue, 02 Jul 2024 04:35:30 GMT  
		Size: 18.8 MB (18827827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c225f5a6552449ce207f5bfbd85f6ed1a26a3b52f2a3e7270b29af2ee771cad`  
		Last Modified: Tue, 23 Jul 2024 04:15:08 GMT  
		Size: 156.8 MB (156756723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ec6fdf43db04c2e6133f92c02f91fe54d3123e5a1cabb3d0368f92a4d26831`  
		Last Modified: Tue, 23 Jul 2024 04:14:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af142f8f7ec876d457a54ad62e2b413df48ec349e9dfbbfddbc3c71251042def`  
		Last Modified: Thu, 25 Jul 2024 17:46:59 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe795db3b36027d6ee12de031961432002225529dc34c548be9607c00db2ad7`  
		Last Modified: Thu, 25 Jul 2024 23:53:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b592a45f2d3d804089c2a453c04ade3641e997d27b2d0312c806e3d7dbc66`  
		Last Modified: Wed, 07 Aug 2024 00:12:55 GMT  
		Size: 16.1 MB (16097058 bytes)  
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
	-	`sha256:d9535a6a2a5f4ad24e8a5fbf1bf5e984e456c5a2fca84053a69a979e67902f7a`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 5.5 MB (5460934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457e9fb4d96a28714651e527f7451da4029af137233074445a09357d1d7fd1d`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95114e5fea9832051ace17904eb9e9e3f9f7ef4748a7811d1398aa117998da63`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 28.0 KB (27968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa992f9162c825e211f68ca2b52a528167d86370e7aadc1c12b0311891a4360`  
		Last Modified: Wed, 07 Aug 2024 01:00:05 GMT  
		Size: 116.7 MB (116738516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0aa69208031a051249fa19626df1606e666c820ee333604c1eef006324e42`  
		Last Modified: Wed, 07 Aug 2024 01:00:03 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318d70f731a356b38ce6bcd1e0f5144080a83762c024d5367e0b04dcbbdd6574`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:ba878db6d7276d5e256a60beccc893c919a3e14bde5fa590f9374b77157add1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e58610306ca15c9862d40ac462815f683f93cdb2d270443f431a669d6b93bb`

```dockerfile
```

-	Layers:
	-	`sha256:7eef595b21fa6dbdbd3a95381a2b3351ec321709c1e08220ec57db19c7a6d28a`  
		Last Modified: Wed, 07 Aug 2024 01:00:02 GMT  
		Size: 4.0 MB (4044407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b014df6d2255ff1bb505dfd73da54cd7068bef34b49744f7c3752ddb4753f7`  
		Last Modified: Wed, 07 Aug 2024 01:00:01 GMT  
		Size: 46.4 KB (46447 bytes)  
		MIME: application/vnd.in-toto+json
