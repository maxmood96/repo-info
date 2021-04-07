## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:1f343e2d9bcd5a5281f4863cc82ce4714cc887497ad31511ceef70c16b0face0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:5b47378546ead0e5a296db5e2bc6682153de0ceed5e1c7a072c07c1127eff42c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.3 MB (717336792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc0d2606038880c316d044f93ae409e662957db2fcd005149f5630d5ad14017`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:29:56 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 03 Apr 2021 01:30:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 03 Apr 2021 01:30:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Apr 2021 01:30:06 GMT
CMD ["jshell"]
# Tue, 06 Apr 2021 22:33:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Apr 2021 22:33:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Apr 2021 22:33:02 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 06 Apr 2021 22:33:02 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Apr 2021 22:33:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Apr 2021 22:33:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Apr 2021 23:01:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 06 Apr 2021 23:01:09 GMT
ENV TOMCAT_MAJOR=8
# Tue, 06 Apr 2021 23:01:09 GMT
ENV TOMCAT_VERSION=8.5.65
# Tue, 06 Apr 2021 23:01:09 GMT
ENV TOMCAT_SHA512=eb5a77d75a46496f7de39c1cba5f4fc4991ec7da7717e7b37ad48b4ca2ea334aeabfd094f64977477b4b2352637b56e30e5d9acfcdf7ccd5f4269a824829dd39
# Tue, 06 Apr 2021 23:01:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 06 Apr 2021 23:01:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 06 Apr 2021 23:01:46 GMT
EXPOSE 8080
# Tue, 06 Apr 2021 23:01:46 GMT
CMD ["catalina.sh" "run"]
# Wed, 07 Apr 2021 00:08:13 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 07 Apr 2021 00:11:39 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 07 Apr 2021 00:13:26 GMT
ENV XWIKI_VERSION=12.10.5
# Wed, 07 Apr 2021 00:13:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.5
# Wed, 07 Apr 2021 00:13:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=3ec3d0ea12e763cc8eb7a1d818428f033c3d5fd6804bced52f33c29c13db0cc5
# Wed, 07 Apr 2021 00:14:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 07 Apr 2021 00:14:06 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 07 Apr 2021 00:14:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 07 Apr 2021 00:14:07 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 07 Apr 2021 00:14:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 07 Apr 2021 00:14:08 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 07 Apr 2021 00:14:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 07 Apr 2021 00:14:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Apr 2021 00:14:08 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829aace300712fbc22a01a55f7581113a5a44b31718a09d4e34a9b4858f57c32`  
		Last Modified: Sat, 03 Apr 2021 01:40:24 GMT  
		Size: 195.0 MB (194975287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b815ec2e095191665d1d4e398d63a78becec95bc228b19d8d98a528f7a96b890`  
		Last Modified: Tue, 06 Apr 2021 23:17:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b3c06bab8d9f7074a571ce3822d43092c45bc12518209a4b7e0c475de084b2`  
		Last Modified: Tue, 06 Apr 2021 23:33:59 GMT  
		Size: 11.7 MB (11652630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7106005a7ddb08f8d98799f25a8cd49938beb4875e25ecf3f63cadf90ce3e0`  
		Last Modified: Tue, 06 Apr 2021 23:33:57 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cc96e5753ea591bd516dda4379e7d6c3ad4ca381ebebec6cadb9b4ee934cfe`  
		Last Modified: Wed, 07 Apr 2021 00:18:16 GMT  
		Size: 168.2 MB (168244415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a428cc3ce5691d20b47c59e6c550e4b37cad1d47320de4ddff9873ac8b038a8`  
		Last Modified: Wed, 07 Apr 2021 00:20:02 GMT  
		Size: 297.1 MB (297054277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ded8a6ff207881f06621e44e8bc507b2a682234f635eff9187612a327bd60eb`  
		Last Modified: Wed, 07 Apr 2021 00:19:41 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fb3ff4fdaf4d4abbd96583441a22cfa67e83ef5d1f2e8a492cb7713d0a92`  
		Last Modified: Wed, 07 Apr 2021 00:19:42 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0a1a3d918242c251b4e87b120f98a490bd9cb621dff3f32040c03413d76392`  
		Last Modified: Wed, 07 Apr 2021 00:19:41 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47208c84b6538b2953b574bf65f87c15af29205b01875c54e0af7a14ca819db`  
		Last Modified: Wed, 07 Apr 2021 00:19:41 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735d07f155f561875dc9bc1693e5b2eaab4f3f19f48449d76bf7ffa5dfaf693a`  
		Last Modified: Wed, 07 Apr 2021 00:19:41 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:4fff6e7909cdd189a33aaee5aa93ca072d71f634b038533d779719f461c5ad08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.6 MB (708638357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ad0e46a7cd56cf6e71c0745315d4ed491d8992c9387f0c76a49aff8b1e2c3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 03 Apr 2021 04:10:04 GMT
ADD file:5a9b188c70f1f07ae9d68f3eb7aa18a1683faf50d5ff20eda1b04db3255877b9 in / 
# Sat, 03 Apr 2021 04:10:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 04:10:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 04:10:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 04:10:14 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 05:41:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 05:41:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 05:41:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 03 Apr 2021 05:42:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 03 Apr 2021 05:42:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Apr 2021 05:42:14 GMT
CMD ["jshell"]
# Tue, 06 Apr 2021 21:42:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Apr 2021 21:42:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Apr 2021 21:42:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 06 Apr 2021 21:42:54 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Apr 2021 21:42:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Apr 2021 21:42:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Apr 2021 22:31:18 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 06 Apr 2021 22:31:19 GMT
ENV TOMCAT_MAJOR=8
# Tue, 06 Apr 2021 22:31:20 GMT
ENV TOMCAT_VERSION=8.5.65
# Tue, 06 Apr 2021 22:31:21 GMT
ENV TOMCAT_SHA512=eb5a77d75a46496f7de39c1cba5f4fc4991ec7da7717e7b37ad48b4ca2ea334aeabfd094f64977477b4b2352637b56e30e5d9acfcdf7ccd5f4269a824829dd39
# Tue, 06 Apr 2021 22:32:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 06 Apr 2021 22:32:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 06 Apr 2021 22:32:21 GMT
EXPOSE 8080
# Tue, 06 Apr 2021 22:32:22 GMT
CMD ["catalina.sh" "run"]
# Tue, 06 Apr 2021 23:29:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 06 Apr 2021 23:30:17 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 06 Apr 2021 23:31:19 GMT
ENV XWIKI_VERSION=12.10.5
# Tue, 06 Apr 2021 23:31:19 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.5
# Tue, 06 Apr 2021 23:31:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=3ec3d0ea12e763cc8eb7a1d818428f033c3d5fd6804bced52f33c29c13db0cc5
# Tue, 06 Apr 2021 23:31:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 06 Apr 2021 23:31:49 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 06 Apr 2021 23:31:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 06 Apr 2021 23:31:51 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 06 Apr 2021 23:31:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 06 Apr 2021 23:31:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 06 Apr 2021 23:31:54 GMT
VOLUME [/usr/local/xwiki]
# Tue, 06 Apr 2021 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Apr 2021 23:31:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2b20d1a80822f7dbd2175f235caa068029e82a265d0924d4f4d39c1bf9dc7f9b`  
		Last Modified: Thu, 01 Apr 2021 08:25:41 GMT  
		Size: 27.2 MB (27176807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e993c4ee9ad2dd0f069e7c34bbf137c835c5a2c2cc3f111e37fba05c79c1d7`  
		Last Modified: Sat, 03 Apr 2021 04:11:51 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2befefc5146bc156f83e891873a69526513f1e942e3d2bf68129f1e2fa17613`  
		Last Modified: Sat, 03 Apr 2021 04:11:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f1b84b0f5e74897b899c79e269e294408197cec9b0f1770ff44d654874d22c`  
		Last Modified: Sat, 03 Apr 2021 05:53:32 GMT  
		Size: 15.9 MB (15894829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6799fbb357c5362d0c8dc8e0452c5ecccfb04cb4f71d12c6a92f63052465d`  
		Last Modified: Sat, 03 Apr 2021 05:53:53 GMT  
		Size: 191.7 MB (191730005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb7c397f8cf2ca1a918a37b8c3ddf1a62378f7ff96ee4d31c995aaba933e34e`  
		Last Modified: Tue, 06 Apr 2021 22:48:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44225db9e34c6761b77ba10c977855d93922b803ef56e710480661406082ecae`  
		Last Modified: Tue, 06 Apr 2021 22:57:17 GMT  
		Size: 11.7 MB (11671523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8bb66010dfed1f9d69b4e3de2094e0f93de93697382c2ed418b145c995fb5`  
		Last Modified: Tue, 06 Apr 2021 22:57:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7340b1930e2e1a9c286692ae6a6a4f3ac848d30342ec2314c5833bdee11c7e90`  
		Last Modified: Tue, 06 Apr 2021 23:33:52 GMT  
		Size: 164.3 MB (164302476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a9893f0fe0a1b675b45356642c326c7193e87cf0a3cadf8ed2efd822b69158`  
		Last Modified: Tue, 06 Apr 2021 23:34:43 GMT  
		Size: 297.1 MB (297054430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fd765f88d96109e532fc3c02478cc417ef6f3857613138d8a2145e61cee2f`  
		Last Modified: Tue, 06 Apr 2021 23:34:10 GMT  
		Size: 795.4 KB (795423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd138ec8e03f96790a91b8b3526122f04ecc045434d1c4d282bf8e09d3b7e96f`  
		Last Modified: Tue, 06 Apr 2021 23:34:10 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c119833c77ca6a6982cf5d61651f37eb3eb69e0b7af7b4711b7f2da5ff743479`  
		Last Modified: Tue, 06 Apr 2021 23:34:10 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e474334a9507d186df41b6cca3f383a3a5021f6e1f703bf4558fbcb8c8713f`  
		Last Modified: Tue, 06 Apr 2021 23:34:10 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9c320f157325370cd0dd6660492c781d36ad796d60b8b1f05a5ffc00aa42da`  
		Last Modified: Tue, 06 Apr 2021 23:34:10 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
