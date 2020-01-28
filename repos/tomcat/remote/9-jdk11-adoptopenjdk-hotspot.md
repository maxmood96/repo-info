## `tomcat:9-jdk11-adoptopenjdk-hotspot`

```console
$ docker pull tomcat@sha256:9e4de93bd03cb529ec5fd2d4ac95c7ed156736ccb2f80fcabcc8df8756f1fc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `tomcat:9-jdk11-adoptopenjdk-hotspot` - linux; amd64

```console
$ docker pull tomcat@sha256:22e43fa869a834dced4c1fb8ff302eda4cea7637a6fac74804c9589e336abc8d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250139270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7401045b47cce37aa2ee06a3806d1c4c26a299d0df3ed32f8512e2668bc09158`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Jan 2020 01:20:31 GMT
ADD file:08e718ed0796013f5957a1be7da3bef6225f3d82d8be0a86a7114e5caad50cbc in / 
# Thu, 16 Jan 2020 01:20:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:20:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:20:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:20:34 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:44:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2020 01:45:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 00:19:44 GMT
ENV JAVA_VERSION=jdk-11.0.6+10
# Tue, 28 Jan 2020 00:19:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04b77f6754aed68528f39750c5cfd6a439190206aff216aa081d62a0e1a794fa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.6_10.tar.gz';          ;;        armhf)          ESUM='ab5b76203e54fe7a5221535f6f407efa43153de029a746f60af3cffb7cb5080b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.6_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9247f0271744188489b0dd628cab90e76ca1f22fa3bbcdebd9bfc4f140908df5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.6_10.tar.gz';          ;;        s390x)          ESUM='250fc79db2d6c70e655ff319e2db8ca205858bf82c9f30b040bda0c90cd9f583';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.6_10.tar.gz';          ;;        amd64|x86_64)          ESUM='330d19a2eaa07ed02757d7a785a77bab49f5ee710ea03b4ee2fa220ddd0feffc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 28 Jan 2020 00:19:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 00:19:56 GMT
CMD ["jshell"]
# Tue, 28 Jan 2020 02:10:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2020 02:10:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 02:10:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jan 2020 02:10:20 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2020 02:10:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 02:10:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 02:10:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 28 Jan 2020 02:10:21 GMT
ENV TOMCAT_MAJOR=9
# Tue, 28 Jan 2020 02:10:21 GMT
ENV TOMCAT_VERSION=9.0.30
# Tue, 28 Jan 2020 02:10:21 GMT
ENV TOMCAT_SHA512=40bf428a534816317e5e8732b679e6d73f6ed977aab4ac5e2b9eaf1eb087eaa68a18b0fd3da8c39ca4b96f5b6fd919dec84517abba0d5e797285ade934a92990
# Tue, 28 Jan 2020 02:11:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Tue, 28 Jan 2020 02:11:19 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 28 Jan 2020 02:11:19 GMT
EXPOSE 8080
# Tue, 28 Jan 2020 02:11:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c939e3a4d1097af8d3292ad3a41d3caa846f6333b91f2dd22b972bc2d19c5b5`  
		Last Modified: Mon, 13 Jan 2020 13:21:09 GMT  
		Size: 26.7 MB (26690191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63719cdbe7ae254b453dba06fb446f583b503f2a2c15becc83f8c5bc7a705e0`  
		Last Modified: Thu, 16 Jan 2020 01:21:44 GMT  
		Size: 35.4 KB (35366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a861ea6baff71b05cd577478984c3e62cf0177bf74468d0aca551f5fcb891c`  
		Last Modified: Thu, 16 Jan 2020 01:21:44 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651c9d2d6c4f37c56a221259e033e7e2353b698139c2ff950623ca28d64a9837`  
		Last Modified: Thu, 16 Jan 2020 01:21:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e1a6e1ff3c935882f4005a6063541af139f9244769187488ef236e2052ce19`  
		Last Modified: Thu, 16 Jan 2020 01:48:24 GMT  
		Size: 13.3 MB (13323265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193adb2bcec5d5aa437d8a278e43e54ea30b31766030833d2d708455a20d5811`  
		Last Modified: Tue, 28 Jan 2020 00:23:13 GMT  
		Size: 198.1 MB (198075301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c211b413c8c6171e531907145d75543ba85753c7b3c1e9b010ef90f3e9cc18`  
		Last Modified: Tue, 28 Jan 2020 02:19:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a2db801c043eda29f52f2446aeebae22a88b123771c9c0bb2783ab037bd175`  
		Last Modified: Tue, 28 Jan 2020 02:19:29 GMT  
		Size: 12.0 MB (12013865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b8ec4b68abf13d86d612f66244294ee37f63755dabfe7d530479e08899aa76`  
		Last Modified: Tue, 28 Jan 2020 02:19:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk11-adoptopenjdk-hotspot` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:b11a54ade78218b29b2c02416fb75b5a41cef5bc49b299dd3caef4e30e28d260
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231040880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224ed876c1d651385494ddc6fb656093e0fc34dbab5a5903f259c7a60c9e9a76`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Jan 2020 00:59:53 GMT
ADD file:28b9597b09e4e4e5e7dd1ff3e470cdc76c4b8dfe6f37e8e0014be90c0e172630 in / 
# Thu, 16 Jan 2020 00:59:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:59:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:00:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:00:02 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:24:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2020 01:24:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 27 Jan 2020 23:58:18 GMT
ENV JAVA_VERSION=jdk-11.0.6+10
# Mon, 27 Jan 2020 23:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04b77f6754aed68528f39750c5cfd6a439190206aff216aa081d62a0e1a794fa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.6_10.tar.gz';          ;;        armhf)          ESUM='ab5b76203e54fe7a5221535f6f407efa43153de029a746f60af3cffb7cb5080b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.6_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9247f0271744188489b0dd628cab90e76ca1f22fa3bbcdebd9bfc4f140908df5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.6_10.tar.gz';          ;;        s390x)          ESUM='250fc79db2d6c70e655ff319e2db8ca205858bf82c9f30b040bda0c90cd9f583';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.6_10.tar.gz';          ;;        amd64|x86_64)          ESUM='330d19a2eaa07ed02757d7a785a77bab49f5ee710ea03b4ee2fa220ddd0feffc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 27 Jan 2020 23:58:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Jan 2020 23:58:48 GMT
CMD ["jshell"]
# Tue, 28 Jan 2020 00:25:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2020 00:25:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 00:25:40 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jan 2020 00:25:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2020 00:25:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 00:25:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 00:25:43 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 28 Jan 2020 00:25:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 28 Jan 2020 00:25:45 GMT
ENV TOMCAT_VERSION=9.0.30
# Tue, 28 Jan 2020 00:25:46 GMT
ENV TOMCAT_SHA512=40bf428a534816317e5e8732b679e6d73f6ed977aab4ac5e2b9eaf1eb087eaa68a18b0fd3da8c39ca4b96f5b6fd919dec84517abba0d5e797285ade934a92990
# Tue, 28 Jan 2020 00:26:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Tue, 28 Jan 2020 00:26:53 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 28 Jan 2020 00:26:54 GMT
EXPOSE 8080
# Tue, 28 Jan 2020 00:26:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b7971fe48ea2bad85b2c477dc04973a339494497fb370b0d70644d8112e48b98`  
		Last Modified: Mon, 13 Jan 2020 15:33:17 GMT  
		Size: 22.3 MB (22275271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f69e9f176e3248cd66374739e12b3cf3a04e10db7a54c44fd0e966335c47d`  
		Last Modified: Thu, 16 Jan 2020 01:04:22 GMT  
		Size: 35.5 KB (35467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91de5a1686ec92fdd4e9870238004fe56639bc59ce8564133b6a54176d8b4603`  
		Last Modified: Thu, 16 Jan 2020 01:04:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bdbc1afabc79dc485c1e0c118c0dfd22850abb2909cd280cb8b38e6a5609cf`  
		Last Modified: Thu, 16 Jan 2020 01:04:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0515c27c2c577a3caf16273891300cd69728c71d19ccbb398335732f3319667`  
		Last Modified: Thu, 16 Jan 2020 01:26:23 GMT  
		Size: 12.3 MB (12267117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441f6e2d014d33a17faceab7b5d1aaf12dba3f4dc0d6326a95efc142a74e010d`  
		Last Modified: Tue, 28 Jan 2020 00:01:04 GMT  
		Size: 184.5 MB (184535642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93630047995ab6aef23a7da4e9ae01a14b301add8c6dea573b4780f3755efe7e`  
		Last Modified: Tue, 28 Jan 2020 00:28:29 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90e437d4bdbb1c6e6d2c529a575b9300d5f02b835d38cfb74739f8777ca3eb4`  
		Last Modified: Tue, 28 Jan 2020 00:28:34 GMT  
		Size: 11.9 MB (11926005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b77b6168b043750d7655a5c25723c31a409813f86868b8c03cd039dad383aa`  
		Last Modified: Tue, 28 Jan 2020 00:28:28 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jdk11-adoptopenjdk-hotspot` - linux; ppc64le

```console
$ docker pull tomcat@sha256:dc9b7d0c821f69891cc39b91526791f729ff10f1c2f52212bf8bdd2ad145b2c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238901134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc7016f9c2cfeae6e9b20a92b2fb0499b1c50a42b7c463b891e4467da95de12`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Jan 2020 01:16:57 GMT
ADD file:9a1a27f07b5eac878569b1a3279d14f876400a0bbb293be818f5554662ac82e9 in / 
# Thu, 16 Jan 2020 01:17:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:17:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:17:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:17:19 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:43:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2020 01:44:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 00:20:37 GMT
ENV JAVA_VERSION=jdk-11.0.6+10
# Tue, 28 Jan 2020 00:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04b77f6754aed68528f39750c5cfd6a439190206aff216aa081d62a0e1a794fa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.6_10.tar.gz';          ;;        armhf)          ESUM='ab5b76203e54fe7a5221535f6f407efa43153de029a746f60af3cffb7cb5080b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.6_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9247f0271744188489b0dd628cab90e76ca1f22fa3bbcdebd9bfc4f140908df5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.6_10.tar.gz';          ;;        s390x)          ESUM='250fc79db2d6c70e655ff319e2db8ca205858bf82c9f30b040bda0c90cd9f583';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.6_10.tar.gz';          ;;        amd64|x86_64)          ESUM='330d19a2eaa07ed02757d7a785a77bab49f5ee710ea03b4ee2fa220ddd0feffc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 28 Jan 2020 00:21:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 00:21:07 GMT
CMD ["jshell"]
# Tue, 28 Jan 2020 02:22:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2020 02:22:52 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 02:22:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jan 2020 02:22:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2020 02:22:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 02:23:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 02:23:03 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 28 Jan 2020 02:23:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 28 Jan 2020 02:23:07 GMT
ENV TOMCAT_VERSION=9.0.30
# Tue, 28 Jan 2020 02:23:08 GMT
ENV TOMCAT_SHA512=40bf428a534816317e5e8732b679e6d73f6ed977aab4ac5e2b9eaf1eb087eaa68a18b0fd3da8c39ca4b96f5b6fd919dec84517abba0d5e797285ade934a92990
# Tue, 28 Jan 2020 02:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Tue, 28 Jan 2020 02:25:14 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 28 Jan 2020 02:25:15 GMT
EXPOSE 8080
# Tue, 28 Jan 2020 02:25:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5592aacf4ac7489bb730c3e5b1799876d68000b7bbf6e9377ca30e16bff059be`  
		Last Modified: Mon, 13 Jan 2020 15:33:24 GMT  
		Size: 30.4 MB (30400610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f7f270f33afb11e2590bebf54c54fcb052048417bc01b24e357117d730d26a`  
		Last Modified: Thu, 16 Jan 2020 01:19:43 GMT  
		Size: 35.2 KB (35217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242585cde72a9805b281397c8fe3b84a8260c6523a4c290da82e6209845c3690`  
		Last Modified: Thu, 16 Jan 2020 01:19:42 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fc799f2e0e3149ea8c75fb5b36528e147c5e7123e226d9da46be9c3c79f36`  
		Last Modified: Thu, 16 Jan 2020 01:19:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5515694a6e8bfc9e87d0ae9d3b2046662f7a29cfbcb1eaa00c8c3d1a2ba211`  
		Last Modified: Thu, 16 Jan 2020 01:50:01 GMT  
		Size: 14.0 MB (13969109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50f145152957bc359cd9f6feb8449ef0ba5de127e17a88e2741c5b5d9e16031`  
		Last Modified: Tue, 28 Jan 2020 00:27:36 GMT  
		Size: 182.4 MB (182438517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bcb3e06055975a3f4aaa4ecdcd4df0ff354e3fec24a2c6674ececb130c30e2`  
		Last Modified: Tue, 28 Jan 2020 02:47:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c697df23d4eb5692a9f8aaf0778fc026ee8ad84a796190a81db580f29e13f3b`  
		Last Modified: Tue, 28 Jan 2020 02:47:24 GMT  
		Size: 12.1 MB (12056301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036a7ff1f2bda5a53415994277ccfd641bd5f4aebc0a94f9e8b8b185367a486c`  
		Last Modified: Tue, 28 Jan 2020 02:47:21 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
