## `openjdk:27-ea-4-jdk`

```console
$ docker pull openjdk@sha256:d74229610f0c67ed577407864f27c0f5558cf87f7776f672c2ed06c89091fe6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-4-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:66cff965e580d106a0c859e76edd28d3318d312f2a3f5ba8d8c415d58bbd300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313529546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c2ee565fd5c8432f8e63b7d37760d6d25b6a48c02fe8e509450ef5e460a80a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:08:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:08:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 12 Jan 2026 20:08:12 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:12 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:12 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d474d946492df41b7e7a91f3c19601cad11d4aa8558516013ba64b34a781712`  
		Last Modified: Mon, 12 Jan 2026 20:08:51 GMT  
		Size: 38.3 MB (38299942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b34947e8cb3e4a23f3db1037f3c281ab1d66ea3e4b15deab9e347d9e73d88`  
		Last Modified: Mon, 12 Jan 2026 20:08:57 GMT  
		Size: 227.9 MB (227912606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:59ec1d3bc1b89a8fcdb10858616b650ef0e71f340f62cdbf6ab91af0a3f9e804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb9edb7e9b3628024bb4b369657e88f6aff81a1dbc6a48c674eec903f986ad2`

```dockerfile
```

-	Layers:
	-	`sha256:e3c899cca72b2d7faa74d626fe107c75046f9eb17dce767bfb4525540e02bfc7`  
		Last Modified: Mon, 12 Jan 2026 22:26:06 GMT  
		Size: 3.7 MB (3655351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050f18a3eee86b339c361d5509139c140b47d08d27d3d20537253a693316e3c1`  
		Last Modified: Mon, 12 Jan 2026 22:26:07 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6bd028cb7d91ca940e92fb1cc9f957c3495c30225f8b87f1e3c5a158e956767b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310438656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7594b54857d107ed5f8795abf4c94db3973ec397b28452a60960f6a86ba4c99a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:08:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:09:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 12 Jan 2026 20:09:11 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:11 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:11 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa04a99adbceec323b63783930bd43b8598872c6606f6327ba43849b46744fe`  
		Last Modified: Mon, 12 Jan 2026 20:09:47 GMT  
		Size: 38.7 MB (38696847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756d8d562e401d3e356a0d092df909ed3601330c8f52c2518496ba73b29e86ba`  
		Last Modified: Mon, 12 Jan 2026 20:10:07 GMT  
		Size: 225.8 MB (225836269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a35079649b126f2cc8efc7bf2268ae2caa1a9a5df384d1a89215ed6ba3b283eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc00c8bd46297151310add8312300e5d53ec6f351b69f696a01d4cfa9338f49`

```dockerfile
```

-	Layers:
	-	`sha256:ad863713a98f09184e84362665c9ef5b5052ecc0c150d3d7b944a64641f18a76`  
		Last Modified: Mon, 12 Jan 2026 22:26:12 GMT  
		Size: 3.7 MB (3653041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb06d7555f99b22544ddd13ceb41045579534895b7c300603fa9a14856aa78d6`  
		Last Modified: Mon, 12 Jan 2026 22:26:13 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-jdk` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:f508322c5de16185ab75ddaaef289a5be413830748e1c6e0f5780843c3aa8789
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478222735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d912435bbf1d851f509d490193d09110a8033a609301f90105f154a4b5970b8a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Mon, 12 Jan 2026 20:08:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Jan 2026 20:08:40 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:08:41 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 12 Jan 2026 20:08:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:08:47 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Mon, 12 Jan 2026 20:08:48 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Mon, 12 Jan 2026 20:09:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:09:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0fc345c745ab527cfd9026b3df35ae3819ee35a168bbe9c00ae31a737d548d`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66931726c3351b015957271f86fff15a7e69cd1984120336f1f1247d63146a22`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 398.3 KB (398288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdf745d3bef4d8bf855d54ddd29ac431efe5e8c34bfc4b4f47e2972c333b343`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc07ce5d0b6fe8fb039f9415551f3029c61e42c67c91096d678be23227fb2b`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 379.4 KB (379360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2891f70eb3c29eb50060e862743983618f4c0cbe66a5d7b8c54781bfcedc69c8`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6c0561395e8c1b679b819aa49af6c97d2cfb813e6ea83e9cf2eedcc9f4512`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c117aeac8da1df9fa84368e26034719cb02127bb704d6243c4fa973ba6d31`  
		Last Modified: Mon, 12 Jan 2026 20:25:57 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da1fa60e1ef8abae4ab0d2593451388520041a53bbde8e9edf367f1267bf0b`  
		Last Modified: Mon, 12 Jan 2026 20:27:40 GMT  
		Size: 224.3 MB (224316802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b94f6e771f9dafd74afc47df4bfb20c52e825f8412d5bb8099f011fc3f15e`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-4-jdk` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:3ee88105ef2b6b434b11c6fc040dc79eae9c229e11e86471fb11fe612c60e100
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2005037582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab684191e94ca6fe0225dc99089efca1a9e60b1e0890b30c245d54c80e4b54e3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 12 Jan 2026 20:07:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Jan 2026 20:08:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:22:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 12 Jan 2026 20:22:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:22:08 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:22:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Mon, 12 Jan 2026 20:22:10 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Mon, 12 Jan 2026 20:22:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:22:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ae91ebb6b06916422f2db8a3c6f63e9ad96d44267ea6c1205256cd05e31ad9`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d05d2dbb94cd655893e275edfdc5a2e8865eb5e7e9e1dcece1cc5c60c612687`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 504.0 KB (503972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61db3d75ae7eb5350754e82153323abe625c73bbfa3c9100125d605844ff5e1`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258674f52f307fa2c7d52de6c1b9fdb8537f14f91bb01485436c3857ede17948`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 351.9 KB (351932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e0892981fd3355c92448b345eb8c727bae3d9d56ca599be1ea587a273e2d73`  
		Last Modified: Mon, 12 Jan 2026 20:23:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a95c936c85b99ef2a32737b748254e16a31c5835d3551846bfef262a925d85`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef02c6d1e7049fc8c2d6e03a0affdfc5f9ac2b695e9a754d0f821ba81300806`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567278d15110aa014186e974fc217ed91f6e537aa9778ff010a9d69d389f7d6`  
		Last Modified: Mon, 12 Jan 2026 20:25:37 GMT  
		Size: 224.3 MB (224294550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046342707d74e0d1a4a5edc74bc827934a82072b4c5a9ae7c5e70a31bca73e89`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
