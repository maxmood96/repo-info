## `openjdk:27-ea-10-jdk`

```console
$ docker pull openjdk@sha256:6c70d851dde0dd6f3a823a63c2fca7fe0217d737820797e084b04663f8e2e566
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-10-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a8b6e69329feb7614fd5d4b7d54d69dce859e25318254dd90f7fb642cd0128eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313985847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb537604e95672ea3a378d841fdaee8c1aebd4f86507d6fd9a70499de7c56d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Sat, 21 Feb 2026 01:28:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 21 Feb 2026 01:28:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 21 Feb 2026 01:28:38 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:28:38 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:28:38 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:28:38 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:28:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9bd672210818c0c09d6939ec6b7e6ba2ccf3d968391f51fcfeb3c6f1d25379`  
		Last Modified: Sat, 21 Feb 2026 01:29:01 GMT  
		Size: 38.3 MB (38296371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3c388863bce15fb3a9c1a0acd47038c949e0e06fcb56cec112bd139d90f765`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 228.4 MB (228380605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:1bcf43e2c857dfc6a5aa6a3711f96c636eed2ef6056b1a83dffc3ee74e9af9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb3a1384ee8b9b0b93e00fce2da184bb32597f7b0adc68858963f7b80f815de`

```dockerfile
```

-	Layers:
	-	`sha256:5ab77068673b246b6d8630a3d193b8e59d5b6df1689f040b54164a96cacd6ecd`  
		Last Modified: Sat, 21 Feb 2026 01:29:00 GMT  
		Size: 3.7 MB (3655435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda033f5a118409625336a92b40e99951eda8b3857f267925ca8be2cfb3644ce`  
		Last Modified: Sat, 21 Feb 2026 01:28:59 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-10-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1a8bbbe4f874c1f959906fc77cc4ad754cb0dcf47da789f427172a4e8614343a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310929206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b4bdac97b2f8e74fc4d08cb20f4cd0bfecf4b5cfc6a63cd10dc40612909ffd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Sat, 21 Feb 2026 01:28:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 21 Feb 2026 01:28:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 21 Feb 2026 01:28:39 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:28:39 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:28:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:28:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8396e6db6b9853e7bf9bec482b6aadd9eea2eea888beec7d439cc8d5476b6fc4`  
		Last Modified: Sat, 21 Feb 2026 01:29:02 GMT  
		Size: 38.7 MB (38693484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f0b5b05b68e6d51eb7cf6f9e2d485ccf5695cf2782eba0a6502e6124d3210f`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 226.3 MB (226333742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5970cf3fb620b21c0df4c2213daa06a8f91dff5926d04ad054a917720d9a1be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec556468ea204a59c3e0f6b382c77ff0e8d676f09d85e368b33351535aec4f1c`

```dockerfile
```

-	Layers:
	-	`sha256:93951b20ab17761be1dc8ec3a60addce6766414cffda0acedadd240b760318f4`  
		Last Modified: Sat, 21 Feb 2026 01:29:00 GMT  
		Size: 3.7 MB (3653125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b444668ecf2896b67c06ecd2f83cd7f1e2bf29cc683ca1a48cac2047f13bd3`  
		Last Modified: Sat, 21 Feb 2026 01:29:00 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-10-jdk` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:6a6abfadfd4389d19bcc7f0e90bb946c0b3b0ff88ee10e26e341d6a0bb5a5a9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190344306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e12410c5095c7c9f16421dbf1e75f952dea803fc307167e255909847a1573`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 21 Feb 2026 01:29:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Feb 2026 01:30:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:30:31 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 21 Feb 2026 01:30:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:30:38 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:30:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_windows-x64_bin.zip
# Sat, 21 Feb 2026 01:30:40 GMT
ENV JAVA_SHA256=243b7c1e79f8514af5765815d8b878c7362cacf8a9c4312c5c9c9e7a1eeee3e9
# Sat, 21 Feb 2026 01:31:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:31:05 GMT
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
	-	`sha256:ed279eb0342bef67902cea078249b3d8f293221bbabe9fd782807ef367d2f9ce`  
		Last Modified: Sat, 21 Feb 2026 01:31:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ab2e4d9c8b47716dbdfb7620c2b1d3650b8682266886cfbf2c6e2c95d9b264`  
		Last Modified: Sat, 21 Feb 2026 01:31:13 GMT  
		Size: 371.4 KB (371435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51ac31a6f483f4d42b35504bea2c102969677853332f3ab6f8fc1fec51ca9cd`  
		Last Modified: Sat, 21 Feb 2026 01:31:12 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9017fa80ba8ffb37007b40cbb36be76e39204c35d6f9b1330a800bf6a370d7`  
		Last Modified: Sat, 21 Feb 2026 01:31:13 GMT  
		Size: 354.4 KB (354358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eb8f1107344fcd54e30c4296415a0e84287490d895c2f97337799f5a986856`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc8d211a9b01c1bf008a396006e3d5a7b8af6bf596b9776589f177ad2c2b04`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8762a6e4fd07791a5f5d92e4f66238558e86b787a98de110287a285a5d72003`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1e29faceb09e635a69e197f1c2569e5018fbe0e462079f0c3b1df43a968254`  
		Last Modified: Sat, 21 Feb 2026 01:31:26 GMT  
		Size: 224.9 MB (224850811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3906a273f1ac9add148f64b77396e404c3cfdc5017bb684362c69fc8e0343b`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-10-jdk` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:24e5a260da8c574b7232f3191ad9cc21d5966524909f8d54ae8b89bd08bc67be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088364326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4f20b44fa7828f77b3bb5949fd9c99033a8b324095d81aba563557dae115cd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 21 Feb 2026 01:26:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Feb 2026 01:27:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:27:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 21 Feb 2026 01:27:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:27:09 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:27:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_windows-x64_bin.zip
# Sat, 21 Feb 2026 01:27:10 GMT
ENV JAVA_SHA256=243b7c1e79f8514af5765815d8b878c7362cacf8a9c4312c5c9c9e7a1eeee3e9
# Sat, 21 Feb 2026 01:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:28:58 GMT
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
	-	`sha256:4455e12a722854dec189070503128f07b315332481bd47ab452831f38dee2024`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994b76b7872980b61a0083cfa6cf66aaaead8b2419a21599d91179a735134c33`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 496.7 KB (496733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca81ba43813b91e8f016387b3b31f870e2c80fcee0cd3660ad532f6c08c8e24d`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc4fbc86b4134ba5b52de34e6d38c3e017c75cac92621f976a81487cb2fc65e`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 344.2 KB (344205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d948c33ed1543b39bba0fba694ed5134d0e8492c95d058bbf5fc165ab385922`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f337d7603f477a8287d116bd201911577005cf4f8208281c54031991139dc`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7388502ef9b29d6f07ab81a98f7fba272b5e950ea08befaace6915e2a42bda50`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3a9454f2509be81920740dd24ac124c46498fd9a90e901c4b1ecb7e79b9a31`  
		Last Modified: Sat, 21 Feb 2026 01:29:20 GMT  
		Size: 224.9 MB (224858332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87699a62cfa4074e20326cea14fb09aeffdf9c9496ac6df7986ad7d8ddf1cf2`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
