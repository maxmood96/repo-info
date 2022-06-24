## `tomcat:jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:6a5ea9678ade16ef62574602eb4eacf83b4d185a32cfa2cadc63aaae2873521a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:c2a7b419e08f6751272d8fc00ac967aeadb157c03fb24e788d9db98d3841feb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90852773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0347d689318b0cedc3c8ff5b333ed46bf0786d12f8d4a8c262bc74c479e790`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:58:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Jun 2022 04:58:46 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 04:58:47 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:58:47 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:58:47 GMT
ENV JAVA_VERSION=11.0.15
# Thu, 23 Jun 2022 05:00:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 23 Jun 2022 22:40:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:40:56 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:40:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:40:56 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:40:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:40:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:40:57 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 23 Jun 2022 22:40:57 GMT
ENV TOMCAT_MAJOR=10
# Thu, 23 Jun 2022 22:43:52 GMT
ENV TOMCAT_VERSION=10.0.22
# Thu, 23 Jun 2022 22:43:53 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Thu, 23 Jun 2022 22:43:53 GMT
COPY dir:183815ef836f4ba84c1c89dd5472bdc8bb16ec8a52fe90fd799dc4ec63e7f398 in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:43:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:43:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:43:58 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:43:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420fab7e4cce528d853465a0775f91b15783a53a42b906820fb3f70f0f731667`  
		Last Modified: Thu, 23 Jun 2022 05:08:38 GMT  
		Size: 3.3 MB (3273402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87982e55af1e38a145b95a51908b42ac808e26e2da7071790966ee117f15af29`  
		Last Modified: Thu, 23 Jun 2022 05:17:47 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383ae62e0c6f9a5c1c7f1c59e6407915c889ab899e09cd1b871574813636cf0a`  
		Last Modified: Thu, 23 Jun 2022 05:19:32 GMT  
		Size: 47.5 MB (47481947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194a59b00acfc35ec491e95c5f2739a3008952556b7e4e83c443910a7b6e6e15`  
		Last Modified: Thu, 23 Jun 2022 23:09:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f03eaf6f85a6107e59b3c72d8fafc1d3e109b9c93645ac903d49abda872ef9e`  
		Last Modified: Thu, 23 Jun 2022 23:12:28 GMT  
		Size: 12.6 MB (12569158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f3c693abfc9e48de70ee2bd38be0cde7346c6e21e26286c2082f5d8d7d8b97`  
		Last Modified: Thu, 23 Jun 2022 23:12:27 GMT  
		Size: 387.7 KB (387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe01ff2615596f45971e7efae0c37e0892dfda358bad677c3ebbf1e13df1e63e`  
		Last Modified: Thu, 23 Jun 2022 23:12:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:51fbee6ea9581f4c3bceffc2c1920a1ce88fb393a8aa6ae8af5c93e1d5aa6a2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88362087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb549a114d2ba88c9c53a6176e4df461439eac3d53e04e3e682b3ac54ea7f24c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:41:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 May 2022 01:41:33 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 01:41:34 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 01:41:35 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 01:41:36 GMT
ENV JAVA_VERSION=11.0.15
# Sat, 28 May 2022 01:42:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 28 May 2022 20:07:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 20:07:39 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 20:07:40 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 20:07:41 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 20:07:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:07:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:07:44 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 28 May 2022 20:07:45 GMT
ENV TOMCAT_MAJOR=10
# Mon, 13 Jun 2022 21:04:35 GMT
ENV TOMCAT_VERSION=10.0.22
# Mon, 13 Jun 2022 21:04:36 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Mon, 13 Jun 2022 21:04:38 GMT
COPY dir:3a64bf39c40a341a0c7c4c6b3bd52f9f3dbbe020366c200d3747feefaa3a0c15 in /usr/local/tomcat 
# Mon, 13 Jun 2022 21:04:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Jun 2022 21:04:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Jun 2022 21:04:44 GMT
EXPOSE 8080
# Mon, 13 Jun 2022 21:04:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fd49b058d9314bede6d26981edcf8cfa5f28eebce620889117829184769a12`  
		Last Modified: Sat, 28 May 2022 01:56:24 GMT  
		Size: 3.1 MB (3126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b5f0afe8e37879f32b03e81e1481bd0e176508e804c8d01ba77c54adb5223e`  
		Last Modified: Sat, 28 May 2022 02:01:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecaffdeb34182f53c1f89178a5f2d68e282dd8383e6193da8e7f44ba48c11ed`  
		Last Modified: Sat, 28 May 2022 02:02:38 GMT  
		Size: 46.6 MB (46566981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc99920d6059046b245afdf98264e9b1245d63f4282e6750b0fe7cdc789e8be8`  
		Last Modified: Sat, 28 May 2022 20:56:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9954342d45205019e05ce8dbeabc407139959749848184707773b8ec96c421b2`  
		Last Modified: Mon, 13 Jun 2022 21:48:15 GMT  
		Size: 12.6 MB (12581028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed2c3f15fec08f387f23f824b1a812c3b917c08744cfa4196544a8ab7cd1cfb`  
		Last Modified: Mon, 13 Jun 2022 21:48:14 GMT  
		Size: 173.7 KB (173673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
