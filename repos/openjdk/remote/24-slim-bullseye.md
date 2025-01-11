## `openjdk:24-slim-bullseye`

```console
$ docker pull openjdk@sha256:b8a205f11a65aef0c37abed39fe8cd02a35a89e9bd2e075cf7e7c93165c2cb81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:19206c47787dfec3bfe29dc02ecd94048b9b884e38f62b854927f0d0c3095043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244546322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b654bfadb629792143f9feea70b65f91408d73fd9cd65a85dbedd4a8d4f65`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436ae4a25f25c6ce039e051eb1a8dd30964ccd98034db583de5f4b52238526`  
		Last Modified: Sat, 11 Jan 2025 02:29:48 GMT  
		Size: 1.4 MB (1377268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d8eb3ad7a20aca54cdbc583fef617f4d29a97ee4c4803cc5633cae512fed3`  
		Last Modified: Sat, 11 Jan 2025 02:29:53 GMT  
		Size: 212.9 MB (212916411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:79b52cde61d3e39f78d28efea0bbd7212baa320b5bef396181b4e8aad2076fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91f672cef5f83f458697feef16a00922fe82da6b05e7315dc0a31ce0f3a6a16`

```dockerfile
```

-	Layers:
	-	`sha256:8a632ee189b062a1738adfd792a95c7c8b5adc31f7cffe0baea60d866bdec9e1`  
		Last Modified: Sat, 11 Jan 2025 02:29:48 GMT  
		Size: 2.8 MB (2827922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12847a0e68ebfba1dd26b2713574e21438823f1f9af698ff43e11227ea22c926`  
		Last Modified: Sat, 11 Jan 2025 02:29:48 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b3f0653ce7753b46369c7b15245715aaefe0e2945a4115c079bb6d4794b221d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240978820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb185122b0652ae7b3aeb84b16b04defa8858a5227127dbd00aeaf80c9359ac1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5c8f0fb84ba0a041b6e177e7fb8753ae3d2ea2da20fd79be83781ec01d2ac`  
		Last Modified: Sat, 11 Jan 2025 03:19:47 GMT  
		Size: 1.4 MB (1361268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea270eb3b6cce37c5684d29a226a45e20098890c3a8f5b264c8f4e25fed61d4d`  
		Last Modified: Sat, 11 Jan 2025 03:25:07 GMT  
		Size: 210.9 MB (210872699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2cd75b38ddd8da297862905cd510f4331e2b14669bdec3191840157a819bbec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4cf6390ab9eda6b68853764eba1f1825da22127cf454773e90ca16ec17317f`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f72dc76238d834c655a4961ccd47d8253f9d7036159a3e6587f8f85041fa5`  
		Last Modified: Sat, 11 Jan 2025 03:25:02 GMT  
		Size: 2.8 MB (2827574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157cd7dcefff900e1f7d72b87e9b80c369836861f7c62b058daa4de706f02a6c`  
		Last Modified: Sat, 11 Jan 2025 03:25:02 GMT  
		Size: 17.7 KB (17712 bytes)  
		MIME: application/vnd.in-toto+json
