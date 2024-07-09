## `openjdk:24-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:31b73db2c5511db66625ad200d5a258a517c49bb320b5767088f2d0d293ee8d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:065099b6ab04f717a9d339c40b920842f69736465e279dbfd396af93609259ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244696457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07deafaa1d28b5c0be80dd72194e6ccf73e7da6ba96125b8847479906fc9827c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af435c41a570899cfce7841f72d05e51f85b51aef96015a4773179fd62d335`  
		Last Modified: Mon, 08 Jul 2024 20:56:50 GMT  
		Size: 4.0 MB (4016822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0332315e8c7a26263cc79dc210a3c9039c1730bb789b3c7e620af7f553ee413`  
		Last Modified: Mon, 08 Jul 2024 20:56:53 GMT  
		Size: 211.6 MB (211553357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:111d6b97eb1aed279f8669a7975e7400f73e6d0cb2888b8c559626ef2b2c8909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d30166a14a7b82cd330720bda90163060e591ebefb5d313d4026c6b27c11be5`

```dockerfile
```

-	Layers:
	-	`sha256:67a3ae5de7410533cade6a2bdfe8607f9dd6ae81e33b6c3877d5a26a3f37b681`  
		Last Modified: Mon, 08 Jul 2024 20:56:50 GMT  
		Size: 2.3 MB (2346333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98cff63f7b53d9bff404aae966f2ac70d3c193f7141719d0d47a1c338094e382`  
		Last Modified: Mon, 08 Jul 2024 20:56:50 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:837f9c53fc7dae21bb7ca36c023954ac601a94ae00265abcd107e56ee1691645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242415962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f7f08d75a3c7270aea62210096c4c07116bae4a274c4960008490529e5374`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2149aac5fc65027f104f3e2bd5589eb7f7ac9175a7e33784da9a9f11041f05e8`  
		Last Modified: Mon, 08 Jul 2024 21:00:06 GMT  
		Size: 3.8 MB (3829946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3179b4a1cbf2c2d850cc0017963e88abb717e8f193aca35f4fafab1b0d773`  
		Last Modified: Mon, 08 Jul 2024 21:00:10 GMT  
		Size: 209.4 MB (209429453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e25c2ed1f2d00ced1fb177020473287f9f6dbbc41816cf28571db4df6304c5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc63dfca6b0c0ffadd29e354bb9d54a66b98d276d498a0616d8735748a042778`

```dockerfile
```

-	Layers:
	-	`sha256:782c5eda1209bbde5a619d7e249ea6e9ce454c76168034bbf6c5c99d09397dd2`  
		Last Modified: Mon, 08 Jul 2024 21:00:05 GMT  
		Size: 2.3 MB (2346687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8646ed8282c04584b420130b613afb1dfa7543647e0ce1db6ba9129356f3cd4a`  
		Last Modified: Mon, 08 Jul 2024 21:00:05 GMT  
		Size: 19.6 KB (19618 bytes)  
		MIME: application/vnd.in-toto+json
