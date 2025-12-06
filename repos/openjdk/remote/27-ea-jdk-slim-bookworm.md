## `openjdk:27-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:e1e1cad6b22ad532010c63fd2cab253195c0f513411d4604fa46baf950c30890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9f88ea065c2f62d891a43c649f0cb198c8300a4a7dbb52715c5ee54a5757e9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260310607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0eaaba1bbecccc8189948cbb0acc3e8a2e86e98545f1934bcedf5dd4527dbc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Sat, 06 Dec 2025 00:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:35:40 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:40 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:40 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:35:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016fc1c0a705635d684dec60fb78aaa95805422f0920697f9c0045027d5b67eb`  
		Last Modified: Sat, 06 Dec 2025 00:36:14 GMT  
		Size: 4.0 MB (4027328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaef671d76b63adc502fbb0c5941a51039a8a35794015d218c992b893efc3852`  
		Last Modified: Sat, 06 Dec 2025 00:36:20 GMT  
		Size: 228.1 MB (228054830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:91a74d7b75e321b61dd5aac6f5f56c90975b14f5890d879e6b21ab9c7f8d865e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a13abd0ac9cee9ea22916075e7e04dfd73c69b26ae67b09ce6efd0c3b2955a5`

```dockerfile
```

-	Layers:
	-	`sha256:71c1ac2fd4b938d63454aee5bf2ffb7416e975c51335de6c57d95d2281465a90`  
		Last Modified: Sat, 06 Dec 2025 01:26:48 GMT  
		Size: 2.6 MB (2649777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b15bc44f7260e92393f20336893d93999a88f89f49cce6f081fdfc86624686f`  
		Last Modified: Sat, 06 Dec 2025 01:26:49 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e43bb3bd1161b8f65c670ca4247bdf3670354b3167b55a8990c0ba205d25aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257913236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8139bd11c1c8fe575fe6caf9cb57587c75d1d846774bbce5d5bbea0d88eda9c1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Sat, 06 Dec 2025 00:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:35:23 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:23 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:23 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:35:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92988c070d1ad11457c4a8a206087a6509154c5e1a17eede57b560663a6c862b`  
		Last Modified: Sat, 06 Dec 2025 00:35:56 GMT  
		Size: 3.9 MB (3851383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bfb5bb2d4e06edc16312f24fc4cd16e2fc0cea3c56ad076f39bc21c65bf93a`  
		Last Modified: Sat, 06 Dec 2025 00:37:50 GMT  
		Size: 226.0 MB (225959646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c3457f5d2d61bbcd2f3fbc7f0b3dfa51ea905d2ad710773f1fc1882ce9ab0d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acbc574b26cda97b8e46c92d82fa93bb2d9faad777d8c2a7dff0da161ff3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:cd6377d59241872b683447550031cdb2e4b02de313adca46d434af79b668980f`  
		Last Modified: Sat, 06 Dec 2025 01:26:53 GMT  
		Size: 2.6 MB (2649411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8c0f642e84d0a6eeddf37cb527fff8461b71f249c50335a56380b4199f32a2`  
		Last Modified: Sat, 06 Dec 2025 01:26:54 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.in-toto+json
