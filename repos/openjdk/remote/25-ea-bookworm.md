## `openjdk:25-ea-bookworm`

```console
$ docker pull openjdk@sha256:f78f5781b93fb7a09b80fb7d53c530a58b07bac8f2c9a4c43601cc4400875980
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:27a33262b48c3feceae6a88fe77769d13bf2511bba735e044738c3f425c3e8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365776084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c25ec28002ecb77933a605b3986e78d3a3ffa4203cbb535235d8585062979`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4334440d2a26f55a3ad5157113e2bee94b85c7845dd6baf3b2d14d8d85148393`  
		Last Modified: Tue, 04 Mar 2025 21:57:08 GMT  
		Size: 16.9 MB (16943107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e21155f02eb47323aa01de4e9ca5f2b07a19229ce064df03afe9d29e92bab0`  
		Last Modified: Tue, 04 Mar 2025 21:57:12 GMT  
		Size: 211.9 MB (211904132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0541b13783ac1c8612c7ac13ff4a46d8daab6fbceaeab590c5a15c9c71998154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8454259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf2c7c1cc6ad32a5e1d9f93505693aab76f7b6a9c09d827ebc260c1035e2359`

```dockerfile
```

-	Layers:
	-	`sha256:4be89bbf97af9a5628dff13c5378206f35eaf8aca84a7421cccd56d659c04b7b`  
		Last Modified: Tue, 04 Mar 2025 21:57:08 GMT  
		Size: 8.4 MB (8435641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ffe55db3fce3b46ccb1968a623b7c001a7bd40e7592053ec15a5edec152f9e9`  
		Last Modified: Tue, 04 Mar 2025 21:57:08 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7c24c02bf4e1ab366c88e114041cb24a589a327529cb6f7a8c6eebd433aa70bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.8 MB (363822011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d505dd89fbc1414731dfb2d2662c873903336eb9b4350254b4d4bd65116f3841`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a4fe2a7c014ec19a707e79af512a2c8832c8c0001e470f4cfefa3f85e4ce1e`  
		Last Modified: Tue, 04 Mar 2025 22:01:28 GMT  
		Size: 17.7 MB (17726793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c7851d0771fac812cfeedb2a587bdd203fa9e4d2b82978daabbd778144c7d2`  
		Last Modified: Tue, 04 Mar 2025 22:01:32 GMT  
		Size: 209.8 MB (209834555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:121195bc6dffd8184ccc37299cfb2435c667937a32bb3b9db7dfd37950d9e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8591267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a12131b46dbc0beb5677420f615f928ed77b2060540744281dddaa6e3b2ea3`

```dockerfile
```

-	Layers:
	-	`sha256:04912dd1ca67f7f6fec4082fb73222203ad54d92403ede945e88588147b607e2`  
		Last Modified: Tue, 04 Mar 2025 22:01:27 GMT  
		Size: 8.6 MB (8572509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ceeb0a518cf40bea58dcbb9d6fbd1fe551bf2c22dc130f04641a7fa24641fc2`  
		Last Modified: Tue, 04 Mar 2025 22:01:26 GMT  
		Size: 18.8 KB (18758 bytes)  
		MIME: application/vnd.in-toto+json
