## `openjdk:26-ea-jdk`

```console
$ docker pull openjdk@sha256:633763f8b329dfe36329f645f17be3c62f6dfff04a68f52f8f57ec005b0351f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:d3167546648699ebff600c118212f6c71c3cc4662ddbda51ce55e9e079eb2bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310533072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4224982cda77bf249b832207e58946492633940c800fe851a2e1512825bd8815`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 09 Aug 2025 00:54:27 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:54:27 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_VERSION=26-ea+10
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:10aec8a104c7ecf055b7137fb34a3666fce4dff1b9f6d210fb88eaddd4c8c329`  
		Last Modified: Thu, 07 Aug 2025 23:49:00 GMT  
		Size: 49.5 MB (49497127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4410a0e9228cc9a481698904112d3e9413d78a9dda6a6ce0bb611241177327`  
		Last Modified: Tue, 12 Aug 2025 21:38:47 GMT  
		Size: 38.0 MB (38004919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71248dd11db07b378397ed2ce1b106645db07f5ce2b92e7cfc3dc48756936d2`  
		Last Modified: Tue, 12 Aug 2025 21:39:33 GMT  
		Size: 223.0 MB (223031026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b4c658e7614822573dc6cddcb21bbbc1845723ca200bd8476daa00d17d559c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed566736b1915b15fb2f04d08723c124c7ea9dec22fede9c6e6642310b59437f`

```dockerfile
```

-	Layers:
	-	`sha256:4fcfcd782d10fe4e95e76dacac1a720ded5d3fe129241212a23d6e8fec85266b`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ea113f79adfb35e94898ee1a549fbb8b215f9f6cb4616fa411ee582d039595`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cc575a9948d4e49e9b2ec0ecb34df713fda0c6ddc211f46e878b7d329d139516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307350070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb57f7ec2fe7f8b65532d5b1068654bda5def9af59275a81e2beebed08a9a3b3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 09 Aug 2025 00:54:27 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:54:27 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_VERSION=26-ea+10
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868932e6de7288e116d57bafe15e69e4d2baebd6453c84a2fbd529067b423d95`  
		Last Modified: Fri, 08 Aug 2025 00:24:48 GMT  
		Size: 38.4 MB (38407094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289551c254514963e8c6627fcc26f871a1bc4bcdf7b3a365ae18366bb01acf44`  
		Last Modified: Wed, 13 Aug 2025 05:56:52 GMT  
		Size: 220.9 MB (220856065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:72b039f7250944a7239ceda7f024222dba42ec3060c583f7cd6da51a8a38b232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d666b4eb915dd747b6dfa99725b8282eee58379889cadf935f45e51bab7d24c`

```dockerfile
```

-	Layers:
	-	`sha256:e74f79ae332fd4823922043d3a6ffe37554215488c155efb2ccc6f25f4a4aa37`  
		Last Modified: Wed, 13 Aug 2025 00:24:28 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1719f0bfad08aef3b9b609b5e1903b255d463f6009f7e61164d4bd8ddc71691`  
		Last Modified: Wed, 13 Aug 2025 00:24:29 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:cb3de8b0192c637700f4ee674b04f9c04aa3e5ffa59282473159be0b65746440
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718547204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5802e0dba17a2bef41300e1fb7b72371ee2969438820262f99cc0f31586916ef`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:33:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:34:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 12 Aug 2025 20:34:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:13 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 20:34:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:14 GMT
ENV JAVA_SHA256=da62aabe3ec673f91e3aafcc742d67304275407dff329118db9e2bcfbddaca5b
# Tue, 12 Aug 2025 20:34:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a10cef8978ae5290ca7e18220c36d2928dcd71d266fde25547632fda46297f`  
		Last Modified: Tue, 12 Aug 2025 20:38:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9132b3afc45b96364af8e47a7f150cb8465174096316ad5e629f052d57dc133`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6882e0d97c94644f7699a23cb82dd0c92270b7a6f44d4cb1148ba0eec10a3d7c`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5af1b40091e65f279501459bce9f39ead2d2d663e723e6b89f9c81914a4792`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 357.5 KB (357504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bf86809e91c72d4e72a1b9e423ff18d59bb9d1359ca14d2d68a0a3327d79e`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d18cf2f1cb9e14f740e1a068b47a7ef1a814a94a4941178af0d4f5fb8fa57a7`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ccdad26d9d16038e40d6088fef1d46d4d0fa20d851f381db1901332f1ca522`  
		Last Modified: Tue, 12 Aug 2025 20:38:35 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d49f5602fa91b48113b5ed11ceff803e700242eb43ca7acb2989e8be3d9520`  
		Last Modified: Tue, 12 Aug 2025 20:46:42 GMT  
		Size: 219.0 MB (218975610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8999220a5fb6d9ae624f0c494abb5bb833542b1ac3ff0d4cc8fa3ba6f9ac20a`  
		Last Modified: Tue, 12 Aug 2025 20:38:36 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:9dcf7a78bafc7fa6267eeeefb728922c8a12354b66d90a78ae7b70c138ab19c2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501325534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d7b817de4dfc900c62202e6219f09748183dca07166ca5d3e3f577bc3c2cb3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:33:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:33:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:33:56 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 12 Aug 2025 20:34:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:04 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 20:34:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:06 GMT
ENV JAVA_SHA256=da62aabe3ec673f91e3aafcc742d67304275407dff329118db9e2bcfbddaca5b
# Tue, 12 Aug 2025 20:34:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb44453f998ae873970ebb2cf9b7344ada6208d3ae918dce541baeee8c1c9e5f`  
		Last Modified: Tue, 12 Aug 2025 20:36:03 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51105a5697c7f6efd7db63b43b8c993512296bc774ff582d7a0e2358cb7c015`  
		Last Modified: Tue, 12 Aug 2025 20:36:02 GMT  
		Size: 343.2 KB (343173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97361a7aae0233b88c7dc8390dcc770147179e16250461d0081192b3ff11e2e9`  
		Last Modified: Tue, 12 Aug 2025 20:36:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b08e89ce9d068a79f518d0c4afdba46c035bd946a97e40a0246336cb5d49fa`  
		Last Modified: Tue, 12 Aug 2025 20:36:04 GMT  
		Size: 332.8 KB (332766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d08fe501ce613175f6fddad35a44d7a5b94835825fa9c6cbe12055fd0aee3f`  
		Last Modified: Tue, 12 Aug 2025 20:36:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd12050a61f8b6208a231be37f8bed489782e26a6214dd7b82ad8ff4cf1e6d5`  
		Last Modified: Tue, 12 Aug 2025 20:36:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a29f81b6a16a667683506a7076e956ea598d59531562ed3f6965bdf85514fb`  
		Last Modified: Tue, 12 Aug 2025 20:36:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2007a66b04ecaac5a23a7b367d7f8ced222d1a8a5fbe430c241165174affcad`  
		Last Modified: Tue, 12 Aug 2025 20:45:34 GMT  
		Size: 218.9 MB (218949928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6951832694311fa47b27a4fc8662b5ec77e8cb66b4d52a1465ead3f04d40b6`  
		Last Modified: Tue, 12 Aug 2025 20:36:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
