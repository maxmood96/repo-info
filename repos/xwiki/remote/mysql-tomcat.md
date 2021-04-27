## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:eb9e5eaf9e9da0860ce5c22fd17a316d7fc15748736ae26112e0d3e0e0edbcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3d235bf30e3ed404bd987938decfeacb8cfca76ae176177deb1ead0c1924a252
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.7 MB (722705095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe7a360c3633c157806e5395dab874932ecd16222e8a6bb79933d51d9cbf1c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 23:23:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:23:20 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Fri, 23 Apr 2021 23:23:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 23:23:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:23:30 GMT
CMD ["jshell"]
# Sat, 24 Apr 2021 05:30:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 24 Apr 2021 05:30:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 05:30:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 24 Apr 2021 05:30:01 GMT
WORKDIR /usr/local/tomcat
# Sat, 24 Apr 2021 05:30:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 24 Apr 2021 05:30:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 24 Apr 2021 05:38:14 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 24 Apr 2021 05:38:15 GMT
ENV TOMCAT_MAJOR=8
# Sat, 24 Apr 2021 05:38:15 GMT
ENV TOMCAT_VERSION=8.5.65
# Sat, 24 Apr 2021 05:38:15 GMT
ENV TOMCAT_SHA512=eb5a77d75a46496f7de39c1cba5f4fc4991ec7da7717e7b37ad48b4ca2ea334aeabfd094f64977477b4b2352637b56e30e5d9acfcdf7ccd5f4269a824829dd39
# Sat, 24 Apr 2021 05:38:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Sat, 24 Apr 2021 05:38:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 24 Apr 2021 05:38:48 GMT
EXPOSE 8080
# Sat, 24 Apr 2021 05:38:48 GMT
CMD ["catalina.sh" "run"]
# Sat, 24 Apr 2021 06:11:35 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 24 Apr 2021 06:13:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Mon, 26 Apr 2021 19:52:27 GMT
ENV XWIKI_VERSION=13.3
# Mon, 26 Apr 2021 19:52:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.3
# Mon, 26 Apr 2021 19:52:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=fc832fe94defff52ac06f1f91408a6c349fc114c652e5413f529373ecdef13ad
# Mon, 26 Apr 2021 19:53:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Mon, 26 Apr 2021 19:53:07 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Mon, 26 Apr 2021 19:53:07 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Mon, 26 Apr 2021 19:53:07 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Mon, 26 Apr 2021 19:53:07 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Mon, 26 Apr 2021 19:53:07 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Mon, 26 Apr 2021 19:53:09 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Mon, 26 Apr 2021 19:53:09 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Mon, 26 Apr 2021 19:53:09 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Mon, 26 Apr 2021 19:53:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Mon, 26 Apr 2021 19:53:10 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 26 Apr 2021 19:53:10 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Apr 2021 19:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Apr 2021 19:53:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592ec2d7c1370aca6ef48ee1d20fbb3a4c148db400adc5dc575778c681f5dba0`  
		Last Modified: Fri, 23 Apr 2021 23:32:39 GMT  
		Size: 16.0 MB (16034099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bba3e5e0dc52b48e0360da5bff4e392e591272470f35bcbe8770cc13b7c698`  
		Last Modified: Fri, 23 Apr 2021 23:33:40 GMT  
		Size: 195.0 MB (194975297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77e1e1efbb0f6d54cbdfddfe01a8639623052e77bcdd025a23c71eb5bb9875`  
		Last Modified: Sat, 24 Apr 2021 05:46:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0fc299d766fbfc5a5dc292ce77c17fcbccc2e93530157fa8ba2784014af055`  
		Last Modified: Sat, 24 Apr 2021 05:50:22 GMT  
		Size: 11.7 MB (11653995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9d90b17b9fc9897512087651a6397ffc61543cde6d844436a8f9a473d57ebd`  
		Last Modified: Sat, 24 Apr 2021 05:50:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671706dc448af40a2824f35f2688090a2791c0a48a84d4b79dc117043095c634`  
		Last Modified: Sat, 24 Apr 2021 06:18:24 GMT  
		Size: 167.4 MB (167448894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faee2bab0640962f7c7983693dabaa27972b05e2e1e12dc1931dbcfa126806fd`  
		Last Modified: Mon, 26 Apr 2021 19:55:04 GMT  
		Size: 301.8 MB (301782703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271937d6b490065b2071a225c54924f31083ffe78a5a06c38d4ac232e403f58f`  
		Last Modified: Mon, 26 Apr 2021 19:54:44 GMT  
		Size: 2.3 MB (2257819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9705f22a44d514f412006bbe668e2a60b02566ec280b897e4c40c28c82aed26e`  
		Last Modified: Mon, 26 Apr 2021 19:54:43 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd630a72924d32ca49c25f0fe6aa9bd87d5e9882d7195b3097d8ae9c2081a5a`  
		Last Modified: Mon, 26 Apr 2021 19:54:43 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853330af2f667ccec57b0ad61e7cf6914d6d7ea251f81fc8839fe59eb8f184dd`  
		Last Modified: Mon, 26 Apr 2021 19:54:43 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d584438f79368f632d5d32162794ea967e69c02d7d8236922c28481c4c1984`  
		Last Modified: Mon, 26 Apr 2021 19:54:44 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
