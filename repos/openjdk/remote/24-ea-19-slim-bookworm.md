## `openjdk:24-ea-19-slim-bookworm`

```console
$ docker pull openjdk@sha256:3372dde349384a0465d6886de834704478a52ef474240b86426017f17235f9b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-19-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:88648c54cf493330dc30042086a1a14e1d650e417fba333f570cd29455dfb99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245555642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fded484bc60a9c729015f7a67d27ceba9c4d5ad2df75059f089bd4f2348cbac`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 00:48:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa61aadbde79f069913e7c31c43e9b4bd3e62858f655052c9603075aeccbd11e`  
		Last Modified: Thu, 17 Oct 2024 01:31:03 GMT  
		Size: 4.0 MB (4018054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b0e0d2b447f137745c4dbb24ce17ef24f539e856413f8039a737eb0840780c`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 212.4 MB (212411299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-19-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:12e1b0222e08544a3f2f034cac91d98e7e0beac5b865ed4a10b8dd64590cf28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dce59ec58fe08d85f94a33ff9b7cdc65ecba9c4fbce728cd6cabbf9674b51c`

```dockerfile
```

-	Layers:
	-	`sha256:9e53609e82d0dc7e7f1b5c7bf6515519303496b01f54988240745619e815d9f9`  
		Last Modified: Thu, 17 Oct 2024 01:31:03 GMT  
		Size: 2.5 MB (2503891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628cfcad5bf56bdabf9f896cf11c10831debf66ab48a161f70588c808cf1d4cb`  
		Last Modified: Thu, 17 Oct 2024 01:31:02 GMT  
		Size: 19.3 KB (19267 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-19-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:25ff88d688ed43a0f1984b6f01e57f1cb52bfdccc0c387fd54abe5d11ebf960f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243289873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fa7758b6d72566decc724b15667f47bfcf6722fe8192a57a19d087224cb9df`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8454d71dbc1964684fb53644ff5a3b1f9765577cc1ef3442b1a933d2b8014a3f`  
		Last Modified: Fri, 11 Oct 2024 19:27:55 GMT  
		Size: 3.8 MB (3833460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7241d41a86493a5695fab4c81f20fb8d96d2a277cb86668e9fffb508133401`  
		Last Modified: Fri, 11 Oct 2024 19:28:00 GMT  
		Size: 210.3 MB (210300044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-19-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:263dd00db68e03f7c32c654a478fd64a150509bd5a750b4a7a1ae2a84b353bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2522472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58d9cf40bd0d14fde6fe81ff04d8859e3c7501a65fd3e52180dbb65c861ba39`

```dockerfile
```

-	Layers:
	-	`sha256:be47445925eec3fe0764ac6245f84246e7927bef947bb5a51166e74c3c3a4634`  
		Last Modified: Fri, 11 Oct 2024 19:27:55 GMT  
		Size: 2.5 MB (2502996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bc1ca5269ade115f8f10f2abae1f539b14c989467bafd0606e27f12786f49e`  
		Last Modified: Fri, 11 Oct 2024 19:27:55 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json
