## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:b6d0da2bccddaae2b80e6e67d2cf674f26414fe1244d82f2c5d07b2c47fa9599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:6ad8f5ba98de3152a877030ac1e4868588ef2d76e893c5483ca590f76a5d27a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314021608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4c2a1c0b3755921db24168d90ed5b4b94b6904783de664d8908fd4d99d218f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 21:24:41 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 02 Mar 2026 21:24:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 02 Mar 2026 21:24:53 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:24:53 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:24:53 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:24:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:24:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b378f89d3b59dd1d2eadb50cf14516db8b51b7dab151586f2653e0c104fe11b7`  
		Last Modified: Mon, 02 Mar 2026 21:25:15 GMT  
		Size: 38.3 MB (38298090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fff2388df8d8696b6cd91a57a90a65878a99c47b7fb50a5a6e2afe2f12a48e`  
		Last Modified: Mon, 02 Mar 2026 21:25:19 GMT  
		Size: 228.4 MB (228414647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:aa9ebeb0d7dee793ede02cbe658c31a01acb00f87c6849295515736195c4dc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da9058b790de1d9c59dc66d62c14adfb041fa6d3fcf635ba6df1cbfc3a62856`

```dockerfile
```

-	Layers:
	-	`sha256:1d4c854ab448b678ce6af4ff009e65600fc3b0b5d720babebcc97ff84ec178b4`  
		Last Modified: Mon, 02 Mar 2026 21:25:13 GMT  
		Size: 3.7 MB (3655435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57996459cec9ed1926d136874dd11e49d447cc1b0644ea8bf713dcf31da24680`  
		Last Modified: Mon, 02 Mar 2026 21:25:13 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:effbf31705c8cbb117fb14b8575eef118ec7a352f3ed5cec394bb0dddd8b8ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310960194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7d3c576848f1f34bf6ae8993492e4a944bfb8af4cf9360dfc6f970bf48e575`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 21:23:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 02 Mar 2026 21:24:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 02 Mar 2026 21:24:06 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:24:06 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:24:06 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:24:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:24:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693a35fbad5e339ce57961bc78978d895c6cdf1e4ac0630de341d4ffb92f2c99`  
		Last Modified: Mon, 02 Mar 2026 21:24:29 GMT  
		Size: 38.7 MB (38693718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deb53670e5a776130fe4b9931c060550e0a0ded14903f7956657142f17c1c5a`  
		Last Modified: Mon, 02 Mar 2026 21:24:32 GMT  
		Size: 226.4 MB (226364496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f184d2a0a9cb56dc40a5705635c04cce1102fc3462140217e10c574ec1421ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0876ecafb5e974cee29a73da82a8cf5f85e5b56a82d708ba824da184fc6638e`

```dockerfile
```

-	Layers:
	-	`sha256:e1bfa79593bfe114beab7784c059036b8b63adcc5c0cf2fb0a9b0615b591a2f1`  
		Last Modified: Mon, 02 Mar 2026 21:24:28 GMT  
		Size: 3.7 MB (3653125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58afdbd10330b0b15ced6039052bb11168096a406a25cf4f4963d010e0986c95`  
		Last Modified: Mon, 02 Mar 2026 21:24:27 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:4bf38219511dbad7c38f385eff794d308e546e2c15158d312ad1d3a9b262ca01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190218926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d63b0adfa8e8f61d264170ded11f0007ca585f13fccb12329349e7d22c6c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Mon, 02 Mar 2026 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Mar 2026 21:26:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:26:15 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 02 Mar 2026 21:26:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:26:21 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:26:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_windows-x64_bin.zip
# Mon, 02 Mar 2026 21:26:23 GMT
ENV JAVA_SHA256=1ddea09bd3dbc807656ba83c0c62c5c0853849c254ca1d8b04786f58bc8d2341
# Mon, 02 Mar 2026 21:26:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:26:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85218dcf86c9e2514eedc07715218d85e9ed6365d1643d3444e2758598250d6b`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e103e013778cbf5e33317ff88baa8b5893736880345e505e9887d81469e313`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 371.7 KB (371712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f387b8fb26c147bba9d2d81029538d40d597732bf175e2c3276fadfd3e633`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3e8e48eb799b4e5f7596f8b161adcb3d77caa8706a2d1db57146725d601ba7`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 355.2 KB (355151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7661f27deb07e52f217d2ffa75645b063755a95ac893f86c3aa548ba3c3b39be`  
		Last Modified: Mon, 02 Mar 2026 21:26:55 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27019e83f7d26a4f955f9822b73e28f39e9cae2011c659a5f7a0f721ec9d00c`  
		Last Modified: Mon, 02 Mar 2026 21:26:55 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bbb0e16b596f7fb33fabfa73710ecdd42409ca10cda9e544a6adc7fddb701f`  
		Last Modified: Mon, 02 Mar 2026 21:26:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9b052aacd88779658d72d8ab5735538537b4bba42e193ef262cde25b214831`  
		Last Modified: Mon, 02 Mar 2026 21:27:11 GMT  
		Size: 224.7 MB (224724299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d70d9025517590aeee02024377ff2bc46d342fcebfeea05a60714a54fcf735a`  
		Last Modified: Mon, 02 Mar 2026 21:26:55 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:a90c99cb8a02f0732aee563280b2ff6d0a961a7480f5a9db2d6462fe10ca5dbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088196183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a63f1d76f8cf9344312187d9ec90c495bd2d833c1b027576ff679775733ef4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 02 Mar 2026 21:31:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Mar 2026 21:32:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:32:19 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 02 Mar 2026 21:32:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:32:29 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:32:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_windows-x64_bin.zip
# Mon, 02 Mar 2026 21:32:31 GMT
ENV JAVA_SHA256=1ddea09bd3dbc807656ba83c0c62c5c0853849c254ca1d8b04786f58bc8d2341
# Mon, 02 Mar 2026 21:34:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:34:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32d8d4cdda12590dd7b8059d3fd077d0a54988de5f46849a98a6a87aeea4cc`  
		Last Modified: Mon, 02 Mar 2026 21:34:30 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79692db1cfa7f9fa3e2d44b6786497d9da26038843a9ed777f998072f746e4b`  
		Last Modified: Mon, 02 Mar 2026 21:34:31 GMT  
		Size: 513.1 KB (513113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e85f6ac7856f87f3fd32db2cd12cdc94a11c5e759754fa4489f3f8939d50f`  
		Last Modified: Mon, 02 Mar 2026 21:34:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173b84a69e9a13c4ea8595fd5ab902e1f76111ff97fb2410a713e3eb474b8fe`  
		Last Modified: Mon, 02 Mar 2026 21:34:31 GMT  
		Size: 326.3 KB (326278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78eb30508a9e4a57d6543d1632b982f558b9d7aad05ec5aaa3893e350b24dfc5`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed81e81ee5bc3b661f1491d894793e9c7e3a8906cbbffb5c9e68a325c6d330d5`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cd17f3d3dd7091d62dda1518a7e58cab64c49165eeffeb1e45d3e6316402f`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec8224147f07b2868dfe0fa0180c7e7aef209b17b40c17f603b9d6216ea1971`  
		Last Modified: Mon, 02 Mar 2026 21:34:45 GMT  
		Size: 224.7 MB (224691651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b061d82a0880bd8593fc64aa1b8bd0aeb5047dd475cf3529f93dd0c295d2f9`  
		Last Modified: Mon, 02 Mar 2026 21:34:29 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
