## `openjdk:26-ea-5-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:e12c0a3a75932d25f7169b169349cafdb1be99868989b8c2e8317621d4ac5910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:26-ea-5-jdk-slim-bullseye` - linux; amd64

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

### `openjdk:26-ea-5-jdk-slim-bullseye` - unknown; unknown

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
