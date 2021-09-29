## `tomcat:8-jre8-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:a1fe33207859d698d59b5cceb9be1961fb4264511f4007fcad30ac817cc7976c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre8-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:a28c5d11dcd382df472252e9aff8d526ab36531e15c7f9215fc76d145bea2fda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83660303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ff7843b4de14359179d53e9adfa793eb1a4c831b8fb7354666ead09f628380`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:26:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 28 Sep 2021 09:26:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 28 Sep 2021 09:26:14 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 09:26:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:26:14 GMT
ENV JAVA_VERSION=8u302
# Tue, 28 Sep 2021 09:28:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 29 Sep 2021 11:30:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Sep 2021 11:30:44 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 11:30:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Sep 2021 11:30:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Sep 2021 11:30:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 11:30:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 12:09:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 29 Sep 2021 12:09:28 GMT
ENV TOMCAT_MAJOR=8
# Wed, 29 Sep 2021 12:09:28 GMT
ENV TOMCAT_VERSION=8.5.71
# Wed, 29 Sep 2021 12:09:29 GMT
ENV TOMCAT_SHA512=292a3f856b0a8c1d11fd1ba252cabd94794201cda4f951dd0522764449bed90f2f43a4a667cd6d28ce13c3b2096736978d9df91709c168ba7133c51544446433
# Wed, 29 Sep 2021 12:09:29 GMT
COPY dir:f2d1d04696eb919f562bfad812b5a5f05ca5358b2c5d5ab1f7d2db539cd5cb79 in /usr/local/tomcat 
# Wed, 29 Sep 2021 12:09:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 Sep 2021 12:09:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 29 Sep 2021 12:09:35 GMT
EXPOSE 8080
# Wed, 29 Sep 2021 12:09:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49190af1e362ddee7f9a92cbf321a9b1444ccbc631019b5ebcc582e4ef2ec3e9`  
		Last Modified: Tue, 28 Sep 2021 09:35:40 GMT  
		Size: 3.3 MB (3269563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caa64be9879d0d50af1a8f3a69f36761cecf8580fd759f8a7ec5462ad395f7b`  
		Last Modified: Tue, 28 Sep 2021 09:48:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0105a479fc8565cbb656349ab85bb55074c8ea54a8c6c0a2b554151623d33f6d`  
		Last Modified: Tue, 28 Sep 2021 09:49:44 GMT  
		Size: 41.6 MB (41641158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65e7fd727e72062f57306147d53ad36d0d29edb46438853e6788d4f160c6a5c`  
		Last Modified: Wed, 29 Sep 2021 12:35:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f645307d09a76c611c054cba231aeddad262c70ff9770e95299104c11c8dcbab`  
		Last Modified: Wed, 29 Sep 2021 12:52:37 GMT  
		Size: 11.2 MB (11215403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630ee00f6ef4ef674d8f863d550cf73ab5a36f38f6b0316c1b9ca17f8691cbdf`  
		Last Modified: Wed, 29 Sep 2021 12:52:35 GMT  
		Size: 387.7 KB (387672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc1c04de7f3d207a55f63d168564f00459daaadc812410bd1f8b4a4218bd20c`  
		Last Modified: Wed, 29 Sep 2021 12:52:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:ff35899da85279f555e99b598b23c98ac5972d03549bfd3f4c44ae163a77b192
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81550811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb2b0d0ad35e0fbb2a89799a2f11eb168a4e4cece9e5a9d570df9be0c6794d3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 05:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 05:53:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 28 Sep 2021 05:53:27 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 28 Sep 2021 05:53:28 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 05:53:28 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 05:53:28 GMT
ENV JAVA_VERSION=8u302
# Tue, 28 Sep 2021 05:55:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 29 Sep 2021 04:13:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Sep 2021 04:13:03 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 04:13:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Sep 2021 04:13:03 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Sep 2021 04:13:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 04:13:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 04:52:20 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 29 Sep 2021 04:52:20 GMT
ENV TOMCAT_MAJOR=8
# Wed, 29 Sep 2021 04:52:20 GMT
ENV TOMCAT_VERSION=8.5.71
# Wed, 29 Sep 2021 04:52:20 GMT
ENV TOMCAT_SHA512=292a3f856b0a8c1d11fd1ba252cabd94794201cda4f951dd0522764449bed90f2f43a4a667cd6d28ce13c3b2096736978d9df91709c168ba7133c51544446433
# Wed, 29 Sep 2021 04:52:21 GMT
COPY dir:197ebbdfaf11358be173556294d12db50b5844c1d10e635c0f2b1682e4865371 in /usr/local/tomcat 
# Wed, 29 Sep 2021 04:52:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 Sep 2021 04:52:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 29 Sep 2021 04:52:27 GMT
EXPOSE 8080
# Wed, 29 Sep 2021 04:52:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f844c3c3d3fdf0c62ff77a82ed24a2a010ad55e3206255c75275457b868825`  
		Last Modified: Tue, 28 Sep 2021 06:06:17 GMT  
		Size: 3.1 MB (3119080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380370971ba630eaa1af5cf1c1a0a4242fa5dfb43a37416f70fb8d358c9f6f44`  
		Last Modified: Tue, 28 Sep 2021 06:20:06 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8479bcf6b78fd1653fbeb2a37bd9f164e1dc717e5e1c76afbdff5f13bc020ba9`  
		Last Modified: Tue, 28 Sep 2021 06:21:42 GMT  
		Size: 40.9 MB (40898531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a678bec6f82cfda1224f20378bba7257909a6d4c8a9a24fa6fb910e6689bd`  
		Last Modified: Wed, 29 Sep 2021 05:35:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdadbda183571efaf784339352865c39e80360e50cf710f2175136fb216e132`  
		Last Modified: Wed, 29 Sep 2021 05:56:50 GMT  
		Size: 11.2 MB (11231487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675cdb59adb989e87635721ef5e8a061600ec0c4a0a249a75d42f9d98b6cbade`  
		Last Modified: Wed, 29 Sep 2021 05:56:49 GMT  
		Size: 386.2 KB (386163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bdc29bb1ba42e5ee070925bf7a0d53cc5aa0797f4438ab4ea71d5ba42b3eca`  
		Last Modified: Wed, 29 Sep 2021 05:56:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
