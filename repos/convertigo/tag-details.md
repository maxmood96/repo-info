<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `convertigo`

-	[`convertigo:7.8`](#convertigo78)
-	[`convertigo:7.8.0`](#convertigo780)
-	[`convertigo:latest`](#convertigolatest)

## `convertigo:7.8`

```console
$ docker pull convertigo@sha256:6c4ae08f664617e300bfd971cd8e235430c89733f6f0293e90a7319f549a6a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `convertigo:7.8` - linux; amd64

```console
$ docker pull convertigo@sha256:ab8185474db2c5835d19f66c5b1d89bc8e8e01ccb2100a76d2ae7e43d3c1112e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436717049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91348e62d4388aec2a831293c3bba9620a432c40d1d28babf13a4c7cf4c20687`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:36 GMT
ADD file:53e587afdbeaee60cc14bd95907f14c8303c04b98c72f98e2c54d4343f15dd38 in / 
# Tue, 12 Jan 2021 00:32:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:57:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 03:57:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Mon, 01 Feb 2021 19:54:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:54:24 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:54:24 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:54:25 GMT
ENV JAVA_VERSION=11.0.10
# Mon, 01 Feb 2021 19:54:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:54:40 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:13:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:13:22 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:13:23 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:13:23 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:13:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:13:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:23:56 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:23:56 GMT
ENV TOMCAT_MAJOR=9
# Mon, 01 Feb 2021 23:23:56 GMT
ENV TOMCAT_VERSION=9.0.41
# Mon, 01 Feb 2021 23:23:57 GMT
ENV TOMCAT_SHA512=b6450e590a37c5bccf049b1176c441f0964796995e80d4c7c7d9fb74f9ad817107c303b6b83ed3d71c9251b2b8acf334b90a4abdf9deea122e338643cece0766
# Mon, 01 Feb 2021 23:24:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 01 Feb 2021 23:24:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 01 Feb 2021 23:24:25 GMT
EXPOSE 8080
# Mon, 01 Feb 2021 23:24:26 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Feb 2021 00:30:53 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Tue, 02 Feb 2021 00:30:54 GMT
ENV SWT_GTK3=0
# Tue, 02 Feb 2021 00:30:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Feb 2021 00:30:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 02 Feb 2021 00:30:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Feb 2021 00:30:59 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     unzip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Feb 2021 00:30:59 GMT
ENV GOSU_VERSION=1.11
# Tue, 02 Feb 2021 00:31:00 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Tue, 02 Feb 2021 00:31:00 GMT
ENV TINI_VERSION=0.18.0
# Tue, 02 Feb 2021 00:31:00 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Tue, 02 Feb 2021 00:31:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Tue, 02 Feb 2021 00:31:03 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace
# Tue, 02 Feb 2021 00:31:04 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Tue, 02 Feb 2021 00:31:04 GMT
ENV CONVERTIGO_VERSION=7.8.0
# Tue, 02 Feb 2021 00:31:05 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.8.0/convertigo-7.8.0.war
# Tue, 02 Feb 2021 00:31:05 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Tue, 02 Feb 2021 00:31:10 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Tue, 02 Feb 2021 00:31:10 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Tue, 02 Feb 2021 00:31:11 GMT
COPY file:589b02719ed77f1ee0adbb9d091153c2e2e219c7df46f5474a836963de39b7cc in / 
# Tue, 02 Feb 2021 00:31:11 GMT
WORKDIR /workspace
# Tue, 02 Feb 2021 00:31:11 GMT
VOLUME [/workspace]
# Tue, 02 Feb 2021 00:31:11 GMT
EXPOSE 28080
# Tue, 02 Feb 2021 00:31:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Feb 2021 00:31:12 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:b9a857cbf04d2c0d2f0f6b73e894b20a977a6d3b6edd9e27d080e03142954950`  
		Last Modified: Tue, 12 Jan 2021 00:38:49 GMT  
		Size: 50.4 MB (50399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d557ee20540b597f518df05bc6888778cfc92bf46040c701d4a622389feb6807`  
		Last Modified: Tue, 12 Jan 2021 04:05:56 GMT  
		Size: 7.8 MB (7812018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ca4f00c2e4896c65625d678544b764d7483dca9dcab92b62093db72f21d3e`  
		Last Modified: Tue, 12 Jan 2021 04:05:55 GMT  
		Size: 10.0 MB (9996375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667fd949ed9338da3c1e09f9b75408c214368c637c448e0fd839467f6f7717b5`  
		Last Modified: Tue, 12 Jan 2021 04:06:20 GMT  
		Size: 51.8 MB (51830144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a945768a17999f090b8cc2ca5b0f89742cd646480cec3e3b146ba8d2c33333`  
		Last Modified: Mon, 01 Feb 2021 20:09:02 GMT  
		Size: 5.6 MB (5587010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f45feafbf988c84bdb4b986ae2db0fffe28598b5609722b383b91329fbfaf`  
		Last Modified: Mon, 01 Feb 2021 20:09:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179e0e40c2056fe2c0f9b29fcb582e5c098270af39f0352304d4324b71a45e8`  
		Last Modified: Mon, 01 Feb 2021 20:09:19 GMT  
		Size: 202.8 MB (202803309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d659cf2d36fdfbc5aedb396c32f27a3414f25dce8f2cc6bf72144015e94c7ebe`  
		Last Modified: Mon, 01 Feb 2021 23:46:03 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2ad1203c1c5e4dc0efe97e3ccb14d2f94f06ed87f5a02b6a83f0b415900a5e`  
		Last Modified: Mon, 01 Feb 2021 23:48:02 GMT  
		Size: 12.5 MB (12452588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfec769b96c0e8d0e8e48e24fef21517599ef67680b452b667ea9b6f4ba5e09`  
		Last Modified: Mon, 01 Feb 2021 23:48:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a1221f4485d8c09dd7cf29189fd094e7988c82316c014b148313a5b0f05536`  
		Last Modified: Tue, 02 Feb 2021 00:31:24 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dced813ad82c47ebc151cef9c35cda05495fdc32b78e2cc5ef4d0d127b9519d`  
		Last Modified: Tue, 02 Feb 2021 00:31:25 GMT  
		Size: 910.1 KB (910088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb5447f6f5aec7ea37404790cdd4a8ff43375ec053a0dab13a11f2b1a04bd0f`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7c814bf0c2cc7915322e2b5065b9ead21bcd5906a69b2b059201d061ba0f14`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 27.3 KB (27321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969cd4cc2f6a0c259f8d9bb898281ffdc1349c7afb2a79c25ab3b45d37e915b9`  
		Last Modified: Tue, 02 Feb 2021 00:31:31 GMT  
		Size: 94.9 MB (94892142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692579ff613f479aa2b5101e2448a991075640ff7804a6ca918a93f9539b0274`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0161c5110a43d9e745d8a7b5f9d7c83291cfd416592671a4d8b238fb63b1b1`  
		Last Modified: Tue, 02 Feb 2021 00:31:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `convertigo:7.8.0`

```console
$ docker pull convertigo@sha256:6c4ae08f664617e300bfd971cd8e235430c89733f6f0293e90a7319f549a6a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `convertigo:7.8.0` - linux; amd64

```console
$ docker pull convertigo@sha256:ab8185474db2c5835d19f66c5b1d89bc8e8e01ccb2100a76d2ae7e43d3c1112e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436717049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91348e62d4388aec2a831293c3bba9620a432c40d1d28babf13a4c7cf4c20687`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:36 GMT
ADD file:53e587afdbeaee60cc14bd95907f14c8303c04b98c72f98e2c54d4343f15dd38 in / 
# Tue, 12 Jan 2021 00:32:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:57:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 03:57:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Mon, 01 Feb 2021 19:54:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:54:24 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:54:24 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:54:25 GMT
ENV JAVA_VERSION=11.0.10
# Mon, 01 Feb 2021 19:54:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:54:40 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:13:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:13:22 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:13:23 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:13:23 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:13:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:13:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:23:56 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:23:56 GMT
ENV TOMCAT_MAJOR=9
# Mon, 01 Feb 2021 23:23:56 GMT
ENV TOMCAT_VERSION=9.0.41
# Mon, 01 Feb 2021 23:23:57 GMT
ENV TOMCAT_SHA512=b6450e590a37c5bccf049b1176c441f0964796995e80d4c7c7d9fb74f9ad817107c303b6b83ed3d71c9251b2b8acf334b90a4abdf9deea122e338643cece0766
# Mon, 01 Feb 2021 23:24:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 01 Feb 2021 23:24:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 01 Feb 2021 23:24:25 GMT
EXPOSE 8080
# Mon, 01 Feb 2021 23:24:26 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Feb 2021 00:30:53 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Tue, 02 Feb 2021 00:30:54 GMT
ENV SWT_GTK3=0
# Tue, 02 Feb 2021 00:30:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Feb 2021 00:30:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 02 Feb 2021 00:30:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Feb 2021 00:30:59 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     unzip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Feb 2021 00:30:59 GMT
ENV GOSU_VERSION=1.11
# Tue, 02 Feb 2021 00:31:00 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Tue, 02 Feb 2021 00:31:00 GMT
ENV TINI_VERSION=0.18.0
# Tue, 02 Feb 2021 00:31:00 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Tue, 02 Feb 2021 00:31:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Tue, 02 Feb 2021 00:31:03 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace
# Tue, 02 Feb 2021 00:31:04 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Tue, 02 Feb 2021 00:31:04 GMT
ENV CONVERTIGO_VERSION=7.8.0
# Tue, 02 Feb 2021 00:31:05 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.8.0/convertigo-7.8.0.war
# Tue, 02 Feb 2021 00:31:05 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Tue, 02 Feb 2021 00:31:10 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Tue, 02 Feb 2021 00:31:10 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Tue, 02 Feb 2021 00:31:11 GMT
COPY file:589b02719ed77f1ee0adbb9d091153c2e2e219c7df46f5474a836963de39b7cc in / 
# Tue, 02 Feb 2021 00:31:11 GMT
WORKDIR /workspace
# Tue, 02 Feb 2021 00:31:11 GMT
VOLUME [/workspace]
# Tue, 02 Feb 2021 00:31:11 GMT
EXPOSE 28080
# Tue, 02 Feb 2021 00:31:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Feb 2021 00:31:12 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:b9a857cbf04d2c0d2f0f6b73e894b20a977a6d3b6edd9e27d080e03142954950`  
		Last Modified: Tue, 12 Jan 2021 00:38:49 GMT  
		Size: 50.4 MB (50399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d557ee20540b597f518df05bc6888778cfc92bf46040c701d4a622389feb6807`  
		Last Modified: Tue, 12 Jan 2021 04:05:56 GMT  
		Size: 7.8 MB (7812018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ca4f00c2e4896c65625d678544b764d7483dca9dcab92b62093db72f21d3e`  
		Last Modified: Tue, 12 Jan 2021 04:05:55 GMT  
		Size: 10.0 MB (9996375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667fd949ed9338da3c1e09f9b75408c214368c637c448e0fd839467f6f7717b5`  
		Last Modified: Tue, 12 Jan 2021 04:06:20 GMT  
		Size: 51.8 MB (51830144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a945768a17999f090b8cc2ca5b0f89742cd646480cec3e3b146ba8d2c33333`  
		Last Modified: Mon, 01 Feb 2021 20:09:02 GMT  
		Size: 5.6 MB (5587010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f45feafbf988c84bdb4b986ae2db0fffe28598b5609722b383b91329fbfaf`  
		Last Modified: Mon, 01 Feb 2021 20:09:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179e0e40c2056fe2c0f9b29fcb582e5c098270af39f0352304d4324b71a45e8`  
		Last Modified: Mon, 01 Feb 2021 20:09:19 GMT  
		Size: 202.8 MB (202803309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d659cf2d36fdfbc5aedb396c32f27a3414f25dce8f2cc6bf72144015e94c7ebe`  
		Last Modified: Mon, 01 Feb 2021 23:46:03 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2ad1203c1c5e4dc0efe97e3ccb14d2f94f06ed87f5a02b6a83f0b415900a5e`  
		Last Modified: Mon, 01 Feb 2021 23:48:02 GMT  
		Size: 12.5 MB (12452588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfec769b96c0e8d0e8e48e24fef21517599ef67680b452b667ea9b6f4ba5e09`  
		Last Modified: Mon, 01 Feb 2021 23:48:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a1221f4485d8c09dd7cf29189fd094e7988c82316c014b148313a5b0f05536`  
		Last Modified: Tue, 02 Feb 2021 00:31:24 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dced813ad82c47ebc151cef9c35cda05495fdc32b78e2cc5ef4d0d127b9519d`  
		Last Modified: Tue, 02 Feb 2021 00:31:25 GMT  
		Size: 910.1 KB (910088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb5447f6f5aec7ea37404790cdd4a8ff43375ec053a0dab13a11f2b1a04bd0f`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7c814bf0c2cc7915322e2b5065b9ead21bcd5906a69b2b059201d061ba0f14`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 27.3 KB (27321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969cd4cc2f6a0c259f8d9bb898281ffdc1349c7afb2a79c25ab3b45d37e915b9`  
		Last Modified: Tue, 02 Feb 2021 00:31:31 GMT  
		Size: 94.9 MB (94892142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692579ff613f479aa2b5101e2448a991075640ff7804a6ca918a93f9539b0274`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0161c5110a43d9e745d8a7b5f9d7c83291cfd416592671a4d8b238fb63b1b1`  
		Last Modified: Tue, 02 Feb 2021 00:31:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `convertigo:latest`

```console
$ docker pull convertigo@sha256:6c4ae08f664617e300bfd971cd8e235430c89733f6f0293e90a7319f549a6a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:ab8185474db2c5835d19f66c5b1d89bc8e8e01ccb2100a76d2ae7e43d3c1112e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436717049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91348e62d4388aec2a831293c3bba9620a432c40d1d28babf13a4c7cf4c20687`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:36 GMT
ADD file:53e587afdbeaee60cc14bd95907f14c8303c04b98c72f98e2c54d4343f15dd38 in / 
# Tue, 12 Jan 2021 00:32:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:57:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 03:57:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Mon, 01 Feb 2021 19:54:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:54:24 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:54:24 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:54:25 GMT
ENV JAVA_VERSION=11.0.10
# Mon, 01 Feb 2021 19:54:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:54:40 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:13:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:13:22 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:13:23 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:13:23 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:13:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:13:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:23:56 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:23:56 GMT
ENV TOMCAT_MAJOR=9
# Mon, 01 Feb 2021 23:23:56 GMT
ENV TOMCAT_VERSION=9.0.41
# Mon, 01 Feb 2021 23:23:57 GMT
ENV TOMCAT_SHA512=b6450e590a37c5bccf049b1176c441f0964796995e80d4c7c7d9fb74f9ad817107c303b6b83ed3d71c9251b2b8acf334b90a4abdf9deea122e338643cece0766
# Mon, 01 Feb 2021 23:24:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 01 Feb 2021 23:24:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 01 Feb 2021 23:24:25 GMT
EXPOSE 8080
# Mon, 01 Feb 2021 23:24:26 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Feb 2021 00:30:53 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Tue, 02 Feb 2021 00:30:54 GMT
ENV SWT_GTK3=0
# Tue, 02 Feb 2021 00:30:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Feb 2021 00:30:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 02 Feb 2021 00:30:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Feb 2021 00:30:59 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     unzip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Feb 2021 00:30:59 GMT
ENV GOSU_VERSION=1.11
# Tue, 02 Feb 2021 00:31:00 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Tue, 02 Feb 2021 00:31:00 GMT
ENV TINI_VERSION=0.18.0
# Tue, 02 Feb 2021 00:31:00 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Tue, 02 Feb 2021 00:31:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Tue, 02 Feb 2021 00:31:03 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace
# Tue, 02 Feb 2021 00:31:04 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Tue, 02 Feb 2021 00:31:04 GMT
ENV CONVERTIGO_VERSION=7.8.0
# Tue, 02 Feb 2021 00:31:05 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.8.0/convertigo-7.8.0.war
# Tue, 02 Feb 2021 00:31:05 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Tue, 02 Feb 2021 00:31:10 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Tue, 02 Feb 2021 00:31:10 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Tue, 02 Feb 2021 00:31:11 GMT
COPY file:589b02719ed77f1ee0adbb9d091153c2e2e219c7df46f5474a836963de39b7cc in / 
# Tue, 02 Feb 2021 00:31:11 GMT
WORKDIR /workspace
# Tue, 02 Feb 2021 00:31:11 GMT
VOLUME [/workspace]
# Tue, 02 Feb 2021 00:31:11 GMT
EXPOSE 28080
# Tue, 02 Feb 2021 00:31:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Feb 2021 00:31:12 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:b9a857cbf04d2c0d2f0f6b73e894b20a977a6d3b6edd9e27d080e03142954950`  
		Last Modified: Tue, 12 Jan 2021 00:38:49 GMT  
		Size: 50.4 MB (50399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d557ee20540b597f518df05bc6888778cfc92bf46040c701d4a622389feb6807`  
		Last Modified: Tue, 12 Jan 2021 04:05:56 GMT  
		Size: 7.8 MB (7812018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ca4f00c2e4896c65625d678544b764d7483dca9dcab92b62093db72f21d3e`  
		Last Modified: Tue, 12 Jan 2021 04:05:55 GMT  
		Size: 10.0 MB (9996375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667fd949ed9338da3c1e09f9b75408c214368c637c448e0fd839467f6f7717b5`  
		Last Modified: Tue, 12 Jan 2021 04:06:20 GMT  
		Size: 51.8 MB (51830144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a945768a17999f090b8cc2ca5b0f89742cd646480cec3e3b146ba8d2c33333`  
		Last Modified: Mon, 01 Feb 2021 20:09:02 GMT  
		Size: 5.6 MB (5587010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f45feafbf988c84bdb4b986ae2db0fffe28598b5609722b383b91329fbfaf`  
		Last Modified: Mon, 01 Feb 2021 20:09:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179e0e40c2056fe2c0f9b29fcb582e5c098270af39f0352304d4324b71a45e8`  
		Last Modified: Mon, 01 Feb 2021 20:09:19 GMT  
		Size: 202.8 MB (202803309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d659cf2d36fdfbc5aedb396c32f27a3414f25dce8f2cc6bf72144015e94c7ebe`  
		Last Modified: Mon, 01 Feb 2021 23:46:03 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2ad1203c1c5e4dc0efe97e3ccb14d2f94f06ed87f5a02b6a83f0b415900a5e`  
		Last Modified: Mon, 01 Feb 2021 23:48:02 GMT  
		Size: 12.5 MB (12452588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfec769b96c0e8d0e8e48e24fef21517599ef67680b452b667ea9b6f4ba5e09`  
		Last Modified: Mon, 01 Feb 2021 23:48:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a1221f4485d8c09dd7cf29189fd094e7988c82316c014b148313a5b0f05536`  
		Last Modified: Tue, 02 Feb 2021 00:31:24 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dced813ad82c47ebc151cef9c35cda05495fdc32b78e2cc5ef4d0d127b9519d`  
		Last Modified: Tue, 02 Feb 2021 00:31:25 GMT  
		Size: 910.1 KB (910088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb5447f6f5aec7ea37404790cdd4a8ff43375ec053a0dab13a11f2b1a04bd0f`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7c814bf0c2cc7915322e2b5065b9ead21bcd5906a69b2b059201d061ba0f14`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 27.3 KB (27321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969cd4cc2f6a0c259f8d9bb898281ffdc1349c7afb2a79c25ab3b45d37e915b9`  
		Last Modified: Tue, 02 Feb 2021 00:31:31 GMT  
		Size: 94.9 MB (94892142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692579ff613f479aa2b5101e2448a991075640ff7804a6ca918a93f9539b0274`  
		Last Modified: Tue, 02 Feb 2021 00:31:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0161c5110a43d9e745d8a7b5f9d7c83291cfd416592671a4d8b238fb63b1b1`  
		Last Modified: Tue, 02 Feb 2021 00:31:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
