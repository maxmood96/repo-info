<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `convertigo`

-	[`convertigo:8.3`](#convertigo83)
-	[`convertigo:8.3.13`](#convertigo8313)
-	[`convertigo:8.4`](#convertigo84)
-	[`convertigo:8.4.2`](#convertigo842)
-	[`convertigo:latest`](#convertigolatest)

## `convertigo:8.3`

```console
$ docker pull convertigo@sha256:fb63fcc583e952eb1aa119bd51264f6ec652c61fc1d2e2c8020200027a73fa29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.3` - linux; amd64

```console
$ docker pull convertigo@sha256:6c0206ffab02ea8d864533313fb6b4d862595803e1609d54bfd7afe0d99d2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343316246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec33abc3c01acb591fbcad518b1e30bdbd2a360bced99ce586dbd25d6552c3d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:06 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:00:15 GMT
CMD ["jshell"]
# Fri, 08 May 2026 00:24:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 00:24:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:24:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 00:24:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_MAJOR=9
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 08 May 2026 00:24:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 08 May 2026 00:25:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:25:00 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:00 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:25:00 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 May 2026 01:15:19 GMT
ENV SWT_GTK3=0
# Fri, 08 May 2026 01:15:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:15:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:15:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:15:26 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:15:26 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 08 May 2026 01:15:26 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 08 May 2026 01:15:26 GMT
ENV CONVERTIGO_VERSION=8.3.13
# Fri, 08 May 2026 01:15:26 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.13/convertigo-8.3.13.war
# Fri, 08 May 2026 01:15:26 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 08 May 2026 01:15:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 08 May 2026 01:15:30 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 08 May 2026 01:15:30 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 01:15:31 GMT
WORKDIR /workspace
# Fri, 08 May 2026 01:15:31 GMT
VOLUME [/workspace]
# Fri, 08 May 2026 01:15:31 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 08 May 2026 01:15:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 01:15:31 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027d3fc39d04639b25ab58acc31f97c4bf3dbb5acdac90ded37e46c4273fb016`  
		Last Modified: Fri, 08 May 2026 00:00:33 GMT  
		Size: 20.7 MB (20696605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62526e041e770419a5db9d3bab84e6a66c9ee9813ca99bf386b4bad8558bfb53`  
		Last Modified: Fri, 08 May 2026 00:00:35 GMT  
		Size: 158.2 MB (158171491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb74a02a719996e19ecba8541bb65bcf48e51d48038d01c9b2458ed0699f2cf`  
		Last Modified: Fri, 08 May 2026 00:00:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6430fdd190873454b9d35ff9fb29de606c23a4b98f13cdc4e309c5935a91919`  
		Last Modified: Fri, 08 May 2026 00:00:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72de3b256789ed1540676148d8319a11ccb6a997927c0fc69f1a42b6c7caa49e`  
		Last Modified: Fri, 08 May 2026 00:25:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4956deeb4635cafcc5d70eb3c4490c95643c0c47eb1db58fccb89f10afdb6a`  
		Last Modified: Fri, 08 May 2026 00:25:12 GMT  
		Size: 14.1 MB (14068163 bytes)  
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
	-	`sha256:9aeccbc6e325050cab060fcbacac76eb5178d08bacdc848d792f58c69d5ab89a`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 1.5 MB (1489969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb83cef1b1c46f759a01f21aa86ad8022a5a0223eacaa8f41ec5b16281ea280d`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 4.5 KB (4469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e599e1bb86bc8917b4312f7a73e43eba0abe9ed522a59217f93fe5b9defb2b16`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 28.0 KB (28049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af29cbf0d2e9fb706340ae6d8752f04468073f0cc0bed9d2f979f5b47e82cc`  
		Last Modified: Fri, 08 May 2026 01:15:49 GMT  
		Size: 119.1 MB (119115401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d764456c5ed13170513953d920c1436bff6525576c46326603e0a260b8413`  
		Last Modified: Fri, 08 May 2026 01:15:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25544a2e66ee2c5143c2a62dfa5d8b1a0c5f90e825a8ac850eb4be022ccb0be`  
		Last Modified: Fri, 08 May 2026 01:15:47 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:5f83332c6d80a390d1902cf9ec447dd98f25753d63c15feb4d483b922b1707ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4392755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b16c6f3b456f0ea216c43d861efb9c56efc91d37b10cfa0df80831b0deb7f28`

```dockerfile
```

-	Layers:
	-	`sha256:9efcc4e1335464fe228c240af2bb2636a90713e022531af7171df13d62712106`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 4.3 MB (4348098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703937ccba023941cbd3db758fcc050097dae66a0feac1ce8cadc5a591eedf3f`  
		Last Modified: Fri, 08 May 2026 01:15:45 GMT  
		Size: 44.7 KB (44657 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.3` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:463bff038d4580f61e262f6b334553819fac5ab9e99406eb36ef8307997bf998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340813585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ac69d2463b070cbbe8e1060463075bd3474431750ba85f14a9fe83928dbdbd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Thu, 07 May 2026 23:59:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:36 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:44 GMT
CMD ["jshell"]
# Fri, 08 May 2026 00:24:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 00:24:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:24:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 00:24:45 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_MAJOR=9
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 08 May 2026 00:25:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 08 May 2026 00:25:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:25:17 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:17 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:25:17 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 May 2026 01:15:06 GMT
ENV SWT_GTK3=0
# Fri, 08 May 2026 01:15:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:15:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:15:06 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:15:18 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:15:18 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 08 May 2026 01:15:18 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 08 May 2026 01:15:18 GMT
ENV CONVERTIGO_VERSION=8.3.13
# Fri, 08 May 2026 01:15:18 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.13/convertigo-8.3.13.war
# Fri, 08 May 2026 01:15:18 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 08 May 2026 01:15:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 08 May 2026 01:15:26 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 08 May 2026 01:15:26 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 01:15:26 GMT
WORKDIR /workspace
# Fri, 08 May 2026 01:15:26 GMT
VOLUME [/workspace]
# Fri, 08 May 2026 01:15:26 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 08 May 2026 01:15:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 01:15:26 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2181368947beedd0baebb72cc634e546cace2a9e56153b8efdd0d9feaaff634e`  
		Last Modified: Fri, 08 May 2026 00:00:09 GMT  
		Size: 22.1 MB (22110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0531f0d9781bc622fd16a5001b25c6278b5f2cc05dc7d27e75652eecf298f88c`  
		Last Modified: Fri, 08 May 2026 00:00:14 GMT  
		Size: 156.5 MB (156473118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ad2f786476b1b167cc28c16983bc0f0f58a421522c543ac07d7e0d817b6959`  
		Last Modified: Fri, 08 May 2026 00:00:08 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26b66a0fbd4fa8104dbbeadd45120babb7b9d348817b55f93e8770c32de754b`  
		Last Modified: Fri, 08 May 2026 00:00:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646fb06cfd09a11ee08314227ee6eef5e2f767f05a4576b67cfdc28128e5adfb`  
		Last Modified: Fri, 08 May 2026 00:25:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92db7f5513b389b8da314a46f0d1d19065fef09004925e6eec8934f07bf6196a`  
		Last Modified: Fri, 08 May 2026 00:25:26 GMT  
		Size: 14.1 MB (14076724 bytes)  
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
	-	`sha256:644af1d2daf4c27a5f1563eb4e18b6122795a5f67dadf11678f3dd7df2ad197d`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 1.4 MB (1393661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f2f12d99b904908f0437dd19f7bbb02bed6520988f7f7487d8dbddab2bb5e`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 4.5 KB (4471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be5269beccb7a295df50dc5a201f2d19997e2fd353f026a5019acdd49633d3`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 28.1 KB (28055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7455442e9c53af605c2be59e90293eef544e91c41cb1ffa768c8866350c0cf35`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 119.1 MB (119115332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e5b85929c202c070511148cca25b1877d47ec534304b9a5ee0270d7d04feb4`  
		Last Modified: Fri, 08 May 2026 01:15:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393269556f8bb3301a11d48e4c848b0b9d9afe380bb4df5195a49a41b404610`  
		Last Modified: Fri, 08 May 2026 01:15:44 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3` - unknown; unknown

```console
$ docker pull convertigo@sha256:95ef55c622480c8682f410e9c4122deac817acf4af121acd94447dfa3bb83e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178506b14bf9fff2ec8b7b7b91ee7b3ed9936b1e5ed0f0ceec1a722e4d6e6ac0`

```dockerfile
```

-	Layers:
	-	`sha256:e38ef39a4ca7eccdee175beee6cfb1817f9a8b78bd6fd35c90e587e622e186d2`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 4.4 MB (4443552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e09b798e5ae1d399100c7ffa66b521edf67ba0d353bbdc9448d1dc4a58c70c7`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 44.8 KB (44797 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:8.3.13`

```console
$ docker pull convertigo@sha256:fb63fcc583e952eb1aa119bd51264f6ec652c61fc1d2e2c8020200027a73fa29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.3.13` - linux; amd64

```console
$ docker pull convertigo@sha256:6c0206ffab02ea8d864533313fb6b4d862595803e1609d54bfd7afe0d99d2814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343316246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec33abc3c01acb591fbcad518b1e30bdbd2a360bced99ce586dbd25d6552c3d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:06 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:00:15 GMT
CMD ["jshell"]
# Fri, 08 May 2026 00:24:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 00:24:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:24:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 00:24:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_MAJOR=9
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 08 May 2026 00:24:39 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 08 May 2026 00:24:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 08 May 2026 00:25:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:25:00 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:00 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:25:00 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 May 2026 01:15:19 GMT
ENV SWT_GTK3=0
# Fri, 08 May 2026 01:15:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:15:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:15:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:15:26 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:15:26 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 08 May 2026 01:15:26 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 08 May 2026 01:15:26 GMT
ENV CONVERTIGO_VERSION=8.3.13
# Fri, 08 May 2026 01:15:26 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.13/convertigo-8.3.13.war
# Fri, 08 May 2026 01:15:26 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 08 May 2026 01:15:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 08 May 2026 01:15:30 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 08 May 2026 01:15:30 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 01:15:31 GMT
WORKDIR /workspace
# Fri, 08 May 2026 01:15:31 GMT
VOLUME [/workspace]
# Fri, 08 May 2026 01:15:31 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 08 May 2026 01:15:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 01:15:31 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027d3fc39d04639b25ab58acc31f97c4bf3dbb5acdac90ded37e46c4273fb016`  
		Last Modified: Fri, 08 May 2026 00:00:33 GMT  
		Size: 20.7 MB (20696605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62526e041e770419a5db9d3bab84e6a66c9ee9813ca99bf386b4bad8558bfb53`  
		Last Modified: Fri, 08 May 2026 00:00:35 GMT  
		Size: 158.2 MB (158171491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb74a02a719996e19ecba8541bb65bcf48e51d48038d01c9b2458ed0699f2cf`  
		Last Modified: Fri, 08 May 2026 00:00:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6430fdd190873454b9d35ff9fb29de606c23a4b98f13cdc4e309c5935a91919`  
		Last Modified: Fri, 08 May 2026 00:00:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72de3b256789ed1540676148d8319a11ccb6a997927c0fc69f1a42b6c7caa49e`  
		Last Modified: Fri, 08 May 2026 00:25:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4956deeb4635cafcc5d70eb3c4490c95643c0c47eb1db58fccb89f10afdb6a`  
		Last Modified: Fri, 08 May 2026 00:25:12 GMT  
		Size: 14.1 MB (14068163 bytes)  
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
	-	`sha256:9aeccbc6e325050cab060fcbacac76eb5178d08bacdc848d792f58c69d5ab89a`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 1.5 MB (1489969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb83cef1b1c46f759a01f21aa86ad8022a5a0223eacaa8f41ec5b16281ea280d`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 4.5 KB (4469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e599e1bb86bc8917b4312f7a73e43eba0abe9ed522a59217f93fe5b9defb2b16`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 28.0 KB (28049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af29cbf0d2e9fb706340ae6d8752f04468073f0cc0bed9d2f979f5b47e82cc`  
		Last Modified: Fri, 08 May 2026 01:15:49 GMT  
		Size: 119.1 MB (119115401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d764456c5ed13170513953d920c1436bff6525576c46326603e0a260b8413`  
		Last Modified: Fri, 08 May 2026 01:15:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25544a2e66ee2c5143c2a62dfa5d8b1a0c5f90e825a8ac850eb4be022ccb0be`  
		Last Modified: Fri, 08 May 2026 01:15:47 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3.13` - unknown; unknown

```console
$ docker pull convertigo@sha256:5f83332c6d80a390d1902cf9ec447dd98f25753d63c15feb4d483b922b1707ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4392755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b16c6f3b456f0ea216c43d861efb9c56efc91d37b10cfa0df80831b0deb7f28`

```dockerfile
```

-	Layers:
	-	`sha256:9efcc4e1335464fe228c240af2bb2636a90713e022531af7171df13d62712106`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 4.3 MB (4348098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703937ccba023941cbd3db758fcc050097dae66a0feac1ce8cadc5a591eedf3f`  
		Last Modified: Fri, 08 May 2026 01:15:45 GMT  
		Size: 44.7 KB (44657 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.3.13` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:463bff038d4580f61e262f6b334553819fac5ab9e99406eb36ef8307997bf998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340813585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ac69d2463b070cbbe8e1060463075bd3474431750ba85f14a9fe83928dbdbd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Thu, 07 May 2026 23:59:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:36 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:44 GMT
CMD ["jshell"]
# Fri, 08 May 2026 00:24:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 00:24:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:24:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 00:24:45 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_MAJOR=9
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 08 May 2026 00:24:45 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 08 May 2026 00:25:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Fri, 08 May 2026 00:25:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:25:17 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:17 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:25:17 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 May 2026 01:15:06 GMT
ENV SWT_GTK3=0
# Fri, 08 May 2026 01:15:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:15:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:15:06 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:15:18 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:15:18 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 08 May 2026 01:15:18 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 08 May 2026 01:15:18 GMT
ENV CONVERTIGO_VERSION=8.3.13
# Fri, 08 May 2026 01:15:18 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.13/convertigo-8.3.13.war
# Fri, 08 May 2026 01:15:18 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 08 May 2026 01:15:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 08 May 2026 01:15:26 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 08 May 2026 01:15:26 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 01:15:26 GMT
WORKDIR /workspace
# Fri, 08 May 2026 01:15:26 GMT
VOLUME [/workspace]
# Fri, 08 May 2026 01:15:26 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 08 May 2026 01:15:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 01:15:26 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2181368947beedd0baebb72cc634e546cace2a9e56153b8efdd0d9feaaff634e`  
		Last Modified: Fri, 08 May 2026 00:00:09 GMT  
		Size: 22.1 MB (22110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0531f0d9781bc622fd16a5001b25c6278b5f2cc05dc7d27e75652eecf298f88c`  
		Last Modified: Fri, 08 May 2026 00:00:14 GMT  
		Size: 156.5 MB (156473118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ad2f786476b1b167cc28c16983bc0f0f58a421522c543ac07d7e0d817b6959`  
		Last Modified: Fri, 08 May 2026 00:00:08 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26b66a0fbd4fa8104dbbeadd45120babb7b9d348817b55f93e8770c32de754b`  
		Last Modified: Fri, 08 May 2026 00:00:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646fb06cfd09a11ee08314227ee6eef5e2f767f05a4576b67cfdc28128e5adfb`  
		Last Modified: Fri, 08 May 2026 00:25:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92db7f5513b389b8da314a46f0d1d19065fef09004925e6eec8934f07bf6196a`  
		Last Modified: Fri, 08 May 2026 00:25:26 GMT  
		Size: 14.1 MB (14076724 bytes)  
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
	-	`sha256:644af1d2daf4c27a5f1563eb4e18b6122795a5f67dadf11678f3dd7df2ad197d`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 1.4 MB (1393661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f2f12d99b904908f0437dd19f7bbb02bed6520988f7f7487d8dbddab2bb5e`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 4.5 KB (4471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be5269beccb7a295df50dc5a201f2d19997e2fd353f026a5019acdd49633d3`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 28.1 KB (28055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7455442e9c53af605c2be59e90293eef544e91c41cb1ffa768c8866350c0cf35`  
		Last Modified: Fri, 08 May 2026 01:15:46 GMT  
		Size: 119.1 MB (119115332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e5b85929c202c070511148cca25b1877d47ec534304b9a5ee0270d7d04feb4`  
		Last Modified: Fri, 08 May 2026 01:15:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393269556f8bb3301a11d48e4c848b0b9d9afe380bb4df5195a49a41b404610`  
		Last Modified: Fri, 08 May 2026 01:15:44 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.3.13` - unknown; unknown

```console
$ docker pull convertigo@sha256:95ef55c622480c8682f410e9c4122deac817acf4af121acd94447dfa3bb83e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178506b14bf9fff2ec8b7b7b91ee7b3ed9936b1e5ed0f0ceec1a722e4d6e6ac0`

```dockerfile
```

-	Layers:
	-	`sha256:e38ef39a4ca7eccdee175beee6cfb1817f9a8b78bd6fd35c90e587e622e186d2`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 4.4 MB (4443552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e09b798e5ae1d399100c7ffa66b521edf67ba0d353bbdc9448d1dc4a58c70c7`  
		Last Modified: Fri, 08 May 2026 01:15:43 GMT  
		Size: 44.8 KB (44797 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:8.4`

```console
$ docker pull convertigo@sha256:0962b49573031687ba09859870a761ce658a30b46db39ddf41d42fcd1b7a0331
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.4` - linux; amd64

```console
$ docker pull convertigo@sha256:e05ced4be1bba1aea8046dfe99428eecb1481c1760224f4764427949dc2b5620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323968609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579b184b381596f080666f61effd13b8bfff5b4c31678cd0cfc296be40dd0f4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:28:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:28:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:28:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:28:50 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:29:42 GMT
CMD ["jshell"]
# Thu, 30 Apr 2026 23:51:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 Apr 2026 23:51:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:51:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 30 Apr 2026 23:51:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:51:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_VERSION=9.0.117
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Thu, 30 Apr 2026 23:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 30 Apr 2026 23:52:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 30 Apr 2026 23:52:09 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:09 GMT
ENTRYPOINT []
# Thu, 30 Apr 2026 23:52:09 GMT
CMD ["catalina.sh" "run"]
# Fri, 01 May 2026 00:16:45 GMT
ENV SWT_GTK3=0
# Fri, 01 May 2026 00:16:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:16:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:16:46 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:16:57 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:16:58 GMT
RUN groupmod -n convertigo ubuntu   && usermod -l convertigo -d /home/convertigo -m ubuntu   && mkdir -p /workspace   && chown -R 1000:1000 /workspace   && chmod -R 777 /workspace   && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo   && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 01 May 2026 00:16:58 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_VERSION=8.4.2
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.4.2/convertigo-8.4.2.war
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 01 May 2026 00:17:07 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 01 May 2026 00:17:08 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 01 May 2026 00:17:08 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 01 May 2026 00:17:08 GMT
WORKDIR /workspace
# Fri, 01 May 2026 00:17:08 GMT
VOLUME [/workspace]
# Fri, 01 May 2026 00:17:08 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 01 May 2026 00:17:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:17:08 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c47a5c1a2f55ee2696423e5c0582023889a363dd5a3ec51a2633d6d340d973`  
		Last Modified: Thu, 30 Apr 2026 23:29:59 GMT  
		Size: 17.5 MB (17462518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38893372039c6251d8c3f63d95d127b0ce85aa0cd7250e1c5da23898f264e01`  
		Last Modified: Thu, 30 Apr 2026 23:30:01 GMT  
		Size: 92.7 MB (92708718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a694d8aa025f026ea647e2324c8daccda22c915159e8672c4a5f3e6861c91`  
		Last Modified: Thu, 30 Apr 2026 23:29:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72256642b392dc03928bb62cf11d7a0b71516f12f919cd170571452e32512580`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89019bf0833cc4fe5e63a4619c0a91d8ccddb40f0fc8bd7c282fd953561d4d`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 14.0 MB (14016964 bytes)  
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
	-	`sha256:db433f95488b3bf054fabba1a8a76e7aba537f55d23d082743cd5fd48f5da7ec`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 6.8 MB (6825004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a456470142b5748b10ca4ded2ddea7c205d0786ab5b7765566c53661954bb3c`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9460745f62642f06acdd09091c6fb4fa39916ab3e43116b2aa088ff7a21a62c`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 28.1 KB (28060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651d550bf5a1e24fc2a827bad037033a68d2a1c0bd8c0485d171d0b2d35fd0b`  
		Last Modified: Fri, 01 May 2026 00:17:32 GMT  
		Size: 163.2 MB (163185269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d465e4362792bd84389b5f16c05d2a88738b57806b5cb9f6cda796bcd39344d`  
		Last Modified: Fri, 01 May 2026 00:17:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a0e6923ec3b910676d88a2e0e0ac160f91a02a71979c1b512ca1f708ea306`  
		Last Modified: Fri, 01 May 2026 00:17:30 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.4` - unknown; unknown

```console
$ docker pull convertigo@sha256:06d67b6fe7844e3b55ef6dcfa7799fc17d2f7a097a0e6e541dafc73003365f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb8eb10e4dc8fb6e635af36a546fc16cbcf62c587758b537adf222ebd84cb3d`

```dockerfile
```

-	Layers:
	-	`sha256:a681fb97e2bf72e3bbba10f97053e1f36364cb0039923cc4bfa17fa03cda9b38`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 3.7 MB (3739884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a9283f1ec8b9025af02a52c0ac341f0472393f5c4ab002c0292740c5b3e10e`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 45.0 KB (45049 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.4` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:326aa8e2491b88e124c1505e197224fb8e0531ea67c5b18fa222245095d229f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323210206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2182c157e6f832c6dc3e3e6069c608c404195eeda9f00ec8bd398eec326357a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:29 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:29:51 GMT
CMD ["jshell"]
# Thu, 30 Apr 2026 23:50:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 Apr 2026 23:50:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 30 Apr 2026 23:50:57 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:50:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_VERSION=9.0.117
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Thu, 30 Apr 2026 23:51:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 30 Apr 2026 23:51:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 30 Apr 2026 23:51:37 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:51:37 GMT
ENTRYPOINT []
# Thu, 30 Apr 2026 23:51:37 GMT
CMD ["catalina.sh" "run"]
# Fri, 01 May 2026 00:15:47 GMT
ENV SWT_GTK3=0
# Fri, 01 May 2026 00:15:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:15:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:15:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:16:04 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:16:04 GMT
RUN groupmod -n convertigo ubuntu   && usermod -l convertigo -d /home/convertigo -m ubuntu   && mkdir -p /workspace   && chown -R 1000:1000 /workspace   && chmod -R 777 /workspace   && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo   && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 01 May 2026 00:16:04 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_VERSION=8.4.2
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.4.2/convertigo-8.4.2.war
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 01 May 2026 00:16:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 01 May 2026 00:16:12 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 01 May 2026 00:16:12 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 01 May 2026 00:16:12 GMT
WORKDIR /workspace
# Fri, 01 May 2026 00:16:12 GMT
VOLUME [/workspace]
# Fri, 01 May 2026 00:16:12 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 01 May 2026 00:16:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:16:12 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71946f2e85166645e08e0a0ee357c65b534a25494df144eb6e9ed58138e2a006`  
		Last Modified: Thu, 30 Apr 2026 23:30:09 GMT  
		Size: 18.7 MB (18654907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaea625f61cff8f5b16017e9557e81694020114b04b1ef9391e98dcb94cace4`  
		Last Modified: Thu, 30 Apr 2026 23:30:11 GMT  
		Size: 91.7 MB (91676965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3d3e809c7aa84288ce77b6c9f90f85c3e5a11b8f0de42da5f3c9afe48fddd5`  
		Last Modified: Thu, 30 Apr 2026 23:30:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0578c2a6e33b250cc9d9898f3aea3fe08ace928e717b4ba6ab40d4a8d49f112`  
		Last Modified: Thu, 30 Apr 2026 23:51:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7d7003b9b72716d432b7dc38ae243d1f154e43109c5a4816a94cf7e63c5ad7`  
		Last Modified: Thu, 30 Apr 2026 23:51:47 GMT  
		Size: 14.0 MB (14027205 bytes)  
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
	-	`sha256:bca9e9eac306e224a6d10034f663af081815a66a9c78dac03e621ed81c52ff54`  
		Last Modified: Fri, 01 May 2026 00:16:33 GMT  
		Size: 6.8 MB (6752942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45874415fd6062a1b69bc29cf96d2b9227696d528c64fb43addb8601485b2ba`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 3.6 KB (3624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270d22a89b5948cb9e68e2bd4508d1dca57cf49eff29fd8f16c5362aa58214d`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 28.1 KB (28054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63c301add3277a654af4fcf39b26e222c0d8847da5602c8423311d785e97da`  
		Last Modified: Fri, 01 May 2026 00:16:36 GMT  
		Size: 163.2 MB (163185248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4333b8d91a54c332a6c2813ec0f901b62a8c0e0d3cd0dab4fe24d22069eb0a`  
		Last Modified: Fri, 01 May 2026 00:16:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c25e3884259d2a122c14db6f0c2489ed8ad83e04f00d14dabb114989c3034e`  
		Last Modified: Fri, 01 May 2026 00:16:34 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.4` - unknown; unknown

```console
$ docker pull convertigo@sha256:d920ecf9ed97fac1e9b7bdf4f2d089df583e351f5f75161d27567af1e601fa64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8efb7b84505ec90fc0cf6664085f5064544c3f12031c9ea6db8d47db5ffe70`

```dockerfile
```

-	Layers:
	-	`sha256:71ac5eca0d2cfc4e23a23c25dcee3d7617cdc588305560cbf5752ae1700a9e70`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 3.9 MB (3871387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826250d4f8bde81b80890b7464e78627575dfb0fe0aa26235f0478d992f93d8e`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 45.2 KB (45201 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:8.4.2`

```console
$ docker pull convertigo@sha256:0962b49573031687ba09859870a761ce658a30b46db39ddf41d42fcd1b7a0331
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:8.4.2` - linux; amd64

```console
$ docker pull convertigo@sha256:e05ced4be1bba1aea8046dfe99428eecb1481c1760224f4764427949dc2b5620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323968609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579b184b381596f080666f61effd13b8bfff5b4c31678cd0cfc296be40dd0f4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:28:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:28:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:28:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:28:50 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:29:42 GMT
CMD ["jshell"]
# Thu, 30 Apr 2026 23:51:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 Apr 2026 23:51:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:51:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 30 Apr 2026 23:51:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:51:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_VERSION=9.0.117
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Thu, 30 Apr 2026 23:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 30 Apr 2026 23:52:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 30 Apr 2026 23:52:09 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:09 GMT
ENTRYPOINT []
# Thu, 30 Apr 2026 23:52:09 GMT
CMD ["catalina.sh" "run"]
# Fri, 01 May 2026 00:16:45 GMT
ENV SWT_GTK3=0
# Fri, 01 May 2026 00:16:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:16:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:16:46 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:16:57 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:16:58 GMT
RUN groupmod -n convertigo ubuntu   && usermod -l convertigo -d /home/convertigo -m ubuntu   && mkdir -p /workspace   && chown -R 1000:1000 /workspace   && chmod -R 777 /workspace   && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo   && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 01 May 2026 00:16:58 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_VERSION=8.4.2
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.4.2/convertigo-8.4.2.war
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 01 May 2026 00:17:07 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 01 May 2026 00:17:08 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 01 May 2026 00:17:08 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 01 May 2026 00:17:08 GMT
WORKDIR /workspace
# Fri, 01 May 2026 00:17:08 GMT
VOLUME [/workspace]
# Fri, 01 May 2026 00:17:08 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 01 May 2026 00:17:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:17:08 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c47a5c1a2f55ee2696423e5c0582023889a363dd5a3ec51a2633d6d340d973`  
		Last Modified: Thu, 30 Apr 2026 23:29:59 GMT  
		Size: 17.5 MB (17462518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38893372039c6251d8c3f63d95d127b0ce85aa0cd7250e1c5da23898f264e01`  
		Last Modified: Thu, 30 Apr 2026 23:30:01 GMT  
		Size: 92.7 MB (92708718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a694d8aa025f026ea647e2324c8daccda22c915159e8672c4a5f3e6861c91`  
		Last Modified: Thu, 30 Apr 2026 23:29:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72256642b392dc03928bb62cf11d7a0b71516f12f919cd170571452e32512580`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89019bf0833cc4fe5e63a4619c0a91d8ccddb40f0fc8bd7c282fd953561d4d`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 14.0 MB (14016964 bytes)  
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
	-	`sha256:db433f95488b3bf054fabba1a8a76e7aba537f55d23d082743cd5fd48f5da7ec`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 6.8 MB (6825004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a456470142b5748b10ca4ded2ddea7c205d0786ab5b7765566c53661954bb3c`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9460745f62642f06acdd09091c6fb4fa39916ab3e43116b2aa088ff7a21a62c`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 28.1 KB (28060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651d550bf5a1e24fc2a827bad037033a68d2a1c0bd8c0485d171d0b2d35fd0b`  
		Last Modified: Fri, 01 May 2026 00:17:32 GMT  
		Size: 163.2 MB (163185269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d465e4362792bd84389b5f16c05d2a88738b57806b5cb9f6cda796bcd39344d`  
		Last Modified: Fri, 01 May 2026 00:17:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a0e6923ec3b910676d88a2e0e0ac160f91a02a71979c1b512ca1f708ea306`  
		Last Modified: Fri, 01 May 2026 00:17:30 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.4.2` - unknown; unknown

```console
$ docker pull convertigo@sha256:06d67b6fe7844e3b55ef6dcfa7799fc17d2f7a097a0e6e541dafc73003365f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb8eb10e4dc8fb6e635af36a546fc16cbcf62c587758b537adf222ebd84cb3d`

```dockerfile
```

-	Layers:
	-	`sha256:a681fb97e2bf72e3bbba10f97053e1f36364cb0039923cc4bfa17fa03cda9b38`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 3.7 MB (3739884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a9283f1ec8b9025af02a52c0ac341f0472393f5c4ab002c0292740c5b3e10e`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 45.0 KB (45049 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:8.4.2` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:326aa8e2491b88e124c1505e197224fb8e0531ea67c5b18fa222245095d229f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323210206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2182c157e6f832c6dc3e3e6069c608c404195eeda9f00ec8bd398eec326357a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:29 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:29:51 GMT
CMD ["jshell"]
# Thu, 30 Apr 2026 23:50:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 Apr 2026 23:50:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 30 Apr 2026 23:50:57 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:50:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_VERSION=9.0.117
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Thu, 30 Apr 2026 23:51:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 30 Apr 2026 23:51:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 30 Apr 2026 23:51:37 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:51:37 GMT
ENTRYPOINT []
# Thu, 30 Apr 2026 23:51:37 GMT
CMD ["catalina.sh" "run"]
# Fri, 01 May 2026 00:15:47 GMT
ENV SWT_GTK3=0
# Fri, 01 May 2026 00:15:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:15:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:15:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:16:04 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:16:04 GMT
RUN groupmod -n convertigo ubuntu   && usermod -l convertigo -d /home/convertigo -m ubuntu   && mkdir -p /workspace   && chown -R 1000:1000 /workspace   && chmod -R 777 /workspace   && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo   && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 01 May 2026 00:16:04 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_VERSION=8.4.2
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.4.2/convertigo-8.4.2.war
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 01 May 2026 00:16:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 01 May 2026 00:16:12 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 01 May 2026 00:16:12 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 01 May 2026 00:16:12 GMT
WORKDIR /workspace
# Fri, 01 May 2026 00:16:12 GMT
VOLUME [/workspace]
# Fri, 01 May 2026 00:16:12 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 01 May 2026 00:16:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:16:12 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71946f2e85166645e08e0a0ee357c65b534a25494df144eb6e9ed58138e2a006`  
		Last Modified: Thu, 30 Apr 2026 23:30:09 GMT  
		Size: 18.7 MB (18654907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaea625f61cff8f5b16017e9557e81694020114b04b1ef9391e98dcb94cace4`  
		Last Modified: Thu, 30 Apr 2026 23:30:11 GMT  
		Size: 91.7 MB (91676965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3d3e809c7aa84288ce77b6c9f90f85c3e5a11b8f0de42da5f3c9afe48fddd5`  
		Last Modified: Thu, 30 Apr 2026 23:30:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0578c2a6e33b250cc9d9898f3aea3fe08ace928e717b4ba6ab40d4a8d49f112`  
		Last Modified: Thu, 30 Apr 2026 23:51:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7d7003b9b72716d432b7dc38ae243d1f154e43109c5a4816a94cf7e63c5ad7`  
		Last Modified: Thu, 30 Apr 2026 23:51:47 GMT  
		Size: 14.0 MB (14027205 bytes)  
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
	-	`sha256:bca9e9eac306e224a6d10034f663af081815a66a9c78dac03e621ed81c52ff54`  
		Last Modified: Fri, 01 May 2026 00:16:33 GMT  
		Size: 6.8 MB (6752942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45874415fd6062a1b69bc29cf96d2b9227696d528c64fb43addb8601485b2ba`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 3.6 KB (3624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270d22a89b5948cb9e68e2bd4508d1dca57cf49eff29fd8f16c5362aa58214d`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 28.1 KB (28054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63c301add3277a654af4fcf39b26e222c0d8847da5602c8423311d785e97da`  
		Last Modified: Fri, 01 May 2026 00:16:36 GMT  
		Size: 163.2 MB (163185248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4333b8d91a54c332a6c2813ec0f901b62a8c0e0d3cd0dab4fe24d22069eb0a`  
		Last Modified: Fri, 01 May 2026 00:16:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c25e3884259d2a122c14db6f0c2489ed8ad83e04f00d14dabb114989c3034e`  
		Last Modified: Fri, 01 May 2026 00:16:34 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:8.4.2` - unknown; unknown

```console
$ docker pull convertigo@sha256:d920ecf9ed97fac1e9b7bdf4f2d089df583e351f5f75161d27567af1e601fa64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8efb7b84505ec90fc0cf6664085f5064544c3f12031c9ea6db8d47db5ffe70`

```dockerfile
```

-	Layers:
	-	`sha256:71ac5eca0d2cfc4e23a23c25dcee3d7617cdc588305560cbf5752ae1700a9e70`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 3.9 MB (3871387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826250d4f8bde81b80890b7464e78627575dfb0fe0aa26235f0478d992f93d8e`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 45.2 KB (45201 bytes)  
		MIME: application/vnd.in-toto+json

## `convertigo:latest`

```console
$ docker pull convertigo@sha256:0962b49573031687ba09859870a761ce658a30b46db39ddf41d42fcd1b7a0331
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:e05ced4be1bba1aea8046dfe99428eecb1481c1760224f4764427949dc2b5620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323968609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579b184b381596f080666f61effd13b8bfff5b4c31678cd0cfc296be40dd0f4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:28:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:28:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:28:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:28:50 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:29:42 GMT
CMD ["jshell"]
# Thu, 30 Apr 2026 23:51:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 Apr 2026 23:51:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:51:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 30 Apr 2026 23:51:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:51:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_VERSION=9.0.117
# Thu, 30 Apr 2026 23:51:10 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Thu, 30 Apr 2026 23:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 30 Apr 2026 23:52:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 30 Apr 2026 23:52:09 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:09 GMT
ENTRYPOINT []
# Thu, 30 Apr 2026 23:52:09 GMT
CMD ["catalina.sh" "run"]
# Fri, 01 May 2026 00:16:45 GMT
ENV SWT_GTK3=0
# Fri, 01 May 2026 00:16:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:16:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:16:46 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:16:57 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:16:58 GMT
RUN groupmod -n convertigo ubuntu   && usermod -l convertigo -d /home/convertigo -m ubuntu   && mkdir -p /workspace   && chown -R 1000:1000 /workspace   && chmod -R 777 /workspace   && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo   && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 01 May 2026 00:16:58 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_VERSION=8.4.2
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.4.2/convertigo-8.4.2.war
# Fri, 01 May 2026 00:16:58 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 01 May 2026 00:17:07 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 01 May 2026 00:17:08 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 01 May 2026 00:17:08 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 01 May 2026 00:17:08 GMT
WORKDIR /workspace
# Fri, 01 May 2026 00:17:08 GMT
VOLUME [/workspace]
# Fri, 01 May 2026 00:17:08 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 01 May 2026 00:17:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:17:08 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c47a5c1a2f55ee2696423e5c0582023889a363dd5a3ec51a2633d6d340d973`  
		Last Modified: Thu, 30 Apr 2026 23:29:59 GMT  
		Size: 17.5 MB (17462518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38893372039c6251d8c3f63d95d127b0ce85aa0cd7250e1c5da23898f264e01`  
		Last Modified: Thu, 30 Apr 2026 23:30:01 GMT  
		Size: 92.7 MB (92708718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a694d8aa025f026ea647e2324c8daccda22c915159e8672c4a5f3e6861c91`  
		Last Modified: Thu, 30 Apr 2026 23:29:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72256642b392dc03928bb62cf11d7a0b71516f12f919cd170571452e32512580`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89019bf0833cc4fe5e63a4619c0a91d8ccddb40f0fc8bd7c282fd953561d4d`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 14.0 MB (14016964 bytes)  
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
	-	`sha256:db433f95488b3bf054fabba1a8a76e7aba537f55d23d082743cd5fd48f5da7ec`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 6.8 MB (6825004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a456470142b5748b10ca4ded2ddea7c205d0786ab5b7765566c53661954bb3c`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9460745f62642f06acdd09091c6fb4fa39916ab3e43116b2aa088ff7a21a62c`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 28.1 KB (28060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651d550bf5a1e24fc2a827bad037033a68d2a1c0bd8c0485d171d0b2d35fd0b`  
		Last Modified: Fri, 01 May 2026 00:17:32 GMT  
		Size: 163.2 MB (163185269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d465e4362792bd84389b5f16c05d2a88738b57806b5cb9f6cda796bcd39344d`  
		Last Modified: Fri, 01 May 2026 00:17:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a0e6923ec3b910676d88a2e0e0ac160f91a02a71979c1b512ca1f708ea306`  
		Last Modified: Fri, 01 May 2026 00:17:30 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:06d67b6fe7844e3b55ef6dcfa7799fc17d2f7a097a0e6e541dafc73003365f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb8eb10e4dc8fb6e635af36a546fc16cbcf62c587758b537adf222ebd84cb3d`

```dockerfile
```

-	Layers:
	-	`sha256:a681fb97e2bf72e3bbba10f97053e1f36364cb0039923cc4bfa17fa03cda9b38`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 3.7 MB (3739884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a9283f1ec8b9025af02a52c0ac341f0472393f5c4ab002c0292740c5b3e10e`  
		Last Modified: Fri, 01 May 2026 00:17:28 GMT  
		Size: 45.0 KB (45049 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:latest` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:326aa8e2491b88e124c1505e197224fb8e0531ea67c5b18fa222245095d229f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323210206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2182c157e6f832c6dc3e3e6069c608c404195eeda9f00ec8bd398eec326357a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:29 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:29:51 GMT
CMD ["jshell"]
# Thu, 30 Apr 2026 23:50:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 Apr 2026 23:50:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 30 Apr 2026 23:50:57 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:50:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_VERSION=9.0.117
# Thu, 30 Apr 2026 23:50:57 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Thu, 30 Apr 2026 23:51:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 30 Apr 2026 23:51:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 30 Apr 2026 23:51:37 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:51:37 GMT
ENTRYPOINT []
# Thu, 30 Apr 2026 23:51:37 GMT
CMD ["catalina.sh" "run"]
# Fri, 01 May 2026 00:15:47 GMT
ENV SWT_GTK3=0
# Fri, 01 May 2026 00:15:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:15:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:15:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:16:04 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     tini     unzip   && apt-get remove -y --purge libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:16:04 GMT
RUN groupmod -n convertigo ubuntu   && usermod -l convertigo -d /home/convertigo -m ubuntu   && mkdir -p /workspace   && chown -R 1000:1000 /workspace   && chmod -R 777 /workspace   && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo   && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Fri, 01 May 2026 00:16:04 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_VERSION=8.4.2
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.4.2/convertigo-8.4.2.war
# Fri, 01 May 2026 00:16:04 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Fri, 01 May 2026 00:16:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Fri, 01 May 2026 00:16:12 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Fri, 01 May 2026 00:16:12 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Fri, 01 May 2026 00:16:12 GMT
WORKDIR /workspace
# Fri, 01 May 2026 00:16:12 GMT
VOLUME [/workspace]
# Fri, 01 May 2026 00:16:12 GMT
EXPOSE map[28080/tcp:{}]
# Fri, 01 May 2026 00:16:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:16:12 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71946f2e85166645e08e0a0ee357c65b534a25494df144eb6e9ed58138e2a006`  
		Last Modified: Thu, 30 Apr 2026 23:30:09 GMT  
		Size: 18.7 MB (18654907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaea625f61cff8f5b16017e9557e81694020114b04b1ef9391e98dcb94cace4`  
		Last Modified: Thu, 30 Apr 2026 23:30:11 GMT  
		Size: 91.7 MB (91676965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3d3e809c7aa84288ce77b6c9f90f85c3e5a11b8f0de42da5f3c9afe48fddd5`  
		Last Modified: Thu, 30 Apr 2026 23:30:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0578c2a6e33b250cc9d9898f3aea3fe08ace928e717b4ba6ab40d4a8d49f112`  
		Last Modified: Thu, 30 Apr 2026 23:51:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7d7003b9b72716d432b7dc38ae243d1f154e43109c5a4816a94cf7e63c5ad7`  
		Last Modified: Thu, 30 Apr 2026 23:51:47 GMT  
		Size: 14.0 MB (14027205 bytes)  
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
	-	`sha256:bca9e9eac306e224a6d10034f663af081815a66a9c78dac03e621ed81c52ff54`  
		Last Modified: Fri, 01 May 2026 00:16:33 GMT  
		Size: 6.8 MB (6752942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45874415fd6062a1b69bc29cf96d2b9227696d528c64fb43addb8601485b2ba`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 3.6 KB (3624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270d22a89b5948cb9e68e2bd4508d1dca57cf49eff29fd8f16c5362aa58214d`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 28.1 KB (28054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63c301add3277a654af4fcf39b26e222c0d8847da5602c8423311d785e97da`  
		Last Modified: Fri, 01 May 2026 00:16:36 GMT  
		Size: 163.2 MB (163185248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4333b8d91a54c332a6c2813ec0f901b62a8c0e0d3cd0dab4fe24d22069eb0a`  
		Last Modified: Fri, 01 May 2026 00:16:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c25e3884259d2a122c14db6f0c2489ed8ad83e04f00d14dabb114989c3034e`  
		Last Modified: Fri, 01 May 2026 00:16:34 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:d920ecf9ed97fac1e9b7bdf4f2d089df583e351f5f75161d27567af1e601fa64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8efb7b84505ec90fc0cf6664085f5064544c3f12031c9ea6db8d47db5ffe70`

```dockerfile
```

-	Layers:
	-	`sha256:71ac5eca0d2cfc4e23a23c25dcee3d7617cdc588305560cbf5752ae1700a9e70`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 3.9 MB (3871387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826250d4f8bde81b80890b7464e78627575dfb0fe0aa26235f0478d992f93d8e`  
		Last Modified: Fri, 01 May 2026 00:16:32 GMT  
		Size: 45.2 KB (45201 bytes)  
		MIME: application/vnd.in-toto+json
