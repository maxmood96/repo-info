## `openjdk:26-ea-slim`

```console
$ docker pull openjdk@sha256:c93c84cf7ef4c489aaf96fb7f5a14a347c9a819e536474982462a3bc7e289797
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:5aec658ca064390bf8425e93f96dc1127de387b992bd545908a5046bdad3f467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255483317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9428ee079a8b2fa72723e157ef20e691834920102aac9c01df3c521d16d787`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 09 Jun 2025 19:07:09 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 19:07:09 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='9d95d3e025035bfe649be52a1a5f94e28f66af98693db6b4e879fa3be4dc4e69'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b80805bd34f0513f09b4cbf9928fb8c73a883c6979ba1df56e71f1b7c12e434'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9459f5ddbaa110278ecdcae7713b3a7e5b94fae310b0b16c09d74125e8cc2739`  
		Last Modified: Mon, 09 Jun 2025 22:06:38 GMT  
		Size: 4.0 MB (4019986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ecb7cf2420604e0a69c7668749802afb8faa9c075d90b808eb3131152ee32b`  
		Last Modified: Tue, 10 Jun 2025 00:42:26 GMT  
		Size: 223.2 MB (223238001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:c5070241b3f05405ce2282ad3a2c79ed2fe7c1b8b90e33fd5c3e3f434af53129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e44573f89a26bda890a5cf97f4d22203a6bbdfe1e19b3f06e272663ab5ac40c`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3b839629c8abb63f5d3fd2135e4dc8ba066b1181a05876039067b02312f56`  
		Last Modified: Tue, 10 Jun 2025 00:26:01 GMT  
		Size: 2.7 MB (2651963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27bd327fe5ec45dae8ffe0485a7f2dd3ac17775791fcf60f69f645eca92aa145`  
		Last Modified: Tue, 10 Jun 2025 00:26:02 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c63439936ccc73c29471034680d9a6544c9fd548be15262adbc37e8e1dbfab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252922008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406c33cc54f95c11e6485ea2ede954418c6ec30b96cbe6290cdd73ba998b65c9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 09 Jun 2025 19:07:09 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 19:07:09 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='9d95d3e025035bfe649be52a1a5f94e28f66af98693db6b4e879fa3be4dc4e69'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b80805bd34f0513f09b4cbf9928fb8c73a883c6979ba1df56e71f1b7c12e434'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8146c9804947f80186d66b9250eee5d43b401e06d60a6f4b0867bfcea74b84e`  
		Last Modified: Tue, 03 Jun 2025 16:25:08 GMT  
		Size: 3.8 MB (3835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b718c7e60de447244c2840ce199301db6b9a2bfab432f872ee972869c32c643`  
		Last Modified: Tue, 10 Jun 2025 00:42:33 GMT  
		Size: 221.0 MB (221021463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:ea0e6574bdf74f829c3d337017bfdc388ccc312bae78e5d5ab34685af20125a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47951c5ecf6106f96875713ee5b559f144655d986c039e82777c6aad7984f64`

```dockerfile
```

-	Layers:
	-	`sha256:38b0a9dc0dcce3a4fa8d519d2c4f887af26ca25d45ff23492a6d483521aab753`  
		Last Modified: Tue, 10 Jun 2025 00:26:06 GMT  
		Size: 2.7 MB (2651693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14216a3e827fb8689af4ec7993111afcdb2d91c0d63bf297a450626af230b906`  
		Last Modified: Tue, 10 Jun 2025 00:26:07 GMT  
		Size: 19.6 KB (19639 bytes)  
		MIME: application/vnd.in-toto+json
