## `openjdk:27-ea-13-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:3eb87e08c90db226c9f0ab03cc26c1304e92a5041e1c5c34d463870db3a52ef8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-13-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:c8baa8fc26efda7a3176a207d22f6e660eab97fd0956466aaf0db88b3c908698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260753142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3550f509439f11b2ad9c582da60a17137adaca22d776aee3ea32bde2a6c950f1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 22:46:25 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:46:25 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:46:25 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 22:46:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:46:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca184effe416637ecac468c8129a256e1793b53982497172a91db8b46483e951`  
		Last Modified: Mon, 16 Mar 2026 22:46:44 GMT  
		Size: 2.4 MB (2371125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86fdacee4ed859737074f7e139c39178d2acc39bec1b2839402b7653a58672b`  
		Last Modified: Mon, 16 Mar 2026 22:46:49 GMT  
		Size: 228.6 MB (228606517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:99074d3d7358e72f9b00914a126ac81b24c4bb1254312629406b5f52b32db387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022501e1bf2a90f0103b41d76653d35c35bfa50db1a9884a35b4ef775a9d5742`

```dockerfile
```

-	Layers:
	-	`sha256:539dc24daa7416e9047bb5dbb8baba1b90f74f1df134c5c02dd9410aa1200fa9`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 2.3 MB (2278895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e3ad14dfe9253dca42aff46160884111af32ad3bd0991d1320495d23a075f6`  
		Last Modified: Mon, 16 Mar 2026 22:46:44 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-13-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e560f41ca16c698e94d399b02fae557b11ceac5dd7830f7a47eef785ba4c248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259024983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c58da14fad5fb2fcb92165b093476441caea1e55b38821ba8f221bf3903c2b4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:48:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 22:48:40 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:48:40 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:48:40 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 22:48:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:48:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a43f0ca9752e55ccb798c69d8ade3d9559d8103f1ba4e8d5116de1489c6367`  
		Last Modified: Mon, 16 Mar 2026 22:49:01 GMT  
		Size: 2.3 MB (2314409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7c7bc29a76f3a82854dfd6303ad1fa97a67548bf971119a92d47e973e5faf7`  
		Last Modified: Mon, 16 Mar 2026 22:49:06 GMT  
		Size: 226.6 MB (226572158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6ec21af87f2b902059e83dfacddd2a1db6cc5725091f740504da1a8a6b9cee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e6ab4f415c714f9eea58fbeec6b9f98e18f8397db67fa3a6ad1f831bb63d6a`

```dockerfile
```

-	Layers:
	-	`sha256:b7101f822accb9413db82ba7957f0ee6d88e9636b27b0226bde330f7bcd5bd85`  
		Last Modified: Mon, 16 Mar 2026 22:49:01 GMT  
		Size: 2.3 MB (2278581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:315a87da2f594a82eff3d30d317025aeea3c5be1f12c48689199e9ec53ec3a51`  
		Last Modified: Mon, 16 Mar 2026 22:49:01 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
