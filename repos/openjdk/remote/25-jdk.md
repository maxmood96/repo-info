## `openjdk:25-jdk`

```console
$ docker pull openjdk@sha256:0aea13718be560514fd7a417cbd8c25cd91417d0d93c13162bf58e1ff38603bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:af6d120c1d3a5f00b34c67b2aec3fa2279bb8662049142838996c3118871ef2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309683366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bfde7855064ecab55eae3fe305284e5a1828cd601647658637ec7323a28d24`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:53:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1d19e87a21f588780c1e2041d7a86fa8c5b805988de43968a7ad8419eeaf76d5`  
		Last Modified: Mon, 10 Feb 2025 19:28:42 GMT  
		Size: 49.1 MB (49097200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9cdf0ddb9ab240f0157d1a2e8b7eb6b7fa629a71987f6ed4ac9d26eb3f635f`  
		Last Modified: Tue, 11 Feb 2025 00:28:32 GMT  
		Size: 48.8 MB (48767933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a4b73366af81d3d4d1d41f76adf00ac8fa7f556b7e41fdcffae76899004a03`  
		Last Modified: Tue, 11 Feb 2025 00:28:35 GMT  
		Size: 211.8 MB (211818233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:9db810be921860dd46ec2ef1cee5f1daa0c543c889923c2fb13ef668b5dc14f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f152e73847cf588e4e743e8f0926e0880a4a9ef9e3dc8ca3d297227e3a17e4`

```dockerfile
```

-	Layers:
	-	`sha256:1db3ce73c51dd4ebb44db85ce4bc15f0384630f812ccf5b87b87ab25c270ad91`  
		Last Modified: Tue, 11 Feb 2025 00:28:31 GMT  
		Size: 4.9 MB (4910727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c6c349080a43ecc6a81b03c524104245e04e7613202c2dddf709af1f902677`  
		Last Modified: Tue, 11 Feb 2025 00:28:31 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e62e28f1621d2f3dd776da6536eda5e46558582df425c4c6c9478a11f1d4536b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306648253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4e286e722f923f1530f408ee4334ef35ad6ba57184c401593e0eef30684378`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:53:06 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63067de277ccb20d99a5e9991dc66234bee83ce4c0d53f55d9f51995ad436f8b`  
		Last Modified: Mon, 10 Feb 2025 19:30:53 GMT  
		Size: 47.7 MB (47669546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e55e0b8b34ea5b3ba919ce4a6401eeba17103634f66be3d05c3f942cc693f8`  
		Last Modified: Mon, 10 Feb 2025 20:38:02 GMT  
		Size: 49.2 MB (49194060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1af2e4923ec73802217aa39c7fbdd0e8953953eae0f77bb63bb97912593b1d`  
		Last Modified: Tue, 11 Feb 2025 00:34:17 GMT  
		Size: 209.8 MB (209784647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:58404b32a2c779c041bb18489aef8303be412be1b2425b588428f4ba7e36712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fcd622deca720dd58f5801fdd603956ce80f74f8f171436077730cd4aa9794`

```dockerfile
```

-	Layers:
	-	`sha256:908d52556b7bfd2fc088a950d3ec9f4d9add49791bed555931fbc37b7ee2e96a`  
		Last Modified: Tue, 11 Feb 2025 00:34:12 GMT  
		Size: 4.9 MB (4908489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8558fa689fa7a3a9d5663d3143a8799cf284c4987155c0318ccba4e8f500d6a7`  
		Last Modified: Tue, 11 Feb 2025 00:34:12 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:688ab0752617388c50755343a9af66f9f118cda56ad25bceece7c5b6d03fa1a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708971131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ff67e6157fefe5aab235549319056de6d26f2702170fd34cf956e39cf77873`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 11 Feb 2025 00:31:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:31:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:31:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:18 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:31:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:31:20 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:31:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d888f48b270b91ba422532bc2e36ee2c9009a235d31b933572c98fb2a11778`  
		Last Modified: Tue, 11 Feb 2025 00:31:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6d45a22f500395beb47e2cb7a4dc7f29a1e447ce85797c4159a693df9d9770`  
		Last Modified: Tue, 11 Feb 2025 00:31:55 GMT  
		Size: 394.2 KB (394200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2eb7def73c0a1a86fddb80a5f0af8612df3ca386325278d00fe8f140af191a`  
		Last Modified: Tue, 11 Feb 2025 00:31:54 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a82330af6585f3125be7439bbfa9509bed31588eab7be0e643bc314eec2739`  
		Last Modified: Tue, 11 Feb 2025 00:31:55 GMT  
		Size: 378.8 KB (378773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbda2a06236f1cefae22bfd35cc52b9fd2b3088850004b86e5b73a42f9fd26`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fa0e475cfce3739a734760a24ab96600b94fb059c433743b787dceec2c25b5`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f516a9976d165910d1d4701490e8f1c8b33267600c632a4af5e9359875cc1c`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e32b4aee8d383ee361871904507d36d3c1a5640b2ea482a9649b5ceed66f8e0`  
		Last Modified: Tue, 11 Feb 2025 00:32:05 GMT  
		Size: 207.9 MB (207912795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14af3433982f0f9353873d19a6be00dbcd17b1b09c03cf9a35f516e89134ddcb`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1fea92a8ecd0a149cecebce5f00335d38107f7e29b5b9556ef8715715acb8453
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470904786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d28d754bdf77e87205f59b3968977948e0c91b6cab673bd24dda8c3ba5357e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 11 Feb 2025 00:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:28:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:36 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:28:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:50 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:28:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:28:51 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20b4d605e705d3f47072b7d2766df33099177a0b668693003d19bdf3c6a9340`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc94b17f055ae5d776d17833337cdb19f892b69e078438574804239ee3ea3bb`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 365.0 KB (365034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99216bb37b1d08e1e59de495a3808e5f400e470cb619f68dbcf10f143ab2c714`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8885f460c82d88e3fbc71353191e82c3f11d2a5a5f3f69268a62645771f400dc`  
		Last Modified: Tue, 11 Feb 2025 00:29:23 GMT  
		Size: 312.4 KB (312424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f6b9653fe28ad47ebbd26d417ab788c68f684fdf834da41b0f6672e04df365`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f671062518fe644d4999c69ddc0b72f5ff59f4ff90fb26d4ff88beee1e87dea8`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddecbdb2d2e8c88371cf678d724b8f18bc26f58257cb49d9a76c0c313765c7ed`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8dabbc2b2320f85a5094a57d80cc2e3a116a500cbf6773a5f0276b91a940ec`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 207.8 MB (207834366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146db06c36f6b9da5d3f925c3bc657440df28e0ab03f8a59292dff5fc21cc19a`  
		Last Modified: Tue, 11 Feb 2025 00:29:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:f650c51434d86949e95dfcdb2e1ba26dd45bee63c70f7bd9661135be36f36b64
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330761709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b15634b5d1bceb4fc9d47cf6decc9bb4a12d352bf6e9cb253c1e9b4453eccc1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 11 Feb 2025 00:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:28:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:28:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:51 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:28:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:28:52 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:29:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:29:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d33258ab6e0502e72c64239e0dd5c590bf2a156c632b46d34c8127a39537053`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31153d41017e64952ec3b550f20ddae4febdf7208e9c920eb50966f878ce8b4a`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 353.9 KB (353902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d902c882c8a22b22919fb02bee9661449192ab8bcafc02a3deb447a8579855f7`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c1d9a7f8ffc141b71076daa2443eb2de53d6ae203846992c96ecc9337998f7`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 338.3 KB (338343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d69a662a2194044d3794bcac38bbf0cab7a1e380c515aaa5a5ba4755cc0932`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1aec3a8d316b1c0b1671699bf88a707af5a877273e073bd5f44c2d390aa87a`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0a46b2d5242b131507997b788234f375db8487fb01fade330ae6fbac38fddd`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d98a337c23ed13506117abd3406da9b0627caf5b3d503d0806641b2304d541`  
		Last Modified: Tue, 11 Feb 2025 00:29:44 GMT  
		Size: 207.8 MB (207849350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dece062bf4bbdde052aec51e1c0265e371f08157140cb2846ca5bb6281714aa`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
