## `openjdk:25-ea-17-jdk`

```console
$ docker pull openjdk@sha256:71bb6bd76fb93696b294a26a99f270d814dbe255544ab0561aeba4ae2e5e0055
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `openjdk:25-ea-17-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:1453e4e37021b5651245970754bd9ca40c8f9aaa22a34b655754f7c109f38638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299438524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ed2a3e0d92e4768633e690d671c15211b1fd56d12044894237fa0d5276d810`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b72bbf6c6a350ed2d03800acd047c623c1bcb0d27833ef77d6741004e4094c`  
		Last Modified: Mon, 07 Apr 2025 22:38:15 GMT  
		Size: 38.1 MB (38108112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f15d75c29b5ee3f30ec3cc6ad81c9476c66aa5c33531d9a30ff7efb1dbc87d2`  
		Last Modified: Mon, 07 Apr 2025 22:38:17 GMT  
		Size: 212.2 MB (212239202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-17-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b5487b1a0867d6255fdd747408dd8ef82a03705e8bd47c5f7884744caa0bfd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e34a68d19693facb5a829c6c8c7c03c17213fa1ad14eb0fdbb8b124f190593`

```dockerfile
```

-	Layers:
	-	`sha256:b6c0b84141b49a8fd8bc2fe64531c9c97c3ae97519616fcabf7ca19a9451ad97`  
		Last Modified: Mon, 07 Apr 2025 22:38:14 GMT  
		Size: 3.6 MB (3624506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80e6013f2c073525888c0f5e70cf95026e94d79c8f40588b53af9eaa984a574e`  
		Last Modified: Mon, 07 Apr 2025 22:38:14 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-17-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:aa4c77d889fd838ab78edb45aa6fe589df1172e3cac844db961a7df07c4cd847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296248884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc7a94dd378c2134f0c1dc52151d882de5b14b8867b29a5d1c71c3d1a03578f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc73a32668bc167dbd00ff7118bdb7d58568584dac2f5c61e9057497c36e654b`  
		Last Modified: Tue, 01 Apr 2025 01:13:12 GMT  
		Size: 38.5 MB (38500679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fdd020d6415a1cedec5e7262d874cd0fc98b46a52c0e118117dc5572c394f3`  
		Last Modified: Mon, 07 Apr 2025 22:52:08 GMT  
		Size: 210.1 MB (210073382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-17-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b2c625eb7e6caee5632801afb8ca813f09dc5f93f9e86b5902feeecd69ca54a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bbb2c35230a000e5bb5f571c2039bfc03b56bf20f76918410236ffdaf1eadd`

```dockerfile
```

-	Layers:
	-	`sha256:94b070ab6ff4cead60c8ac8347533466083cfaaf9490cd1335aa576f9dc7b442`  
		Last Modified: Mon, 07 Apr 2025 22:52:04 GMT  
		Size: 3.6 MB (3622262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b09363dce0ce9288c1bf657f0c257d5f52ba6873178cc095c1c0165781327c`  
		Last Modified: Mon, 07 Apr 2025 22:52:03 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-17-jdk` - windows version 10.0.26100.3775; amd64

```console
$ docker pull openjdk@sha256:9180feb2a5a3a91f4845d874aa654f5e9fa4a0daa0c2dbc1642e48a9de348972
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3603763931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd371fc75b9e9c6d4ecf91ce01e7ce5e1f714afc796b20e15e727d7906005faf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:49:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:49:44 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 00:49:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:49:54 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 00:49:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_windows-x64_bin.zip
# Wed, 09 Apr 2025 00:49:57 GMT
ENV JAVA_SHA256=46c47281310039b4e8d7e583a1629bfb2ca08a102794c3a68d1f2051101e9f5b
# Wed, 09 Apr 2025 00:50:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:50:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4421324a5d82f1532ca4f4f8c3f3a46ea089f697096c41559aa63e8c88d9feb1`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8999c0d868c51f88dbf27c4a0dc8aefdda18ea0356df7d3b1e34b724005b5080`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 367.9 KB (367911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc012495130e3a0ae9399601254a6897b2d8df4f57fa6652f81f322b8b00635`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5927f63ef491059db77b52528a506d430a2aec5116a570a6d7e8297c9aacbeef`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 354.7 KB (354709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8011b0d24d2f2482d6e56731e1f6304cd71918afd80b989ef6d3a099afdb4114`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cf5a60a550cb3ca7c38007a46b2487c0fb34728fb47e518a256cd2cdfaca7e`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8269bfbec0d9583badb286a551789fd4e2ae40ca896c88adfd889a15ff935c5`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d3ab8c70214ed52d5c08e86428092dc1bd752730d25141f4a132231b3ea60`  
		Last Modified: Wed, 09 Apr 2025 00:50:37 GMT  
		Size: 208.4 MB (208354054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352880e1f5682a7be7e7b95465f692e5435848797c12ebb618719a0b1d67f9fe`  
		Last Modified: Wed, 09 Apr 2025 00:50:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-17-jdk` - windows version 10.0.20348.3453; amd64

```console
$ docker pull openjdk@sha256:c0954461eecf4d7baa4c6457e85240af50b08dc21963605f5d1b7dea659a3e6b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2479996220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24d8c12f2378caf782056cdeb2c17e8170eb2fdc99de0fee3d41511f950d6c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:48:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:48:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:48:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 00:48:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:48:45 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 00:48:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_windows-x64_bin.zip
# Wed, 09 Apr 2025 00:48:46 GMT
ENV JAVA_SHA256=46c47281310039b4e8d7e583a1629bfb2ca08a102794c3a68d1f2051101e9f5b
# Wed, 09 Apr 2025 00:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:49:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1725b949f271948738dd74be509c3f9885faee7889f91e60cb776d644e80093`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc96e579503c81e09d425e008f32a85d6f65083661c993e9d875712df18c9791`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 348.7 KB (348708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe17892597c242561d3c862d619654905e9dadfb73fc2a10b8e5b8936061a35`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364e7f4c5f62ccf2d5c8c347977b5bdf977a3aac01859c4721272f42b4eab083`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 335.1 KB (335053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec550b18eddc6bba47031c6916be9e4e60419e43275e992ac38cab644f9a1800`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b317ba8e78c1b63d7773b3930df3ffa685441ea6ecc3c14a1d031b6fdc262fd2`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a2fbed936c9dd0687cbe3834a2e426a4e6212aba8381077f85a41038fd95c3`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cdfe45a7631746d14a9334343ab1e59198d35a8d713cd07afeea0d410838cf`  
		Last Modified: Wed, 09 Apr 2025 00:49:22 GMT  
		Size: 208.3 MB (208308976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00972856ccc41326779514c3c03b345ba39103ee142dc5c62608f8b3fc576197`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-17-jdk` - windows version 10.0.17763.7136; amd64

```console
$ docker pull openjdk@sha256:1603154078d941b3d609206e93a1070325ab47779b600158441379aa50c91626
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2371692760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139704ac86833b01ea875fb6f5ee0bbf2606ad4c76e4b53b0a8ee9737638afc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:04:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:05:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:05:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 01:05:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:05:35 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 01:05:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_windows-x64_bin.zip
# Wed, 09 Apr 2025 01:05:37 GMT
ENV JAVA_SHA256=46c47281310039b4e8d7e583a1629bfb2ca08a102794c3a68d1f2051101e9f5b
# Wed, 09 Apr 2025 01:06:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:06:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccce759214b5cc94f0d493c8374bf94f12c711734dcb2a995d2ce56a3a25013`  
		Last Modified: Wed, 09 Apr 2025 01:06:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf514a523f524809bd0f3561b943c2f7985c8428183f52553b3c350e0dedd5b`  
		Last Modified: Wed, 09 Apr 2025 01:06:08 GMT  
		Size: 332.5 KB (332491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592ff6df9a1f92e87c62a416aae9d4056c32ef2ee095c5b02125bae253ca5ac`  
		Last Modified: Wed, 09 Apr 2025 01:06:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13178848ee7919569d6c166258771fa684e34d1fd273e9d76b9843899684d84f`  
		Last Modified: Wed, 09 Apr 2025 01:06:07 GMT  
		Size: 317.2 KB (317243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e0f1b2759f00c692cb8776008820d81534b0809d30b6d92f1b01fa3fe5aab8`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab2508b18a927fb4be63aac475ed56592db925cf53d7d8529b4eb09fbb600b`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d0edc950a2a4a05c20612f9736fe87879c5e0b463d13bc2ed33d0b7a7d50db`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5968e43975c84c37d9ebaa2f904b7c72730ab6948ad716b9cb0a12f5ca2af87`  
		Last Modified: Wed, 09 Apr 2025 01:06:18 GMT  
		Size: 208.3 MB (208309348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d77ffabdb44cf89a19ff1609ac661283ff8f02db2bf6ce2cfdbc3fa3f3eac2`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
