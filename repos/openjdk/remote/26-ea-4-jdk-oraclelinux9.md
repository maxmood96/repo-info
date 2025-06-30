## `openjdk:26-ea-4-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:d99233d88063abea2cab873079b24994ee2abaee19116a52a0f2f6708d5e9dcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-4-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:91cb591465358a631809946d21e4d8cfb5acd55fab2b685701094398b975970b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310459460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd263a60f3d44f4344f747da07a803792c8f4706734423bca47af1778950bb1b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Jun 2025 23:22:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 25 Jun 2025 23:22:00 GMT
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b708cdfd909aa007afaf0cd052ec13b343cc61d506253442731b14edcdfd4801`  
		Last Modified: Mon, 30 Jun 2025 17:29:08 GMT  
		Size: 38.1 MB (38092150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd06e053f651e29fdb4bc6f1ead55056dab2d731fa8661ea5246fbda799a3cef`  
		Last Modified: Mon, 30 Jun 2025 18:32:15 GMT  
		Size: 222.9 MB (222866648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-4-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:49a5e4e7f1245b6e5c6dd8138ec9eea694346ca15e952ef0a27e108cd90052cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb49fad455094437960ab9e9ac796359713eb8cbf76262f1d7a35fa020c85972`

```dockerfile
```

-	Layers:
	-	`sha256:06c47726e0446ba67bc309a2077ff388135a645421bfac426b96d647dc984bf7`  
		Last Modified: Mon, 30 Jun 2025 18:25:25 GMT  
		Size: 3.6 MB (3641292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ad22620f8788cbe671edcdf9e2233fbe3485231bcf4907adfe58796067ea91`  
		Last Modified: Mon, 30 Jun 2025 18:25:26 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-4-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dc64f7766bb24e255a0d6b970b13261746e9b91f8d22e4b999480d44db5a1cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307237320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e1f38f3e6de988a5d555d094333dc79dba196ab3bb41b81b7374e58f13fe84`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Jun 2025 23:22:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 25 Jun 2025 23:22:52 GMT
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
	-	`sha256:8651adb19772f22f50f38bb61855702b5099b0a0045fea8c9db8dcc1cadfea34`  
		Last Modified: Thu, 26 Jun 2025 05:13:18 GMT  
		Size: 48.1 MB (48087180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0ee1c604fdbae17917604a097f1f42ae8abcc22cd62c1260386266d1d6ac8`  
		Last Modified: Thu, 26 Jun 2025 04:43:33 GMT  
		Size: 38.5 MB (38495135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9327765445f688b9b9b791e125cc8913cfba1c56fb74de1b6f80a34ac86c666a`  
		Last Modified: Mon, 30 Jun 2025 18:32:05 GMT  
		Size: 220.7 MB (220655005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-4-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:44c424995431fad847ebc9f97713d5e7fdeb88d0a56a166525cf9994fc2b80b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b871b1a3b519c1cbe53304dbc63655313d8169762d6703028656627d582c306e`

```dockerfile
```

-	Layers:
	-	`sha256:76e735371769752e6f4c7b1adfb2f10e7d931c8128b44d98a00cc7464811d57c`  
		Last Modified: Mon, 30 Jun 2025 18:25:31 GMT  
		Size: 3.6 MB (3639054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c78090ed94c75f11c18e180db391294e4257f31b53f01f0e8d7dc840559f8c`  
		Last Modified: Mon, 30 Jun 2025 18:25:32 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
