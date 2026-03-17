## `openjdk:26-rc-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:1ee4eb446d1e7fc44848eb84799a2d08d1e1fd428da6f69093abf8bdada2299f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:71d0ba940a18515bc0a880ece0fbc9075b0c6a6b6d868610f41f2bef223dc6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260371836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a618f032c169c25cf351702c22dc4f405025516e6a0c772b2602ce8505f285`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 16 Mar 2026 22:46:22 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:46:22 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:46:22 GMT
ENV JAVA_VERSION=26
# Mon, 16 Mar 2026 22:46:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:46:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de3808e46409a3f9a477fd4ea8e48a36b4b7b31d366f7799e427561551d76d2`  
		Last Modified: Mon, 16 Mar 2026 22:46:42 GMT  
		Size: 4.0 MB (4029192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c121f9eed603c80a1c93b13828c39c65af14b01996dcfb07da1aeaab1efde45`  
		Last Modified: Mon, 16 Mar 2026 22:46:46 GMT  
		Size: 228.1 MB (228106419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c07a7f3b707ab7ca1b1ffe0df1b4851d5a63c2cbbac5febc36ad1b2a2f554384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb8b25d0e83fcbf2966b9c5e649e899272d172baa388fe5f06851f64029e0dd`

```dockerfile
```

-	Layers:
	-	`sha256:df187c899628e952f6ec50e3eecd392777f978be7434b1fad53a41dd8afaefae`  
		Last Modified: Mon, 16 Mar 2026 22:46:42 GMT  
		Size: 2.6 MB (2649744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2378482c24170fc4954903ec5ff83fed27d9e3fcba106f080a74f4b65ccc08f3`  
		Last Modified: Mon, 16 Mar 2026 22:46:42 GMT  
		Size: 16.3 KB (16267 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:63ab7b0139ae0644bb213fa670f64a9da4f3d99fd730ff55bc405cdbccddc5d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257997840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d90f3c2add17df57043058b6d5859ea3c1e0aa26b27bcdbdbe3eb4c3457bf07`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 16 Mar 2026 22:48:24 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:48:24 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:48:24 GMT
ENV JAVA_VERSION=26
# Mon, 16 Mar 2026 22:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9e2087c29461cdd3938cd152653be4b0501859f0436f9ee802079c38a40c70`  
		Last Modified: Mon, 16 Mar 2026 22:48:45 GMT  
		Size: 3.9 MB (3851974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e92083b8d5275af2bae8ac29bd4d0459bcf4a4940d8703d5d2a50500bc8903`  
		Last Modified: Mon, 16 Mar 2026 22:48:49 GMT  
		Size: 226.0 MB (226029801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c717fa9dcf65200a3bf8ad26d710e2d786c45b6edb5839f87b205448d2ff31cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cb6edda487d05326a508d89187f1325ca9f0079483acb3e0f5d9c871cd967f`

```dockerfile
```

-	Layers:
	-	`sha256:0be9df531c1f228a8ee275d36ad621b7db0d433e455b739c66db12fc6dc46cbe`  
		Last Modified: Mon, 16 Mar 2026 22:48:44 GMT  
		Size: 2.6 MB (2649354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41dcbc010384b8924227c1ea472ad5cd61b90249db781daa5b2479a6e180231`  
		Last Modified: Mon, 16 Mar 2026 22:48:44 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json
