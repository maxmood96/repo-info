## `openjdk:27-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:f7357760e69e625bf0f86f63805656dbe7b2c27cb6b6cdadd1f5a77969f9daee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:946ac4b6709d4c4e8a9f0224753ebcbc4ac45a9e3d9ee2591b9a488d3b100682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (380962361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e16d254cc270e0f538b7b538c54c682c9edf025bc8dbc10d6aaaf119bea1d6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Jun 2026 23:32:06 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:06 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:06 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:32:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2cb8ff4697303fc967dd827b124425d5a02bfc5f6e8307943109c3987e1180`  
		Last Modified: Tue, 16 Jun 2026 23:32:31 GMT  
		Size: 16.9 MB (16946416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da15e40f7ceaf1fa79095a9d1ca18b9c013358b2d22719b668e424d3db2d42b2`  
		Last Modified: Tue, 16 Jun 2026 23:32:36 GMT  
		Size: 227.1 MB (227065787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cd122466862f69edcfd619700eaed8f6e5218dc003ad5afe7854680926629ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a0ea5d392cf28ae2cbfe712fb1efce0d651a256ce7d53489f3d981864a5ee5`

```dockerfile
```

-	Layers:
	-	`sha256:fbb92d93ad3db3baef4bc77a9aaf8bff2de14200873afdd5d149947d12df991c`  
		Last Modified: Tue, 16 Jun 2026 23:32:31 GMT  
		Size: 8.7 MB (8666374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1bb55c74681375a19d52a61deb3608902b22cbefae57dfbe591573570af6ad`  
		Last Modified: Tue, 16 Jun 2026 23:32:30 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ff76317715a606009b98bde5b3df770b2ca03c3ee0c5e6b543e29fc947457b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379263956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e21c588f3056b08f120be702fb6e8f0c4fee8e2769f2578e26dadbae4121ec`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:31:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Jun 2026 23:31:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:31:58 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:31:58 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:31:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:31:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d38e936f9f598ca9752c72cb19c5dd4904dce9d07222b78bf66088f3b7945`  
		Last Modified: Tue, 16 Jun 2026 23:32:24 GMT  
		Size: 17.7 MB (17730232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c636ed27416ac5d29f615014888e727d67dcab91e5bed68ea4cf5fffed2d5f`  
		Last Modified: Tue, 16 Jun 2026 23:32:30 GMT  
		Size: 225.0 MB (225043534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c8fa937b5f0795ae7f8a03a9b378930c18f48351353cdd3920192e090059147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8de5e27e70a4c85c71986eceacef9cd96e0c511c873a1c0089e7821dc478e1`

```dockerfile
```

-	Layers:
	-	`sha256:3269a460fce744c04f7a8194e018f0c506068ca65e995ae8686e7e2bb524aba5`  
		Last Modified: Tue, 16 Jun 2026 23:32:24 GMT  
		Size: 8.8 MB (8803219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c4bc8b030db2653344eb427ddb385f50e09f29abc3b0c522e7af3c7ea860de`  
		Last Modified: Tue, 16 Jun 2026 23:32:23 GMT  
		Size: 18.1 KB (18057 bytes)  
		MIME: application/vnd.in-toto+json
