## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
