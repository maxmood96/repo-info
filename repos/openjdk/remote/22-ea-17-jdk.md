## `openjdk:22-ea-17-jdk`

```console
$ docker pull openjdk@sha256:e6a72e27013e7e07f0c84411bb01795a2a54112988384bdbaafb93e6b0bb69c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `openjdk:22-ea-17-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:3c74b9066c34f3f2682e9a4ed517603abd2ed4064e3457639f04fb15a63b78de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265066978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d4d5729d13a46212b6c4bb426ac704eda6688457d649203eac5aca871dcf9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:55:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:55:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Thu, 21 Sep 2023 23:55:47 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 23:55:47 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 01:28:22 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:28:34 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:28:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab4e2287a59db00ae2d401e107a120e21ac3a291b097faffb1af38a1bc773c`  
		Last Modified: Thu, 21 Sep 2023 23:57:32 GMT  
		Size: 15.0 MB (15031479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e4994e1d4b81a4a34fc9b26ddf652e560c70d4777a60bc1853d4e4e011869`  
		Last Modified: Tue, 03 Oct 2023 01:31:08 GMT  
		Size: 205.1 MB (205076352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-17-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c1e403293e083c17074b1bd6285aaf08a7527ddd175ac1ef88b3e55f688034bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262738923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a8390fa097a94d71f37f44b2bbee4ddb84ad1e7df82fb01b08c4bee05db0f6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Fri, 22 Sep 2023 00:02:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 22 Sep 2023 00:02:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Sep 2023 00:02:00 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 00:02:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 01:32:45 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:32:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:33:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5f8d4b6eb464428f46a11bf9639aada6dca4156bdef2cbe73cb3f2d805f96c`  
		Last Modified: Fri, 22 Sep 2023 00:04:18 GMT  
		Size: 15.7 MB (15692651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d345319f6887e24146618b7509916cbf21808ff05179fb00604e9c1ca595f5`  
		Last Modified: Tue, 03 Oct 2023 01:35:15 GMT  
		Size: 203.4 MB (203388546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-17-jdk` - windows version 10.0.20348.1970; amd64

```console
$ docker pull openjdk@sha256:f8add9ce60dc57178a985aec024d132b3062631f79bb89a60d0b49c384849495
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037429391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a26c339ef6302a8787cdaa4a3fdd4fd628c4edf5731ef1995eb54ae86586f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 01 Sep 2023 00:43:48 GMT
RUN Install update 10.0.20348.1970
# Wed, 13 Sep 2023 01:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 05:14:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Sep 2023 05:14:16 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Sep 2023 05:14:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 03 Oct 2023 01:31:35 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:31:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_windows-x64_bin.zip
# Tue, 03 Oct 2023 01:31:36 GMT
ENV JAVA_SHA256=74da8d5884f315e4443456f215e71219b4208fa9a970ac75bb49ebc0331867f7
# Tue, 03 Oct 2023 01:32:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 03 Oct 2023 01:32:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feca8e06011ab171ad74cda49c7c305e791965aef283d5b7c2b987dd5388e6c7`  
		Last Modified: Tue, 12 Sep 2023 18:24:42 GMT  
		Size: 448.7 MB (448675362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f40969dbf1e035a6c49e7c40b216960e3ee98ec3b76f76f9fe4498d0110bee`  
		Last Modified: Wed, 13 Sep 2023 02:15:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b411249ef1c74d6763984f0b9b085ac311c6e49aba35a7dbbc1d42264a11ba`  
		Last Modified: Wed, 13 Sep 2023 05:25:31 GMT  
		Size: 462.9 KB (462878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d5d90c5ae40ed0401706ba6915059213a0cc520cc862f8fdbff4e582cbc835`  
		Last Modified: Wed, 13 Sep 2023 05:25:31 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84e7bb658094bff788d92f8ca930570e83805ce31d072d4c675acbef78b62b`  
		Last Modified: Wed, 13 Sep 2023 05:25:31 GMT  
		Size: 274.9 KB (274889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39267ac3ccc09ba6dcd24a7ce2cfe615f21f9ef52636b2ab0c61a575284a8fe`  
		Last Modified: Tue, 03 Oct 2023 01:35:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b729afeb9b91af7d2477ffffa02e12349e08b349f1bb94dc0eaf63207d2f67`  
		Last Modified: Tue, 03 Oct 2023 01:35:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2c62eb1754b73ceccd7163c122827de1bbda67d8ea50b3d91c515b8fc79492`  
		Last Modified: Tue, 03 Oct 2023 01:35:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc576c822ab145244d874f75bee3e76fb643a7b107fd6f2ce890fe68b3c8c03`  
		Last Modified: Tue, 03 Oct 2023 01:36:14 GMT  
		Size: 199.4 MB (199409099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf0c1ac44e11df79c19b82815466e7e71f87439c066889591b46ebec31e7b7`  
		Last Modified: Tue, 03 Oct 2023 01:35:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-17-jdk` - windows version 10.0.17763.4851; amd64

```console
$ docker pull openjdk@sha256:8c6867e21d59f21d73e9d1dab2c0a125ffa5b3eaa536e139e0675d214c08a2d6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216363023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516a0657bd9d253d829d05b79fae0549b77bdbc5c730f722b5081945b821e4ed`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 05:16:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Sep 2023 05:16:38 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Sep 2023 05:17:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 03 Oct 2023 01:32:48 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:32:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_windows-x64_bin.zip
# Tue, 03 Oct 2023 01:32:49 GMT
ENV JAVA_SHA256=74da8d5884f315e4443456f215e71219b4208fa9a970ac75bb49ebc0331867f7
# Tue, 03 Oct 2023 01:34:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 03 Oct 2023 01:34:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da151b70a7f82a6d6963a3317229ba06177114b9d44cd362e90207d42aa4d828`  
		Last Modified: Wed, 13 Sep 2023 05:26:10 GMT  
		Size: 255.5 KB (255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f8ba7984984551020a40f5b8881b3c1fb035e9785ba3bdbae07f7c770a4f6d`  
		Last Modified: Wed, 13 Sep 2023 05:26:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e0c6f3841f682fcfe5bcc0fb248fac7844337b14dd92db7132434ac8133685`  
		Last Modified: Wed, 13 Sep 2023 05:26:09 GMT  
		Size: 216.8 KB (216765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ba225834bd9a70d5a70c98ed7d7190a182e254002b1804cb5e80bfe48873a7`  
		Last Modified: Tue, 03 Oct 2023 01:36:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5f4ce1434857eda3a06bebf7984b6edeb6fb07e9449c90419265e9e093ff27`  
		Last Modified: Tue, 03 Oct 2023 01:36:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6133487700b45f5becac2b16107ec33d4aaa16bf42a2bcee3ba955a8fccb0080`  
		Last Modified: Tue, 03 Oct 2023 01:36:34 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af340185b4ece7e9cb5f04c2bb1d67d653fc010012ad65a721cb3d15e00897ef`  
		Last Modified: Tue, 03 Oct 2023 01:36:55 GMT  
		Size: 199.6 MB (199552403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e33cdfea661d27602ed12adaa329d3243c4ce140634c82a23736e32d8b0560`  
		Last Modified: Tue, 03 Oct 2023 01:36:34 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
