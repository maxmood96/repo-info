## `openjdk:27-ea-3-jdk-oracle`

```console
$ docker pull openjdk@sha256:d6d41b7d2d84f9c740bfb5fc6a14f7e166f39a29ee085ca2275f184f0b41565e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-3-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:d16207ee89ce49fb7b15a8adac551321589c8effaf59e7878b4c5f19e5496d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313541987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3e2ac75f36c7834220c60049652f8a484eb7fba6ee288609cdc1a7829a430a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 06 Jan 2026 18:35:35 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 18:35:35 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jan 2026 18:35:35 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 06 Jan 2026 18:35:35 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 06 Jan 2026 18:35:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbf6bbe9372d42f174442a34bcb5f2b935b166ac96e1db2b5ec8b7831919d02`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 38.3 MB (38298919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e7c0f7c27cf8bc8dd1fb0d13587edc56f2e5e7ea57055707192a6951106df`  
		Last Modified: Tue, 06 Jan 2026 18:36:18 GMT  
		Size: 227.9 MB (227926070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d78322fb252dc29e7010d6fcc10ccede9ae08578d99504b195f5af384f54d75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b87058d751bdd01b3b9064e66ef7e5d2b7e1fef2a8cdfe8cbbf04648d85136`

```dockerfile
```

-	Layers:
	-	`sha256:8d8483ad35d4e9c032bc9e10dbf071be4eaddce74c093103c45ecef6f22ca04c`  
		Last Modified: Tue, 06 Jan 2026 19:24:12 GMT  
		Size: 3.7 MB (3655343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4216f1a93de4a66a820fbd4d3ff25086608436bf20114ca7a00a91464770cc16`  
		Last Modified: Tue, 06 Jan 2026 19:24:13 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-3-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d628db6172dd3c6a79642f64a45bc124a499e6bbaae3b988016eba4a8d569d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310461573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25362698285a7c02504499d8c7d4431f487ff6d3fbecf4471c8397b08a91c90`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:36:32 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 06 Jan 2026 18:36:45 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 18:36:45 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jan 2026 18:36:45 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 06 Jan 2026 18:36:45 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 06 Jan 2026 18:36:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6d6b35db767fda1d9d3942e4e296726328299f6d8fd81ce1869bb1b8cf9bb1`  
		Last Modified: Tue, 06 Jan 2026 18:37:23 GMT  
		Size: 38.7 MB (38700254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aed520ec4f4e63fefea6a3b540a7cfc905ab4d6549713fe8ca8c96891e97058`  
		Last Modified: Tue, 06 Jan 2026 18:37:26 GMT  
		Size: 225.9 MB (225855779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6892a71bc1a14aa0d1fbbe61c7dc34a3ba6893669daa789520164e54dca349b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bb131d2d4e69d1b2896425865e3b8af0d8de5c7be73072385e3e4201d62f7c`

```dockerfile
```

-	Layers:
	-	`sha256:e7888f41d724bf9cc4b01036d3f7cf89677bcfc43e7d21b85fe42d3e980cb699`  
		Last Modified: Tue, 06 Jan 2026 19:24:17 GMT  
		Size: 3.7 MB (3653033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0badfc0a177898a484f289474b4b2271fe02f98beeffb3f6c52af50000db8e`  
		Last Modified: Tue, 06 Jan 2026 19:24:18 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
