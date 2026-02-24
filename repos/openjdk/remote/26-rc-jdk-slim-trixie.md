## `openjdk:26-rc-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:87c58b59f089d5bd0914bcbe26e53c9284201401a6f5b3d9a1240b17cf8d455d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:d04b43693a4320ca0440de830751fa1e9b387e526441e086f25015e9db28245e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260258863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0c16fdefdc7df12d66ce00b67ca6b14782227ef4768736180705d8b05821a6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:28:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 24 Feb 2026 19:28:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:28:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:28:10 GMT
ENV JAVA_VERSION=26
# Tue, 24 Feb 2026 19:28:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:28:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a39ca790f65cb2bf34e1db99ad0e8c8fcfd1b8e7c0587e05c6b3ebf24c1aad`  
		Last Modified: Tue, 24 Feb 2026 19:28:28 GMT  
		Size: 2.4 MB (2371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9bacee0d1e9e6f41a9c9f974a4b24059d9f88ca1d7cdd2bd0c45c75b37d62`  
		Last Modified: Tue, 24 Feb 2026 19:28:33 GMT  
		Size: 228.1 MB (228109194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:59e00f6bea39c85f37903b2f457b838edcda852ae7d70c9ee21ae7a6dae6f87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110290a07761cca2131e40f44a503e087375a1807d1c7f9191a50d80f5b4ae72`

```dockerfile
```

-	Layers:
	-	`sha256:e16c92665d3a53210ffa49f1f06684487d0915558891848b04bae1479ac2dab1`  
		Last Modified: Tue, 24 Feb 2026 19:28:28 GMT  
		Size: 2.3 MB (2278168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0dc0a91644cb80a5d556bfdf8b0a9e5ae39bedd57b571e11ccb33bfe74e7fb`  
		Last Modified: Tue, 24 Feb 2026 19:28:28 GMT  
		Size: 16.9 KB (16873 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3eb3566a082b94caf29492a0edc855350e18294351f607b8b1e53512ebbd5fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258490073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0f716af1314f5c50a915d34778af75e7b2f87434ae7652d43e965f2bfb5323`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:32:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:32:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 24 Feb 2026 19:32:56 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:32:56 GMT
ENV JAVA_VERSION=26
# Tue, 24 Feb 2026 19:32:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:32:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a99f8dd5047f2067238dc441a532f871f52ed72c30c4ace6674d537113bba58`  
		Last Modified: Tue, 24 Feb 2026 19:33:17 GMT  
		Size: 2.3 MB (2314432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f4a53d267eb01c6aaf31ef1a113064f3307449f31e4981e34ec5beab09195`  
		Last Modified: Tue, 24 Feb 2026 19:33:22 GMT  
		Size: 226.0 MB (226035543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:26345bf02061fbde727f7fe5c69f59f2032cd60c9b748d4c8c821c6a4b14a009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66b74211c4271831182430c86bdee54901e5b61b1d90c5747bf1c4ea5ffb799`

```dockerfile
```

-	Layers:
	-	`sha256:1ead902ab4ce6e0bb219fe540b84148513c1e1eae59d68bad8fa53d9335a4c73`  
		Last Modified: Tue, 24 Feb 2026 19:33:17 GMT  
		Size: 2.3 MB (2277806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224b0f14d3b36c5e9adbd307259b8fdeb207f83590a9cdcbb38f0e4f35cefdf8`  
		Last Modified: Tue, 24 Feb 2026 19:33:17 GMT  
		Size: 17.0 KB (16991 bytes)  
		MIME: application/vnd.in-toto+json
