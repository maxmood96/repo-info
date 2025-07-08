## `openjdk:25-ea-30-jdk`

```console
$ docker pull openjdk@sha256:b297c329c82273582353dea312621614ce844f7a667d0386beef7f88792f220e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-30-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a5cb5d4a7921f573675d6374b574dd79154241007d8776f5928ede0b8814c03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310648292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d5d5bf5353325e38e7d4fd2e7e9e045a320ece62fbcbe1591363b9862a2455`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jul 2025 18:39:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:39:37 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad0cab3faec3438bcfbccacca666f745132fdfb9c0b58be7d741f94c36a176`  
		Last Modified: Mon, 07 Jul 2025 21:00:12 GMT  
		Size: 38.1 MB (38092469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9147bc517b3cefdb78a99efe0f50b2427dc09f0c0dc058dfd1bb7b1d57784a5d`  
		Last Modified: Mon, 07 Jul 2025 21:34:12 GMT  
		Size: 223.1 MB (223055275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-30-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:75b8173946f66cda1e6e5e0266834559e8de96d6c01c648cfcc973e15bf1b983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b888151f5447c053f82e530efa4e371b076f58c802a943b2f19ec2b35a12d7e`

```dockerfile
```

-	Layers:
	-	`sha256:cb57cc7296acb5638fdae42235171dc086cee2dec01aababa23d18ba6fd5fae1`  
		Last Modified: Mon, 07 Jul 2025 21:23:21 GMT  
		Size: 3.6 MB (3641308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a11356e5b6eff60e7136a3053b3000c501697e0448cec4a0c680469914a276f`  
		Last Modified: Mon, 07 Jul 2025 21:23:22 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-30-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:562c93d2f4381202814b0381f638e5dc63531c7afad744be754c73a4f0f30e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307440576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226ad99ef26f101ee9881243692b6ebb1704a9b11e191b9b9ee92970aad368d2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jul 2025 18:40:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:40:37 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
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
	-	`sha256:a1b3616054de9c0bac9f37201aae5e8167e6a19029f86b2031922b31f9187f1b`  
		Last Modified: Tue, 08 Jul 2025 12:51:41 GMT  
		Size: 220.9 MB (220858106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-30-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a57edbfc81d2b51caf7cccfd57c86989f22614b14c724f6460f46091c258b3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc2338a8a60568f7dfe146cee6eef0521b30c88c1e0d293248e190aa0621e95`

```dockerfile
```

-	Layers:
	-	`sha256:c751d3f226bacf254540334efb6b5314eeeb2423e7717a96d36297a05e0677f6`  
		Last Modified: Tue, 08 Jul 2025 03:23:23 GMT  
		Size: 3.6 MB (3639070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a7f5f760050e96e22cade72ba69aee7815ecc3bf6c7d8c9a51cb2044bdf6b0`  
		Last Modified: Tue, 08 Jul 2025 03:23:24 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-30-jdk` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:1c69e529ede3ab119e53a9701cb474cc8d1f8c9a9063d0374bc9fc83c4d12a62
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695900861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056fac987f4f9b090aadbb2adc483988f4dc559144dd2c90fd5bd2f0b15bffb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 07 Jul 2025 21:04:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 21:04:50 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:51 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Jul 2025 21:04:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:59 GMT
ENV JAVA_VERSION=25-ea+30
# Mon, 07 Jul 2025 21:05:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_windows-x64_bin.zip
# Mon, 07 Jul 2025 21:05:01 GMT
ENV JAVA_SHA256=917fc8ab9ae5f7aa7aa1d45bd5a8612a2fd33d6835b9a42728532d0a14f8b42e
# Mon, 07 Jul 2025 21:05:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:05:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e938d6b0e5edca79a5928df43e859a2a15a22090811426cdc69ac2f310ffa1`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ca2ae35f583f195c485d73ced4b3e8630948eaa76211b5996325e7c378a4d`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 396.2 KB (396151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30dce903d7d0c48719fbff751e24f2e557b696c6efca989f4e69dd567213552`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb21b589c9ed77c9f72fb7cb963350d12aecde199f606cbf7824ecea1e0d390`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 381.2 KB (381244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41db697c19c1d0ab66b5408ad82dccbaeda0e6baf187283a21680b55d83cbfc`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988e83c8a9bcd145930bc544c99e16f706af0448473d98b4d98320aaae4d08a8`  
		Last Modified: Mon, 07 Jul 2025 21:09:03 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac2d5b11295729549ce3d04541d90710929fa6a2c81ae644257aac33a82adf6`  
		Last Modified: Mon, 07 Jul 2025 21:09:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431fc89c7171ac6909d98b0213d2a14001c26f67731b36780c7d99efa11c212f`  
		Last Modified: Mon, 07 Jul 2025 22:08:55 GMT  
		Size: 218.9 MB (218941690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d1bb8c66f23651f4c061bcfceb97cb9e42f004255d495978220082ff8f6615`  
		Last Modified: Mon, 07 Jul 2025 21:09:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-30-jdk` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:b465a4175b4d5107f23fe193b13b3e54b12fe3cc34d7eca74dc6ee7074247b01
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499862580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae92283a71c98b78928e6d79e99b9bf26130dad670c448cb35271ed94e59301`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 07 Jul 2025 20:59:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 20:59:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Jul 2025 20:59:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:34 GMT
ENV JAVA_VERSION=25-ea+30
# Mon, 07 Jul 2025 20:59:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_windows-x64_bin.zip
# Mon, 07 Jul 2025 20:59:36 GMT
ENV JAVA_SHA256=917fc8ab9ae5f7aa7aa1d45bd5a8612a2fd33d6835b9a42728532d0a14f8b42e
# Mon, 07 Jul 2025 20:59:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:00:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f18c600e3f1e6920a9c13e2bc1cb85fe722ed3f4c485d7232ab8b219784bdb`  
		Last Modified: Mon, 07 Jul 2025 21:00:28 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eceaeca1107bb95fdc4e4cf9e11b6ab194048ffc8d2dcbac5d04a78f093cce5`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 356.7 KB (356728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff3c45c8aa311b9ea73d06c6812e68a19df67ef9b9620162bb77958a8cde4`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d2c54236a297b70de340f1058bf553e9f801f477c9bf5f3f3a781810e731c`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 345.4 KB (345449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea667565e692cf293be7cb956420752cfa282d797157fe71009c15e4c6afcea`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0844edca565cc66cea58c88d52881bcf4ec81bf0d8597e8725497acf387b6a69`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6426423c9c77930251dba727e82e1616b45f18e4dc07733653607065b30874`  
		Last Modified: Mon, 07 Jul 2025 21:00:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4142f979958b0d74dacddbf46f937781885770bc9abbf4116b435e3b72b25531`  
		Last Modified: Mon, 07 Jul 2025 21:05:52 GMT  
		Size: 218.9 MB (218901116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325bc6bc2c5ff81b9dab75b85fcea93ffe06f03ccec9027af8b78444a00a305d`  
		Last Modified: Mon, 07 Jul 2025 21:00:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
