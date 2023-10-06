## `openjdk:22-ea-jdk`

```console
$ docker pull openjdk@sha256:79b7d864b7de8898f5403f92da7a6cfbf9bc83421f6d6873c897fec6676d1489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `openjdk:22-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:d88f3ffa0e6ffe5a3c05aed8fe18da27060dff69d6dfb69ccfe63805af9ac0e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265102390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3e922d72ffe8909f22531dacee24ff465e80cb74723ce7373aec8db6a4e69`
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
# Fri, 06 Oct 2023 20:13:06 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 20:13:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='07830a4cc21745464a68057e8c441e98d4cd673cd02348e9791d9eafe9f3d0df'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='03432a54970a3005c521d34b44a2438ac28f8fe150bf686e28cea6ea9b2a002e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Oct 2023 20:13:18 GMT
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
	-	`sha256:68687f5629d99f7020b33d1872b1c1ade9dfe5c5975b857e5c0a4689a78cb170`  
		Last Modified: Fri, 06 Oct 2023 20:15:40 GMT  
		Size: 205.1 MB (205111764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:14964fd319464864ad4967db765e48d9b93d3bd44240696c7b298f99236df249
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262746619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621dabffc2832d1ca4b9d597f77f5ede9d8cfc4c0fdaf90b26e0051c200afef9`
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
# Fri, 06 Oct 2023 20:22:42 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 20:22:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='07830a4cc21745464a68057e8c441e98d4cd673cd02348e9791d9eafe9f3d0df'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='03432a54970a3005c521d34b44a2438ac28f8fe150bf686e28cea6ea9b2a002e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Oct 2023 20:22:57 GMT
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
	-	`sha256:4e39ea8dbd41ef462bfd1a1bf754507a642280ce0449cb3ee1baffaa1ea50351`  
		Last Modified: Fri, 06 Oct 2023 20:25:16 GMT  
		Size: 203.4 MB (203396242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk` - windows version 10.0.20348.1970; amd64

```console
$ docker pull openjdk@sha256:21ead4c37600f78c748dbe4da4a4c42d55fc4dd2cc7a0ccc672b36ef36d51a20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037437444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca550af4ef2ea638c7f86174dfd2f1b31678e8fdaef59fde38821ee751ec6dc`
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
# Fri, 06 Oct 2023 19:22:40 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 19:22:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_windows-x64_bin.zip
# Fri, 06 Oct 2023 19:22:41 GMT
ENV JAVA_SHA256=9514da1d60086946d1324cfabda5280213d7243eec44e2268bbbf02248d910ff
# Fri, 06 Oct 2023 19:23:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Oct 2023 19:23:30 GMT
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
	-	`sha256:5183453d52f48d4566cca8c148af7c366e9f49319e6ada23452c88d89c393cf8`  
		Last Modified: Fri, 06 Oct 2023 19:26:56 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d35f0b838e4b4ebce3404ba5519e64397f22c6a0ef5f5502c6fd119df58882`  
		Last Modified: Fri, 06 Oct 2023 19:26:55 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1826af811d247dd1a729717f715141f1fea0068cb427655fefdcb42995acd3`  
		Last Modified: Fri, 06 Oct 2023 19:26:56 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7790dad9e18b808741f949055a5374d537d0b0ba722b0cd439557aa595929d10`  
		Last Modified: Fri, 06 Oct 2023 19:27:13 GMT  
		Size: 199.4 MB (199417252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572bb338c95cd876a95d56b0d43ee49245d63e4d650c0f8a910abda858bd3797`  
		Last Modified: Fri, 06 Oct 2023 19:26:55 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk` - windows version 10.0.17763.4851; amd64

```console
$ docker pull openjdk@sha256:6c991eef6547d7c9a985262798fa1d4f1578b05a3a004b61e856434b38db8bca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216366855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f9d52f5c7a367373113f14d9f53c7208c8c2a53e1d3ace6dc0420b56acc9f4`
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
# Fri, 06 Oct 2023 19:23:42 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 19:23:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_windows-x64_bin.zip
# Fri, 06 Oct 2023 19:23:43 GMT
ENV JAVA_SHA256=9514da1d60086946d1324cfabda5280213d7243eec44e2268bbbf02248d910ff
# Fri, 06 Oct 2023 19:25:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Oct 2023 19:25:18 GMT
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
	-	`sha256:546e19438720ca5be9cc6f6ca12dd43dbd0ee51e3d956fa050684eea20145129`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1df7a8549db58b678cf0dffe7a47dbf7e0cc16219d70b61bd646b668aea8be`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0955a80e4c5c94da0b6a3a76fc08e78ae0edd17619653dcac0a5ccbb7b9fbb70`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d90a92e8079e54a9e719807c15fc68d3dcd25cb14c07f21234d870e29be38d`  
		Last Modified: Fri, 06 Oct 2023 19:27:53 GMT  
		Size: 199.6 MB (199556397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659ccf3fd0e7f326819a4feeb79c55112e329af41c1d6d004b1dc0039e08827f`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
