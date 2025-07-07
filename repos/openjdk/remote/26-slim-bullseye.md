## `openjdk:26-slim-bullseye`

```console
$ docker pull openjdk@sha256:991926a262ce25427040ffb5e71490951850c4a311b43868bad76837d20da82e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:47fcdfc0bb677c74414287a4f8404c784bc5d521529e0d4bb95f7a4530e28c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254935606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69a57648386afedfce819a5e8f9320042b17e852a4c00adb0619bd87e18e4fb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924babc950a58ed2205015d6f1855bc7a1aaff814d7888d0204d392c7b30c256`  
		Last Modified: Mon, 07 Jul 2025 21:01:02 GMT  
		Size: 1.6 MB (1583560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223977fd6f92c9f0a8e94fe7ffdf399ce2f9c4efcbfafca936300b85e0dfbe7a`  
		Last Modified: Mon, 07 Jul 2025 21:41:22 GMT  
		Size: 223.1 MB (223095999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f0f2d3be4d85c5b927774de95b0be4911a31e72991fc1585b266a005106bde78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d423d19ef0cfebf3502a636304295c4a1481d7f79bae64c6632769cfd5c6cb`

```dockerfile
```

-	Layers:
	-	`sha256:2a9150dfe4c21fc315bf5cb905f563bb695e6ea1d4d5a5e46ba00b13d0e705a1`  
		Last Modified: Mon, 07 Jul 2025 21:25:33 GMT  
		Size: 2.9 MB (2942642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281b9b8a520c202b0d377ae15dc338cd5a07507b6128f10d6768c1ad6724ab4a`  
		Last Modified: Mon, 07 Jul 2025 21:25:33 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1c02e65e4db625530f0dd0b88599e877b4cb4c0061d3d22c20a000417681434d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251123577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca5df11c960b05f6e407ce0696b36ec7a9d82d6e49f32ece22c17ce9207e882`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Jun 2025 00:54:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 28 Jun 2025 00:54:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+4
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='49aa2a8f29bd63727be9ab8e279ffceba2ee6d09beca9d221a69784da673476f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='529cc863c692cfa63afec612e73bdb9f2d8097a509454664315649e9955a16c2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480e6ba42e9b93790207d2cffe82f71c4bbfb92871f7982c3a5ba4ce9b96e222`  
		Last Modified: Tue, 01 Jul 2025 07:35:13 GMT  
		Size: 1.6 MB (1567207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1136514abdba7b5924f5600da9c140c8b1d464b387135e885491aadc33d9f`  
		Last Modified: Tue, 01 Jul 2025 11:27:47 GMT  
		Size: 220.8 MB (220812230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:50e761adb973cb59aa1613007950e361d8dc111137251554aff2f3fefc22f0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885c6b06fc780459aede999f74f5e3cd77d4ab4d9fd29db6f9bf959bdf2d09e`

```dockerfile
```

-	Layers:
	-	`sha256:4ce0ee6a3a572fcad4c4e30418636b7f2f7b90fa44b03ade73bd1718d7c075db`  
		Last Modified: Tue, 01 Jul 2025 09:24:36 GMT  
		Size: 2.9 MB (2942294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:374e7a84dd6166a0819f6c18e46fe8a4a2f87de850e7de4de7daac7a0f6affcc`  
		Last Modified: Tue, 01 Jul 2025 09:24:36 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
