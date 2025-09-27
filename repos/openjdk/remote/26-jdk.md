## `openjdk:26-jdk`

```console
$ docker pull openjdk@sha256:d68937e781574ae2d28e4cf88586bc43cb9f6d793411f6e501188b8b866c00ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:85bf1547e4f47a5a68edd1b89579b921ffe297b4a3fd9d6ce9be6b35ee00091a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313170498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61205f39abc35014919df946f7b2eb231992965a056b0f17e7334c85adad462b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3978622ba31aff71854710c68fe819e916e1ce4e21abc85be84f70fc2d4fa341`  
		Last Modified: Fri, 26 Sep 2025 22:15:01 GMT  
		Size: 38.1 MB (38082823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e26d0ee90a443892a5613a9be17fe407f9d4a263f49dc1098b67a1d493f697`  
		Last Modified: Sat, 27 Sep 2025 00:29:27 GMT  
		Size: 225.6 MB (225590679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:01b424cab3548c688f189c8417145239dd0e80983d7d2bd822392a854191f7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1b3e277ab6cff4697172e260a3d71b79b7d9ef9a77006c36184d697c404864`

```dockerfile
```

-	Layers:
	-	`sha256:6007011baa68c4f80c3eb86b1208df40f409e15e6655204058456eae9f0b477b`  
		Last Modified: Sat, 27 Sep 2025 00:23:27 GMT  
		Size: 3.6 MB (3640737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9ddcbe61b9036c882b6ac594753b2efb3dde01f622d7e469dec3c71aeb3d41`  
		Last Modified: Sat, 27 Sep 2025 00:23:28 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7f263ce94ce3cd88051c95552d99396f9d2202347e7b1a76faebc82bea813b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310056157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839f330ffc5de52ce88426d77f63762633428c2ea03f3c67e807aa215eb8baba`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7731c6ea3baa371ddae08c2fb859de4c036b6bb3645f0a586674f4bba25ac44`  
		Last Modified: Fri, 26 Sep 2025 22:14:24 GMT  
		Size: 38.5 MB (38490457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884042d7209f6dcdcfd725e9844c384044d68983b10cd58e5b59022ec8a71322`  
		Last Modified: Sat, 27 Sep 2025 00:24:17 GMT  
		Size: 223.5 MB (223477403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:e55df8e764165572d98e8f4400fdfa0df9d1602b9eb6867556d8386bb41df505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb6d298e3467ceb9e060eb53a0ce28439a98243e93dcabf2d1c3ecbc669b41`

```dockerfile
```

-	Layers:
	-	`sha256:8fe5084c40f2ce6472625065cf2963355c138e04fdbb712671ff67b16bb1c38d`  
		Last Modified: Sat, 27 Sep 2025 00:23:32 GMT  
		Size: 3.6 MB (3638499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3806d6b06110a62fc46f48538f2c6abeca5742a3acfe55c387f6a59f6dff8fcd`  
		Last Modified: Sat, 27 Sep 2025 00:23:33 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:fae012c81e329f7fd4eaf1ec6584ac039464e54b4a1084e5c65ec1665bba9653
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3793763073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d3bb0a0140eca3ead037e1ada6d72f28d43dfe61eda3d25df59d1865861a77`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 26 Sep 2025 22:01:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 22:01:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:01:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 26 Sep 2025 22:01:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:01:51 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 22:01:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_windows-x64_bin.zip
# Fri, 26 Sep 2025 22:01:52 GMT
ENV JAVA_SHA256=5232e47e862086980b6e18c5b212648b57221ea3661f5e4a368a78a5a905f677
# Fri, 26 Sep 2025 22:02:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:02:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127d1dcaf57b855d2a18529f04f68465361ae6574e2c30cd69535c2d6dbfee5`  
		Last Modified: Fri, 26 Sep 2025 22:11:09 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010682b59ccea315f50fb62e715de595bcfbf51152b2c19874f3808853db6fae`  
		Last Modified: Fri, 26 Sep 2025 22:11:09 GMT  
		Size: 400.0 KB (400004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed02dd38d9aa2bef1f1f39b76ebf71be7eb1e5b930c7568dc805d38e3b8166`  
		Last Modified: Fri, 26 Sep 2025 22:11:09 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414123a90d7ac6a66bf21a5f38348150671d28374f65167107c0328368ab1377`  
		Last Modified: Fri, 26 Sep 2025 22:11:10 GMT  
		Size: 373.0 KB (373043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a137c7b0fc399e9fc1e7e942ae9521ea9103cb57506b4f4b2c293863f0d8626`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed28f8f00045324c2faa7cac89cca00b6a562cce4afa462600594f555fb4a225`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864e2ae49679fe665d74b1c8df50148a2fc073dddcf8115093648fbc20f3815`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30c29adc8ae5e3f9d48cc4b9148e8cf8094b423035d35705022f1d2d12c48ba`  
		Last Modified: Fri, 26 Sep 2025 22:47:22 GMT  
		Size: 221.5 MB (221542474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35251f650a26c92eff3d57449a38cef0e64265be932fab6cb91194cc37e1f734`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:32e62cbf59b691e1e2f1c948ac18df18f0273f211fe39a573fb7912fb117dc32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504379459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849b94694fa20c6da370c9ca2f2a791be3f0065f960e5e9433d03fc0f5a6dbda`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 22:03:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 22:03:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:03:58 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 26 Sep 2025 22:04:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:04:06 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 22:04:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_windows-x64_bin.zip
# Fri, 26 Sep 2025 22:04:08 GMT
ENV JAVA_SHA256=5232e47e862086980b6e18c5b212648b57221ea3661f5e4a368a78a5a905f677
# Fri, 26 Sep 2025 22:05:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:05:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7380dd82e573dd1fb534faf790209813e4f1f136ded593b7e489f8e4727d7569`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50323695b31e3d1d4cc7baf6c3e6d3f4de0bd1e149d261f19d53c8107cfbe4f7`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 368.2 KB (368243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4172bb520e60e637f22921d9bc8c4bd6e446f15fbf70f93c40944ddebe41c07`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824b6f7f9b98f8d81c55904104df1a0975fc02c2986f24803eea86731a49d5dc`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 346.6 KB (346588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52204e8a94ec27f9196776e06d7c399ec17c76f9b545a0150ff42ac47fdea6e`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4910947c4237df258772e8290558a4b2b113a2c6aa749180d1b81103f46387`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f23730b4133f46419f0b0eba3ecff834c2a8fddd84b153e88935a9b985cc22`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1081dd2e451c47cabc45b979ccdcb3b6b7e397f4abd30f8009c27a0082f89be`  
		Last Modified: Fri, 26 Sep 2025 22:49:07 GMT  
		Size: 221.5 MB (221511804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793f6cef32e8c0574ae4a4fba9611b9cf273c56d7f8dfa20e2ede6d9ea5bab00`  
		Last Modified: Fri, 26 Sep 2025 22:17:01 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
