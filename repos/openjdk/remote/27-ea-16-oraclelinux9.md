## `openjdk:27-ea-16-oraclelinux9`

```console
$ docker pull openjdk@sha256:932349837554319e26bb73cfda3194a97063a5402527ba3296e1f4bb52568a59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-16-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:26eacf25f93996dd2bd9ec0a11cec4c5abcc2c91f07fbab6708d4c84b22b91ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314399850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba3ba10b06d99f4a5039df977a077d1a144aaaddaae950fa5ffa30d43204109`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Mon, 06 Apr 2026 18:24:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 06 Apr 2026 18:24:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 06 Apr 2026 18:24:34 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:24:34 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:24:34 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:24:34 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 06 Apr 2026 18:24:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998edec12bfc51a6cf8cb6a1fea4115cef9c17044a6bc9c84e398059122e8e0b`  
		Last Modified: Mon, 06 Apr 2026 18:24:57 GMT  
		Size: 38.3 MB (38297709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3499e982ea4aad562fb81ad30ba117fb5f3ac31aca7096f7553e04abee5dc2b1`  
		Last Modified: Mon, 06 Apr 2026 18:25:02 GMT  
		Size: 228.8 MB (228791872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f2cfb647bb943e6a876d5fe4dfcadfe73c0e9638d612bd6fee9005350f650e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115071e0c7eb186f24469bd8fe2213f49256401205f8da9ecf888e29e495d026`

```dockerfile
```

-	Layers:
	-	`sha256:c83cf8e0ec134f4e4c9e541bd28d6410bbb34e001da6ff45f52af695614f9de7`  
		Last Modified: Mon, 06 Apr 2026 18:24:55 GMT  
		Size: 3.7 MB (3652947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a50626264f8be9d803d0a4cd6d7ac84de5d7a53729af942404cf93770f2556`  
		Last Modified: Mon, 06 Apr 2026 18:24:54 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-16-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d5ea72a794033b557283e27970e2e8225cdaa909b6e5a9b5df1ad0942c8b66fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311349773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f790915deb01d6d399ae02d46a1274052b721ea396e7651a17aa0af3d04471a6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Mon, 06 Apr 2026 18:24:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 06 Apr 2026 18:25:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 06 Apr 2026 18:25:03 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:25:03 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:25:03 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:25:03 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 06 Apr 2026 18:25:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5f0e07464dd1aaa92eb7a4ac1f8b1c253b8f63a587a938084e615be190676`  
		Last Modified: Mon, 06 Apr 2026 18:25:26 GMT  
		Size: 38.7 MB (38692472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd458e5e031ae73566b3e498ac82c4c9c1491c9022594232625c356411e6642`  
		Last Modified: Mon, 06 Apr 2026 18:25:29 GMT  
		Size: 226.8 MB (226759319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:b64088fa6212aaff0290d6f134389163984eb73fed1b1106895f75ef7931d884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3666003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5b251accbdd7919d3073f6ddc69ca742e92fb418ccfd5d82e9f8e391c92074`

```dockerfile
```

-	Layers:
	-	`sha256:9435704640e93468580078f4780271e2ea01b6cd50faec53433c911d58afd2af`  
		Last Modified: Mon, 06 Apr 2026 18:25:25 GMT  
		Size: 3.7 MB (3650541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dea330c345fc9bfb70250d1109563371dc475b7f04a77dc95b7e9351db33fda`  
		Last Modified: Mon, 06 Apr 2026 18:25:24 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
