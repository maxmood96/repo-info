## `openjdk:24-jdk-slim`

```console
$ docker pull openjdk@sha256:5e5da7422ab58d66da3c0befee74cc632a5e759fa3fc487fa3ff243519e03cb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:35963eed35cae69a86d347e8c1c34637336c6d0705761dab214f70e5d4c812dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (244985608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7474a47ce0fbb8af1fce3f9e4953597b54bd7cbcfe35ddc18527acc3739608`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc215dc5072dd48add0608293a39a74271f23f24327ef05642734d11646b13e`  
		Last Modified: Mon, 06 Jan 2025 20:28:11 GMT  
		Size: 3.8 MB (3824659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a42a5e131732afe9e57d8356a5db015e2e2eef75312e46d6ff2a0af2f1853`  
		Last Modified: Mon, 06 Jan 2025 20:28:16 GMT  
		Size: 212.9 MB (212929368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:97a986f30d7ab4175fb457938e11f9ec2fc34660aa1096a7acbc33ff24aee533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970f552497d2048b97209e5ed7961ffbfb4bd83c83b75329f0b1332e4c14858e`

```dockerfile
```

-	Layers:
	-	`sha256:d61e4b9b7dfff83fcf9f475786fd31fe3d3362ab4f3b91d2a0783d0a36cdbbd4`  
		Last Modified: Mon, 06 Jan 2025 20:28:11 GMT  
		Size: 2.5 MB (2534519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a1c53303157419626cab3ad0caaed6191676f08819c3f73338aaa2666d3a7e`  
		Last Modified: Mon, 06 Jan 2025 20:28:11 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:93a85f1f0a2b059417ca4677c3d27fe462a3179102a5bd965e65d912435b26c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242579398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3719486df9530bd18097b69001c820c48aae0ca6f8a393a33876acb45f7db1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d3f765461c27f0e2a8b9395e935b925cdf54757357b1c5c319321b27758c55`  
		Last Modified: Wed, 25 Dec 2024 02:33:37 GMT  
		Size: 3.6 MB (3639386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13919d082b4f61d4d21a5f6fcbfec530eb8feb6226eed3b7098eb06897a42be6`  
		Size: 210.9 MB (210881289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:67df43e70e10cf22446ba16b011c1046cd8853c97b56e30a8af89d9857c0ab81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc384495a43d2077a1b5c48c79171de67634a45f8051899e0ac49b993dfb375b`

```dockerfile
```

-	Layers:
	-	`sha256:10a5cb69816f5fb40d5cb8fd4716f94b25eace99a05ca8df43e0dd52dcb899df`  
		Last Modified: Mon, 06 Jan 2025 20:36:13 GMT  
		Size: 2.5 MB (2534249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c1539603b557d41d86a4ffded1351b80889c33690a3eae44c40d5d8a1116caa`  
		Last Modified: Mon, 06 Jan 2025 20:36:12 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
