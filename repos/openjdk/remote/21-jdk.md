## `openjdk:21-jdk`

```console
$ docker pull openjdk@sha256:1f8e1c7ec6b273ce3e639d60187dec922d3705bc9195558ceab328054b90bc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `openjdk:21-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:22e96613efd892f6af829ba7867b8226a682d657fafc92a0533de753004842b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255933527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b7c9d1482134e904cfb1f939053ea9b7ded78c76edda75f58369a18a0fced`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:12 GMT
ADD file:f2aead35bfc542632b7274d3b1132eb2bb3752d6cb61414febbffb746120622c in / 
# Fri, 27 Jan 2023 23:36:13 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 23:54:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 27 Jan 2023 23:54:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 27 Jan 2023 23:54:20 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:54:20 GMT
ENV LANG=C.UTF-8
# Fri, 27 Jan 2023 23:54:20 GMT
ENV JAVA_VERSION=21-ea+6
# Fri, 27 Jan 2023 23:54:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/6/GPL/openjdk-21-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='42cc4d00436ce57168aeb9c1e19e1f52f3338be6a53943b2bbbfa645fd0c7bff'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/6/GPL/openjdk-21-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3ecc95318c2a450012f0415ccd8c0de1bae00e0228f7fed7dade040638814c34'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Jan 2023 23:54:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:39fbafb6c7ef40878b859fd0e4475c5ebd2ddfa8ed785a588594e8731b7cd0e8`  
		Last Modified: Fri, 27 Jan 2023 23:37:50 GMT  
		Size: 44.6 MB (44561081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70086a6ca030344addd4b8e51d50d209385d29d8e70c28a102f5d9668e8535b9`  
		Last Modified: Fri, 27 Jan 2023 23:59:16 GMT  
		Size: 12.3 MB (12251614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a16f980a7552d3daee890bb609da2f1c05122d67a91e768aeb87aaad48a9b1`  
		Last Modified: Fri, 27 Jan 2023 23:59:39 GMT  
		Size: 199.1 MB (199120832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:626642f49b93f61fc461ae0fe51fc0785442950e3ff4001e6bb0ae8fe820b7a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254119142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435befa8a63c758745e70c760e9bd7b8ed4ffb418746b92731400afa0cc9bfbe`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 22:41:06 GMT
ADD file:63b5b4161762e1845c1eb2bb2c967a07179819b4a1f12ab7596d9c6bd15c9cbd in / 
# Fri, 27 Jan 2023 22:41:06 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 22:58:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 27 Jan 2023 22:58:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 27 Jan 2023 22:58:45 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 22:58:45 GMT
ENV LANG=C.UTF-8
# Fri, 27 Jan 2023 22:58:45 GMT
ENV JAVA_VERSION=21-ea+6
# Fri, 27 Jan 2023 22:58:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/6/GPL/openjdk-21-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='42cc4d00436ce57168aeb9c1e19e1f52f3338be6a53943b2bbbfa645fd0c7bff'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/6/GPL/openjdk-21-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3ecc95318c2a450012f0415ccd8c0de1bae00e0228f7fed7dade040638814c34'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Jan 2023 22:58:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d26cdabfc8c6a31055d655a58d8a8f9757f43e1ce58451b8b6b02c5dd6e6d482`  
		Last Modified: Fri, 27 Jan 2023 22:42:28 GMT  
		Size: 43.5 MB (43456742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175fa1491e9fc183c9d73f4393db52b943e03e50258cf81fd2c6970905be7318`  
		Last Modified: Fri, 27 Jan 2023 23:04:19 GMT  
		Size: 13.1 MB (13068665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7184256fcfbedfe6dbf18c3b7be86b3e6bc0f34cbaa3fac3b5cfd03c71c2f0`  
		Last Modified: Fri, 27 Jan 2023 23:04:30 GMT  
		Size: 197.6 MB (197593735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk` - windows version 10.0.20348.1487; amd64

```console
$ docker pull openjdk@sha256:29bd6a30840171ee54c60489703807e827baf65abe42889a43cdd8faa5543ab2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1581773775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58292d957c1649f2e7946d1b17f3e812a08ab9941dc14c4073e42eeb3e6a37a7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:07:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:07:35 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:07:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 20 Jan 2023 22:16:30 GMT
ENV JAVA_VERSION=21-ea+6
# Fri, 20 Jan 2023 22:16:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/6/GPL/openjdk-21-ea+6_windows-x64_bin.zip
# Fri, 20 Jan 2023 22:16:33 GMT
ENV JAVA_SHA256=7b6fc834d28b4beb09ec65861767bab492c8375f1840c9df33c79e8521d4f955
# Fri, 20 Jan 2023 22:17:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 20 Jan 2023 22:17:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa8e5b91e3c425a756945d0dec251c1595992592fd0dcf4df0ec0a7962717eb`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 614.6 KB (614563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6284573ed998f0926754c8fd5dc7faff95102e54cf06b0d280cd07428b048e11`  
		Last Modified: Thu, 12 Jan 2023 05:22:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee2720203565dd5e40979d2f76187379d7c05254dd58609d0f974f653b1db40`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 552.5 KB (552462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cce8ee928cc2744119f7d564eb83205271d7612f37c7e56b516fccb17532f6`  
		Last Modified: Sat, 21 Jan 2023 02:19:12 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3be27c69b7ed746ea1d2ac96a8ca1ee1702f53a010c9c7bec1e0eccde6f8e`  
		Last Modified: Sat, 21 Jan 2023 02:19:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2185f9fd7249dd254eb38118ea1dd98b7cbe160f44ba112531b89d370fd604c`  
		Last Modified: Sat, 21 Jan 2023 02:19:12 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebaaaeac657741d815afc2850ce1674a1eebffdbbb09d542688f79758de768d`  
		Last Modified: Sat, 21 Jan 2023 02:19:35 GMT  
		Size: 194.6 MB (194569278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2be264bcaf79de33df15e48e792674b8daa647cdf2fe2d8738fe94955ebaa8`  
		Last Modified: Sat, 21 Jan 2023 02:19:12 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:4411d6cfc6e4e4288d29d99c9dfa31e724d19533e348bea6c75bc8553ca2f551
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1903004543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5d519094603e784cb4bc3dc79fa7a772e637726c6d25c9acc6d78ce72bffde`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:09:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:09:36 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:10:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 20 Jan 2023 22:18:06 GMT
ENV JAVA_VERSION=21-ea+6
# Fri, 20 Jan 2023 22:18:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/6/GPL/openjdk-21-ea+6_windows-x64_bin.zip
# Fri, 20 Jan 2023 22:18:09 GMT
ENV JAVA_SHA256=7b6fc834d28b4beb09ec65861767bab492c8375f1840c9df33c79e8521d4f955
# Fri, 20 Jan 2023 22:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 20 Jan 2023 22:19:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fe1d317f0927d209417077d671ba0fb8e3b7ff9c583727da819f0d16252e80`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 367.5 KB (367453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6807e3d75deac242f3cfe460728c148c2f68e1d8366ad3f0358a3c9237042b6`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe0b64cf9fa2560a38a4c1a75582463f16f8e35e9776b14d87cd13167e4281`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 320.0 KB (320032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709e64db8228ecface39a4922e84eecf7468c7f41dbeecca238d891f2b86a5bb`  
		Last Modified: Sat, 21 Jan 2023 02:19:52 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3580b805283202348d798c815fc6b61c3ea3fbe7d5ec845dd40664343a332d`  
		Last Modified: Sat, 21 Jan 2023 02:19:52 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f267d4eecdf71ad1235569e22192b494e43cc1217972b6eb9e62ab79e672871`  
		Last Modified: Sat, 21 Jan 2023 02:19:52 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9e65b3aeaff1d7779aaf42c8886e2529dd326e985f7640d577e0e528e1f12d`  
		Last Modified: Sat, 21 Jan 2023 02:20:16 GMT  
		Size: 194.4 MB (194364885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158d8951e4102e20497878a16927fd7447683a7bf67b975b9b8aa0f5112eea7a`  
		Last Modified: Sat, 21 Jan 2023 02:19:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
