## `openjdk:28-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:0558d35eb8e7b329aa4efef6dc4d89cca1f8ee2e8290e9c368cbe912ef1d9f5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:306148491aaf3aba212fa1b32762697946b353e7631b28dfe92b8d1bb18a1579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259461297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79074e51b02509607dabb68c1d9e890f52e117a79513411087d09366cc8ef0eb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 00:48:00 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:48:00 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:48:00 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 00:48:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:48:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8cf0ccb772a2d464f41bcd735a899402b60367bbce1d4f9a4b10a511d7d33a`  
		Last Modified: Thu, 11 Jun 2026 00:48:19 GMT  
		Size: 4.0 MB (4032907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99cb8f2f989cb2906c701b2f66d17c8d7c9ceb9eaa27747380f4ba186139141`  
		Last Modified: Thu, 11 Jun 2026 00:48:23 GMT  
		Size: 227.2 MB (227190766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c35ef6e64280f2ac96a7c6ceb1abce8d4f8d884aa54aac168d2a8753390e961b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad523c863309b7988723aeaa8a64ae6e8f2b64b4afea93a2c8594f93147f6453`

```dockerfile
```

-	Layers:
	-	`sha256:8e3b7e37ad7374aec8280a8285ffc2c2c0a81bad6b2653dd96df0a5f1d809973`  
		Last Modified: Thu, 11 Jun 2026 00:48:19 GMT  
		Size: 2.6 MB (2647278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc96d21717bd979bedcd04d63d799a681a0d47e8730c53bfb628bd66e20f2d3`  
		Last Modified: Thu, 11 Jun 2026 00:48:19 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:34ae631e2ea8ac927e1b7869d1bd22e9794eb5cd69a44e4b009e7c2d11b40926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257134096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9256ac6a0631434296e1f9835bf677bb7614da38630eb0201f0ddd1aeaa30964`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:49:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:49:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 00:49:27 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:49:27 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:49:27 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 00:49:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:49:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d3eace6841e220dac6694b175fbf9173edd32ca606fe50bc05dd2c94b2e80d`  
		Last Modified: Thu, 11 Jun 2026 00:49:48 GMT  
		Size: 3.9 MB (3852818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6234f0541d9c1c2f7dce08736c5a26c58e41ceb664f5921698463434586d784b`  
		Last Modified: Thu, 11 Jun 2026 00:49:53 GMT  
		Size: 225.2 MB (225158971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b37d040ab5168171b6c9b94eb47fe8d1825f7952312d2837892b5de482d269af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e0c1bb7e75de8f57b8683e50c392e3ac6954b645210ac0cbc4cf231ba0a60`

```dockerfile
```

-	Layers:
	-	`sha256:f5ebfbceb9f808a99b2b4c7c8ac5a6d28b71ff3ffa49715eceefec750d10789e`  
		Last Modified: Thu, 11 Jun 2026 00:49:48 GMT  
		Size: 2.6 MB (2646912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ceaeb5983383f12ce3ed12f8809bcc7ab257d619eb01de46f5a1cde05dab2`  
		Last Modified: Thu, 11 Jun 2026 00:49:48 GMT  
		Size: 17.0 KB (16975 bytes)  
		MIME: application/vnd.in-toto+json
