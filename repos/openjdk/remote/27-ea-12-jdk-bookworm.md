## `openjdk:27-ea-12-jdk-bookworm`

```console
$ docker pull openjdk@sha256:8ba7b2b3a7dc264ff169e5b30a98e7df6efa4c3155283e4a6dd1e649503d234e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-12-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:548267253a14443fcefa9fe94176501cb810993fd9739b0429c320e9a839338d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.4 MB (382400778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26239805c538f5c5aa4e829af51447c5be4d1b7b619e40ded29b1520c76a18dd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:42:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:42:14 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:42:14 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:42:14 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:42:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:42:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbd438a93fcaec5915727934d4d2ef7d683a9403498f8d234ed20ea821e5f44`  
		Last Modified: Sat, 07 Mar 2026 00:42:39 GMT  
		Size: 16.9 MB (16945173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7d0b2290f77870c243ff74d70c6f5cbbd072534920ae33d4192d6c29ffb1d4`  
		Last Modified: Sat, 07 Mar 2026 00:42:43 GMT  
		Size: 228.5 MB (228532525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-12-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bda945f7d3b527f455ef1f342ec5415538dc243164a5f006705162cd51fb3ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936008fabe429d24bacae835405d4aa0279f060a2d58b0fc56274c697b1efc7a`

```dockerfile
```

-	Layers:
	-	`sha256:8480c50b4dedcf1c864ce332c6d60c3ae1798dfe10d31e87f728f6380649c4dd`  
		Last Modified: Sat, 07 Mar 2026 00:42:39 GMT  
		Size: 8.7 MB (8668887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:576b1b6358bae42744eb280336a86cee5f85c3c20d4e00456b6605084fefa346`  
		Last Modified: Sat, 07 Mar 2026 00:42:38 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-12-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:74e804010373442ffcac8a0eac04dc0945e8585cc28d0b3396e07bf895ba2eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46689472df172caa32a3022202d993239e5916aade46ac0e16647598f5f1446b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:43:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:43:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:43:24 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:43:24 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:43:24 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:43:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:43:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a3c74c2906b310d932519e6990118ae0e6fda6827fbedad09826309e788bf3`  
		Last Modified: Sat, 07 Mar 2026 00:43:50 GMT  
		Size: 17.7 MB (17729091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf48348b9523639dcb22c7767d38b4e3d7e9b84374e77b0fde29509b0f5790c3`  
		Last Modified: Sat, 07 Mar 2026 00:43:54 GMT  
		Size: 226.5 MB (226484626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-12-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9e8c303d26aa7ef1cae90bec7956be8c7d8b3c1cb874ad9e14a6351d94bda677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89548fe54e223f9ba86f4a034020e3f07e3a7576d427bad98ed4a8c6e28050db`

```dockerfile
```

-	Layers:
	-	`sha256:5eb9599bbc572b830163271e0d56ebe90a9b2e91f3f5481bcba2affd9007ece6`  
		Last Modified: Sat, 07 Mar 2026 00:43:49 GMT  
		Size: 8.8 MB (8805732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7015e2e0ffc9a0f312dc46d38fcbcc23ff62b167bd29e8b1adbb9ca36ed7d9f6`  
		Last Modified: Sat, 07 Mar 2026 00:43:49 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
