## `convertigo:latest`

```console
$ docker pull convertigo@sha256:1870a3bd3a0102150e7c89f4e7f9c0c69637fee5375bfb21356243d38833fbef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:2846744dbdfeb9cd9f6ad53659b373cfffe7512be2dbd525bbf539a8ab08ca73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348356522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bdf100b9ccb3c2255fbc2edb19577f6cc2c1a1605e7ec8d562de14afbf1cdc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Mon, 04 Nov 2024 09:52:53 GMT
ARG RELEASE
# Mon, 04 Nov 2024 09:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 04 Nov 2024 09:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 04 Nov 2024 09:52:53 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 04 Nov 2024 09:52:53 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 09:52:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 04 Nov 2024 09:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 09:52:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["jshell"]
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 09:52:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
WORKDIR /usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 04 Nov 2024 09:52:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_MAJOR=9
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_VERSION=9.0.100
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_SHA512=e0b1379866d09b54f2743afb382c32a33bca9652c379467c1fa0a5b15a1b98830ae23fb1d8f96c43148844ce95b6c1d22a66db3f8efaf41f225b158c3cb71c92
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 04 Nov 2024 09:52:53 GMT
ENTRYPOINT []
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["catalina.sh" "run"]
# Mon, 04 Nov 2024 09:52:53 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Mon, 04 Nov 2024 09:52:53 GMT
ENV SWT_GTK3=0
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
WORKDIR /usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CONVERTIGO_VERSION=8.3.2
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.2/convertigo-8.3.2.war
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Mon, 04 Nov 2024 09:52:53 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
WORKDIR /workspace
# Mon, 04 Nov 2024 09:52:53 GMT
VOLUME [/workspace]
# Mon, 04 Nov 2024 09:52:53 GMT
EXPOSE map[28080/tcp:{}]
# Mon, 04 Nov 2024 09:52:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ce665314df6489df49d894b81a8b7d89dcbb3916abb4b8f2d9f04f7f30fba`  
		Last Modified: Tue, 04 Feb 2025 07:21:28 GMT  
		Size: 20.7 MB (20684621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c63f325f81a44cbc524343f5cdcec789fb188c2333543d3238cdac7cfeafb7`  
		Last Modified: Tue, 04 Feb 2025 07:18:33 GMT  
		Size: 157.6 MB (157591234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864a83d54ff514b209c491364b5476319cda130d7de9e481c432148668d4f0ab`  
		Last Modified: Tue, 04 Feb 2025 07:30:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8df0decf9d7f3577a33fb03b83ae0fc1cb904ea030014ac9bc7a5954ccbfec`  
		Last Modified: Tue, 04 Feb 2025 07:16:07 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b63ff0952bb268c5f085ec4677be5a09b3902fef14f07d2c4e11f35150a80`  
		Last Modified: Wed, 19 Feb 2025 00:29:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e48874e1e7c7c89b05c6ad00c6ff96f8ae6a6afcfd6efd15dcb186abd8cac2`  
		Last Modified: Wed, 19 Feb 2025 00:29:37 GMT  
		Size: 19.4 MB (19382045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219110cb4f6b6b6e26b8f9ab4c779c357317f8441dcacc30f8769b83e1067817`  
		Last Modified: Wed, 19 Feb 2025 01:09:10 GMT  
		Size: 2.4 MB (2431455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3532cd43b13c88d0330ca1c92c884a94165b7f70a58d6ef4ec46e8626dd2f997`  
		Last Modified: Wed, 19 Feb 2025 01:09:02 GMT  
		Size: 4.5 KB (4465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c5ca795b82f21a36b938d3aac591dd067d0b0dbcbd945491730bd534b124e`  
		Last Modified: Wed, 19 Feb 2025 01:09:02 GMT  
		Size: 28.0 KB (27990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73065e809055432042cf14d144db155fc55303797d214b120ad6beddbb9cc08`  
		Last Modified: Wed, 19 Feb 2025 01:09:14 GMT  
		Size: 118.7 MB (118693337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064ea5d8b8411a7c23bca0679d2da090c4c450d7dc3c7f1f844d5b8f7dd28256`  
		Last Modified: Wed, 19 Feb 2025 01:09:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c04d34e777adef0492808c98392ca75fc9a627fe54d25abc08ac685307ed78`  
		Last Modified: Wed, 19 Feb 2025 01:09:02 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:7ccad2fbeb63aabaea3edd553a354134c8151d4ffb9eb2559e08d82639eb2e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0738c8f058de8150178a55ee10b49294d81f8bb788d41be143ccfb5a8678cb50`

```dockerfile
```

-	Layers:
	-	`sha256:c4c9f3b47e332537884338685a0b9a14c7925cbb112d86fd06d4bd024be8e789`  
		Last Modified: Wed, 19 Feb 2025 02:59:17 GMT  
		Size: 4.1 MB (4137401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e600ffc63ad76624989894d516ba65df5f0b105ba23e9e0816cc3767ac6ec4`  
		Last Modified: Wed, 19 Feb 2025 02:59:18 GMT  
		Size: 45.1 KB (45145 bytes)  
		MIME: application/vnd.in-toto+json

### `convertigo:latest` - linux; arm64 variant v8

```console
$ docker pull convertigo@sha256:67f928eb4a67963de3494e80918c3e523746a591b39e4d3377664974c72a98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344595045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d7df5ea6bd06a6bfcca1ed51bd2fe7a7b412d430f44341d2f94c2d98390104`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Mon, 04 Nov 2024 09:52:53 GMT
ARG RELEASE
# Mon, 04 Nov 2024 09:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 04 Nov 2024 09:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 04 Nov 2024 09:52:53 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 04 Nov 2024 09:52:53 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 09:52:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 04 Nov 2024 09:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 09:52:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["jshell"]
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 09:52:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
WORKDIR /usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 04 Nov 2024 09:52:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_MAJOR=9
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_VERSION=9.0.100
# Mon, 04 Nov 2024 09:52:53 GMT
ENV TOMCAT_SHA512=e0b1379866d09b54f2743afb382c32a33bca9652c379467c1fa0a5b15a1b98830ae23fb1d8f96c43148844ce95b6c1d22a66db3f8efaf41f225b158c3cb71c92
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 04 Nov 2024 09:52:53 GMT
ENTRYPOINT []
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["catalina.sh" "run"]
# Mon, 04 Nov 2024 09:52:53 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Mon, 04 Nov 2024 09:52:53 GMT
ENV SWT_GTK3=0
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
WORKDIR /usr/local/tomcat
# Mon, 04 Nov 2024 09:52:53 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     gosu     sudo     tini     unzip   && apt-get remove -y --purge wget libfreetype6   && apt-get autoremove -y   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace     && chown -R convertigo:convertigo /workspace     && chmod -R 777 /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n        <Valve className="org.apache.catalina.valves.ErrorReportValve"  errorCode.404="webapps/convertigo/404.html" errorCode.0="webapps/convertigo/error.html" showReport="false" showServerInfo="false" />\n      </Host>,'         -e 's,</Service>,<!--SSL<Connector port="28443" protocol="org.apache.coyote.http11.Http11AprProtocol" SSLEnabled="true" maxThreads="64000" relaxedQueryChars="{}[]|">\n      <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol" />\n      <SSLHostConfig>\n        <Certificate certificateKeyFile="/certs/key.pem"\n                     certificateFile="/certs/cert.pem"\n                     certificateChainFile="/certs/chain.pem"\n                     type="RSA" />\n      </SSLHostConfig>\n    </Connector>SSL-->\n  </Service>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*     && chmod 777 conf/context.xml conf/server.xml # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CONVERTIGO_VERSION=8.3.2
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/8.3.2/convertigo-8.3.2.war
# Mon, 04 Nov 2024 09:52:53 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Mon, 04 Nov 2024 09:52:53 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && mkdir /certs && chmod 777 /certs     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && chmod 777 WEB-INF/web.xml WEB-INF/lib WEB-INF/classes         && rm -rf /tmp/*) # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
COPY ./root-index.html webapps/ROOT/index.html # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
COPY ./docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 09:52:53 GMT
WORKDIR /workspace
# Mon, 04 Nov 2024 09:52:53 GMT
VOLUME [/workspace]
# Mon, 04 Nov 2024 09:52:53 GMT
EXPOSE map[28080/tcp:{}]
# Mon, 04 Nov 2024 09:52:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 09:52:53 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917805cfb6502c189ce3cf996ddbc16ac349000799293570d30f8455b5182667`  
		Last Modified: Tue, 04 Feb 2025 13:17:34 GMT  
		Size: 22.1 MB (22066656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59234f8844652c8c120816e45f1ec1e0a572df42dc02216a900effd642bcaa7a`  
		Last Modified: Tue, 04 Feb 2025 14:34:31 GMT  
		Size: 155.9 MB (155867873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bc701a616a1c3a463bab5785d49f63264c0d90e7b71527b22f03f2acdfc402`  
		Last Modified: Tue, 04 Feb 2025 15:27:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c78c35442c357eb9d11a68f29737b48872f43824c72b85021cf5bd4dd1726d7`  
		Last Modified: Tue, 04 Feb 2025 13:30:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63f6ee592cd9471e8bf598a533978dd31f35c541fc3eacea0ad51f3e5dc362d`  
		Last Modified: Wed, 05 Feb 2025 07:15:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa47c8ad2e214158d5ab6e94c8da49a046edd8e000a3182cdab762eb5ba7465`  
		Last Modified: Wed, 19 Feb 2025 01:15:12 GMT  
		Size: 18.3 MB (18309155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2b692f62a6e30d4a1c08d343fa1f2e0f68c30032a7ecc91d59005c06be398f`  
		Last Modified: Wed, 19 Feb 2025 02:20:59 GMT  
		Size: 2.3 MB (2261948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f20270b5635c3500f5d2ff28d8f6aa978c8960ed5871db340bfc9b8004daf`  
		Last Modified: Wed, 19 Feb 2025 02:20:52 GMT  
		Size: 4.5 KB (4468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2555cca835628c0a0d4f215a20be1745a1ca3d0ae82a4d1a182dc27a5b392b`  
		Last Modified: Wed, 19 Feb 2025 02:20:52 GMT  
		Size: 28.0 KB (28005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cb451e8018341a73fa1c6118823461decba6a28597dba76e4cd40a44efe374`  
		Last Modified: Wed, 19 Feb 2025 02:21:15 GMT  
		Size: 118.7 MB (118693322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5ec1ec5af6599abed128a5cfcd7ccfac7df796f1707695962dce8768bec5d8`  
		Last Modified: Wed, 19 Feb 2025 02:20:52 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b84d10468f811c3549cd9d3ff8c6654c79f6fe9759cd2883afd1f7913dec2`  
		Last Modified: Wed, 19 Feb 2025 02:20:51 GMT  
		Size: 2.2 KB (2244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `convertigo:latest` - unknown; unknown

```console
$ docker pull convertigo@sha256:4da71dd658c801715782121738b76ace28cf8d7c6cc3b6ca6b08eca2a2aee948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15122128210fc92c91e91b97c2cf88cec8e86f72c143c754d4a99cd382971f5c`

```dockerfile
```

-	Layers:
	-	`sha256:08ce11ec8e4c655b8a6e4e43c3030971c12026beecb094da2041bbb79a73724a`  
		Last Modified: Wed, 19 Feb 2025 05:59:20 GMT  
		Size: 4.2 MB (4232866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78cb0972432068a406c2702e5b4845498ae0b70efec51d80aa694baa476842a`  
		Last Modified: Wed, 19 Feb 2025 05:59:21 GMT  
		Size: 45.3 KB (45297 bytes)  
		MIME: application/vnd.in-toto+json
