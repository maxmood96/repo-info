## `openjdk:26-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:ef103f8c412b85c7679e9b8b4db3f813c3365eee984ad42d69b667a75a8fab7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:e5895b28fe65e7082b125bb262095127a985c5d25f2c323a3c6607615e124707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310530802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6cf49a16e243550d026efdf778a437e1df04989348fc3b6d45f16d7b101418`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jul 2025 18:39:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:39:37 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0b9e0c332974b134a26832e0094bd1e94146688157c40b653863949f251140`  
		Last Modified: Mon, 07 Jul 2025 20:59:50 GMT  
		Size: 38.1 MB (38092442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd235c0af5d1a9ffd16bde2fd2ff3d825891f567eaa53f4dc3c5ce860103dbb`  
		Last Modified: Mon, 07 Jul 2025 21:40:55 GMT  
		Size: 222.9 MB (222937812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:274ca70eed39d5c45a2ac0f0ef0f79101f3802bfbfb906f162db17643fb893fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fee690c357072492a9397f9ded301a6e2653c8f899285ea673d1592d29be2b`

```dockerfile
```

-	Layers:
	-	`sha256:9da6d59b67a28b8c43dcf2b8c8b4c70995c72d408568bddaaee4415f7f115566`  
		Last Modified: Mon, 07 Jul 2025 21:25:02 GMT  
		Size: 3.6 MB (3641292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ac265684df980af3ce35a266616a75a892decdc66ac421d8e673e95cae76ee`  
		Last Modified: Mon, 07 Jul 2025 21:25:03 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8f0a0171d200c0d95ab701618c9aa534e0d504528ef099ad21e15703d764b41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307237450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192f7247d3226eb2e5dac9a17293111fc9cd502112cb0094202a90e39e15c7c2`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Jun 2025 00:54:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
CMD ["/bin/bash"]
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 28 Jun 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+4
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='49aa2a8f29bd63727be9ab8e279ffceba2ee6d09beca9d221a69784da673476f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='529cc863c692cfa63afec612e73bdb9f2d8097a509454664315649e9955a16c2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e41c14547bdbf6ff3b0e0c9c9c5853d4884135fac836a7107e73bc0a6a42f5`  
		Last Modified: Wed, 02 Jul 2025 06:14:27 GMT  
		Size: 38.5 MB (38495386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f736abc40b0e765a20958a7fd15ad60b2895b6bc91ca7d8e6dde7bd1e7068711`  
		Last Modified: Wed, 02 Jul 2025 09:34:08 GMT  
		Size: 220.7 MB (220654980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:41e6652dd5b57c86af73499b7962d6d929940481cbba090ff165140a18ace45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222ff5a7a14a7ac74137487627ce1cbb3a5246b5efc562b805137bcc29092c9c`

```dockerfile
```

-	Layers:
	-	`sha256:53289adcb639cf9848cabe16c51803129c8d85df6443d1d65807c21fdec27a1f`  
		Last Modified: Wed, 02 Jul 2025 09:24:19 GMT  
		Size: 3.6 MB (3639054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e6b0de6180c1e173ce4a2373ada48f5545e89321be9ea00e50f6bb3caeea3d`  
		Last Modified: Wed, 02 Jul 2025 09:24:20 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
