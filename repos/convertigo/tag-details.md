<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `convertigo`

-	[`convertigo:8.3`](#convertigo83)
-	[`convertigo:8.3.2`](#convertigo832)
-	[`convertigo:latest`](#convertigolatest)

## `convertigo:8.3`

```console
$ docker pull convertigo@sha256:7ccf1f358335ff897e4eabb5e03f3476ba8978edd7ca231b7b00eff52295b0d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.3` - linux; amd64

```console
$ docker pull convertigo@sha256:4a776dcd67caacb0c09ad6cca98eb5a90d601fe9a82e77753bf09dad84a5f789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342598024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef12fc0308f67d6c20ac9baf5abcdb10db1962cd2ff738da2db1727a60756d20`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["jshell"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_MAJOR=9
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_VERSION=9.0.96
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT []
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Sep 2024 16:49:48 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 19 Sep 2024 16:49:48 GMT
ENV SWT_GTK3=0
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_VERSION=8.3.1
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.1/convertigo-8.3.1.war
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 19 Sep 2024 16:49:48 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /workspace
# Thu, 19 Sep 2024 16:49:48 GMT
VOLUME [/workspace]
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5d4d56ef13b8a0dc2486230ea1989490aa6a301fbc594a8423fc3a2f861e89`  
		Last Modified: Thu, 24 Oct 2024 00:58:40 GMT  
		Size: 20.7 MB (20691339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4219879992d7c2f81b5b001a1c16992a494a179741f0e543f84b55b1c5cffa0`  
		Last Modified: Thu, 24 Oct 2024 00:58:44 GMT  
		Size: 157.6 MB (157585538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9630db58b5232fb46e6ef560b306e2517df1dae909df8fbd69fec8010c8f5568`  
		Last Modified: Thu, 24 Oct 2024 00:58:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10353dd74c3c29e485737364bc076929167f6d3f2cab9c31376eef898e729ddb`  
		Last Modified: Thu, 24 Oct 2024 00:58:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e57f58938381906263c5c9b0ff710d32b9de2adcec673458d74ca78fe599437`  
		Last Modified: Thu, 24 Oct 2024 01:55:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57077d415e426d214a64b9f7497db44b56443ce56cc46e16d592afd2ce0088fe`  
		Last Modified: Thu, 24 Oct 2024 01:55:33 GMT  
		Size: 13.7 MB (13656685 bytes)  
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
	-	`sha256:7e7774b2359e5ce6bca142d1dd4edae14a20f5b341a95d42b75edda1138819ea`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 2.4 MB (2400797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36da87cf7e5ac850c984e519ed2677e898eae2174333b41fd9eada3384af915`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0aa3b3e4877b893976665f7bfc84b6d3bfa12ba4b2ac4d86be34bafaecd566`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 27.9 KB (27942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a6266c630ea88caf644abaa9569ee4db5721e07227563cd8104f2e3fa10315`  
		Last Modified: Thu, 24 Oct 2024 02:56:21 GMT  
		Size: 118.7 MB (118690133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f650d65680d6b1015d5a1b2f56b74896306a4c0ec85df7edc9236391f862734b`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a40415834e011e2675f35e140de80f59bc27f13877713a426116d6aa57300d1`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:9e3c91d903fde04e09573e57ec9c5ca31544ca4eb5c4fc9da1d1a1ef91fd3a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adcb64077e94c222597dbdd0f9bc1c9666a7ff6fd5816d0d0675cc443b31d7`

```dockerfile
```

-	Layers:
	-	`sha256:8c1042e093f18622f0bb4d8dae0bf41319b8a13f704030cc9a16e9bf54832512`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 4.1 MB (4141478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e1efe151f04a6d698921c7175bb19dcb424853299a35286dcd52306d443b92`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 45.8 KB (45815 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.3` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:c8aad6459285018b4769ebf50bb573bd784de5c13955751fa7e23ac074a7e91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339864619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752475bea943da8c00ca7056ca321ae3493879015f832ba2ed6ea01bf660f70c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["jshell"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_MAJOR=9
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_VERSION=9.0.96
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT []
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Sep 2024 16:49:48 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 19 Sep 2024 16:49:48 GMT
ENV SWT_GTK3=0
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_VERSION=8.3.1
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.1/convertigo-8.3.1.war
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 19 Sep 2024 16:49:48 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /workspace
# Thu, 19 Sep 2024 16:49:48 GMT
VOLUME [/workspace]
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd1f22a9dd7228be27e706b25f1b3429d02ca813b8c0e0263edaa65a05911c8`  
		Last Modified: Thu, 24 Oct 2024 01:09:29 GMT  
		Size: 22.1 MB (22072026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c454e4083771448c1ca566548905f47f1628bcd3d645e5486a44156028a57`  
		Last Modified: Thu, 24 Oct 2024 01:15:08 GMT  
		Size: 155.8 MB (155805359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6fa8b0f1fe6e6b10b29a94eda5f2f8685322a6a9a25fcdf3aa25f40dd28d31`  
		Last Modified: Thu, 24 Oct 2024 01:15:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795abbf1e836cd5e5bbe1b004ef8374ccd5b8067cf7902905f2776353abd5423`  
		Last Modified: Thu, 24 Oct 2024 01:15:04 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079140ed1a9484d15ac5149bed8c7559223c85ccd76a78149a23f951dd75ab98`  
		Last Modified: Thu, 24 Oct 2024 05:03:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ce0d40c536519fa100fe562033c99fc5fbf6a9050aadaa433a236cd9003d3`  
		Last Modified: Thu, 24 Oct 2024 05:11:47 GMT  
		Size: 13.7 MB (13665965 bytes)  
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
	-	`sha256:b4760b6d84f165555f37ade943de08cfcb8ccdaa7312750aed92ec3d8a6a6611`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 2.2 MB (2234884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c77ac83bf25c7d15aa68ed6ce92e5b36907b40dec97a7d734ab3fa89c08dd`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 4.5 KB (4475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f35175381c6ba0a05feca41270153352d838b143020ce3b92bd7a2bb06bb1eb`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 27.9 KB (27946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab85da939d7b4344e1c5fb68fbcb03afbc9c27f80f82b9fee877bdf39b8b46e2`  
		Last Modified: Thu, 24 Oct 2024 12:46:07 GMT  
		Size: 118.7 MB (118690200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f608967abbf62bfa3c30537be3a2b3c85462becab4794ee696dff9b978683569`  
		Last Modified: Thu, 24 Oct 2024 12:46:05 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174ba2b1dbc2daae6b6118db20a2744c42c532d13d3f9b09476050f6b207f46`  
		Last Modified: Thu, 24 Oct 2024 12:46:05 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:4d985094dfb08cde7303fb940ae7229dbb632b6f8e877dfabd34cf362d20f64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4283026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad65925068b3c410481b8576c7197e946280b2d03fafe3b63261f8f91bb531c`

```dockerfile
```

-	Layers:
	-	`sha256:ca324759474beb5712d2becdf3cf1e1acd7dc0d17e89a4418b2899854647ee2d`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 4.2 MB (4237059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f63ad99d373d198755f56f89323e5e663962986687150582646febf8fd8bb04`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 46.0 KB (45967 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:8.3.2`

```console
$ docker pull convertigo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `convertigo:latest`

```console
$ docker pull convertigo@sha256:7ccf1f358335ff897e4eabb5e03f3476ba8978edd7ca231b7b00eff52295b0d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:4a776dcd67caacb0c09ad6cca98eb5a90d601fe9a82e77753bf09dad84a5f789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342598024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef12fc0308f67d6c20ac9baf5abcdb10db1962cd2ff738da2db1727a60756d20`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["jshell"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_MAJOR=9
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_VERSION=9.0.96
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT []
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Sep 2024 16:49:48 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 19 Sep 2024 16:49:48 GMT
ENV SWT_GTK3=0
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_VERSION=8.3.1
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.1/convertigo-8.3.1.war
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 19 Sep 2024 16:49:48 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /workspace
# Thu, 19 Sep 2024 16:49:48 GMT
VOLUME [/workspace]
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5d4d56ef13b8a0dc2486230ea1989490aa6a301fbc594a8423fc3a2f861e89`  
		Last Modified: Thu, 24 Oct 2024 00:58:40 GMT  
		Size: 20.7 MB (20691339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4219879992d7c2f81b5b001a1c16992a494a179741f0e543f84b55b1c5cffa0`  
		Last Modified: Thu, 24 Oct 2024 00:58:44 GMT  
		Size: 157.6 MB (157585538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9630db58b5232fb46e6ef560b306e2517df1dae909df8fbd69fec8010c8f5568`  
		Last Modified: Thu, 24 Oct 2024 00:58:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10353dd74c3c29e485737364bc076929167f6d3f2cab9c31376eef898e729ddb`  
		Last Modified: Thu, 24 Oct 2024 00:58:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e57f58938381906263c5c9b0ff710d32b9de2adcec673458d74ca78fe599437`  
		Last Modified: Thu, 24 Oct 2024 01:55:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57077d415e426d214a64b9f7497db44b56443ce56cc46e16d592afd2ce0088fe`  
		Last Modified: Thu, 24 Oct 2024 01:55:33 GMT  
		Size: 13.7 MB (13656685 bytes)  
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
	-	`sha256:7e7774b2359e5ce6bca142d1dd4edae14a20f5b341a95d42b75edda1138819ea`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 2.4 MB (2400797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36da87cf7e5ac850c984e519ed2677e898eae2174333b41fd9eada3384af915`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0aa3b3e4877b893976665f7bfc84b6d3bfa12ba4b2ac4d86be34bafaecd566`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 27.9 KB (27942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a6266c630ea88caf644abaa9569ee4db5721e07227563cd8104f2e3fa10315`  
		Last Modified: Thu, 24 Oct 2024 02:56:21 GMT  
		Size: 118.7 MB (118690133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f650d65680d6b1015d5a1b2f56b74896306a4c0ec85df7edc9236391f862734b`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a40415834e011e2675f35e140de80f59bc27f13877713a426116d6aa57300d1`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 2.2 KB (2243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:9e3c91d903fde04e09573e57ec9c5ca31544ca4eb5c4fc9da1d1a1ef91fd3a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adcb64077e94c222597dbdd0f9bc1c9666a7ff6fd5816d0d0675cc443b31d7`

```dockerfile
```

-	Layers:
	-	`sha256:8c1042e093f18622f0bb4d8dae0bf41319b8a13f704030cc9a16e9bf54832512`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 4.1 MB (4141478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e1efe151f04a6d698921c7175bb19dcb424853299a35286dcd52306d443b92`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 45.8 KB (45815 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:latest` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:c8aad6459285018b4769ebf50bb573bd784de5c13955751fa7e23ac074a7e91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339864619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752475bea943da8c00ca7056ca321ae3493879015f832ba2ed6ea01bf660f70c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["jshell"]
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Sep 2024 16:49:48 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_MAJOR=9
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_VERSION=9.0.96
# Thu, 19 Sep 2024 16:49:48 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT []
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Sep 2024 16:49:48 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 19 Sep 2024 16:49:48 GMT
ENV SWT_GTK3=0
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Sep 2024 16:49:48 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_VERSION=8.3.1
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.1/convertigo-8.3.1.war
# Thu, 19 Sep 2024 16:49:48 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 19 Sep 2024 16:49:48 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Thu, 19 Sep 2024 16:49:48 GMT
WORKDIR /workspace
# Thu, 19 Sep 2024 16:49:48 GMT
VOLUME [/workspace]
# Thu, 19 Sep 2024 16:49:48 GMT
EXPOSE map[28080/tcp:{}]
# Thu, 19 Sep 2024 16:49:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 19 Sep 2024 16:49:48 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd1f22a9dd7228be27e706b25f1b3429d02ca813b8c0e0263edaa65a05911c8`  
		Last Modified: Thu, 24 Oct 2024 01:09:29 GMT  
		Size: 22.1 MB (22072026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c454e4083771448c1ca566548905f47f1628bcd3d645e5486a44156028a57`  
		Last Modified: Thu, 24 Oct 2024 01:15:08 GMT  
		Size: 155.8 MB (155805359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6fa8b0f1fe6e6b10b29a94eda5f2f8685322a6a9a25fcdf3aa25f40dd28d31`  
		Last Modified: Thu, 24 Oct 2024 01:15:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795abbf1e836cd5e5bbe1b004ef8374ccd5b8067cf7902905f2776353abd5423`  
		Last Modified: Thu, 24 Oct 2024 01:15:04 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079140ed1a9484d15ac5149bed8c7559223c85ccd76a78149a23f951dd75ab98`  
		Last Modified: Thu, 24 Oct 2024 05:03:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ce0d40c536519fa100fe562033c99fc5fbf6a9050aadaa433a236cd9003d3`  
		Last Modified: Thu, 24 Oct 2024 05:11:47 GMT  
		Size: 13.7 MB (13665965 bytes)  
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
	-	`sha256:b4760b6d84f165555f37ade943de08cfcb8ccdaa7312750aed92ec3d8a6a6611`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 2.2 MB (2234884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c77ac83bf25c7d15aa68ed6ce92e5b36907b40dec97a7d734ab3fa89c08dd`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 4.5 KB (4475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f35175381c6ba0a05feca41270153352d838b143020ce3b92bd7a2bb06bb1eb`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 27.9 KB (27946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab85da939d7b4344e1c5fb68fbcb03afbc9c27f80f82b9fee877bdf39b8b46e2`  
		Last Modified: Thu, 24 Oct 2024 12:46:07 GMT  
		Size: 118.7 MB (118690200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f608967abbf62bfa3c30537be3a2b3c85462becab4794ee696dff9b978683569`  
		Last Modified: Thu, 24 Oct 2024 12:46:05 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174ba2b1dbc2daae6b6118db20a2744c42c532d13d3f9b09476050f6b207f46`  
		Last Modified: Thu, 24 Oct 2024 12:46:05 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:4d985094dfb08cde7303fb940ae7229dbb632b6f8e877dfabd34cf362d20f64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4283026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad65925068b3c410481b8576c7197e946280b2d03fafe3b63261f8f91bb531c`

```dockerfile
```

-	Layers:
	-	`sha256:ca324759474beb5712d2becdf3cf1e1acd7dc0d17e89a4418b2899854647ee2d`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 4.2 MB (4237059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f63ad99d373d198755f56f89323e5e663962986687150582646febf8fd8bb04`  
		Last Modified: Thu, 24 Oct 2024 12:46:04 GMT  
		Size: 46.0 KB (45967 bytes)  
		MIME: application/vnd.in-toto+json
