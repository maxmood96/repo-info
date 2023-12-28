## `openjdk:22-ea-29-jdk`

```console
$ docker pull openjdk@sha256:0a5c05730eb236adde80db68c53282e7e62347eddfd71a72660346fd5aad8de6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `openjdk:22-ea-29-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:d913b718c6946ab2b70e9f505b1d97e76522b4fe0bd072b25d3502ff241ec996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269065297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a23a90e3ff3b5a55a71f36bedc105850e8c45e67225a96487af1d53d1cc89a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:50 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
# Wed, 20 Dec 2023 22:40:51 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389fb4b832d27607a7383e0960802239a63b583d8c29daa293fab73421ab3ba`  
		Last Modified: Wed, 27 Dec 2023 21:54:05 GMT  
		Size: 15.0 MB (14995331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664716af15e8070b43e686190dacf8e1adf1ba7be18db9cac2322a993aac3164`  
		Last Modified: Wed, 27 Dec 2023 21:55:58 GMT  
		Size: 202.7 MB (202746498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-29-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:7fee356af6bfa6cec1cd273696e248ace31234404b7597388a159500f608d7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2001dd969c8a06769414c7dcc4b0d28a806009b39dc52619ec261d15ed951601`

```dockerfile
```

-	Layers:
	-	`sha256:8d1c7f297b32118920ab34858f620646371dae58c884da24ac5039b87c105716`  
		Last Modified: Wed, 27 Dec 2023 21:54:04 GMT  
		Size: 1.9 MB (1915851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd82a861e21c3adc1a01818e4047acfcb1f1addc8fcdd9c6546bb0dc752f436`  
		Last Modified: Wed, 27 Dec 2023 21:54:04 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-29-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:feff842fbefc974fcda104f6c0561fc57d483547780dda0922e720722f5d57aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266560512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139d2d28eacc7bc24feabe68a162f3c124f14e7d86fc9c2d1dea5acac87ffa43`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:53:14 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
# Wed, 20 Dec 2023 22:53:15 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f352f0f1de3c800e109fad5b2dae0cb9097249a14ca89d420642f858cc188`  
		Last Modified: Thu, 21 Dec 2023 07:07:40 GMT  
		Size: 15.7 MB (15690041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a21130bc7fa0f0b5ed7e5d41422bfe5af1c331e8cecb4d264993df794985a`  
		Last Modified: Thu, 28 Dec 2023 05:05:04 GMT  
		Size: 200.8 MB (200790757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-29-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f596027c21e4a00423662e52121bda61dc58a30d87e428dbfbbad3753c48880b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bc0980301bb12010e417828157e4543fb61e77cce59c15752f2a05f97f7bed`

```dockerfile
```

-	Layers:
	-	`sha256:8fc727417b9c5e9dea7b03293b8225bc750802e75b4ef99174336a4ae4c2dada`  
		Last Modified: Thu, 28 Dec 2023 05:04:58 GMT  
		Size: 1.9 MB (1914425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b23e23f7bf42dbd94c16de460705fd0891a044ded5adeae34639d9c37e348f`  
		Last Modified: Thu, 28 Dec 2023 05:04:58 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-29-jdk` - windows version 10.0.20348.2159; amd64

```console
$ docker pull openjdk@sha256:c71219ecb8929437572dbbfa8b11ef33da336b7a994fdec7e7a665e0bbad9db1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087834212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8ba2c958e8186aa5855dd2059c6799a4c5f68617d7832b37a1917f586f79ec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Wed, 27 Dec 2023 21:53:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Dec 2023 21:54:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:54:24 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 27 Dec 2023 21:54:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:54:31 GMT
ENV JAVA_VERSION=22-ea+29
# Wed, 27 Dec 2023 21:54:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_windows-x64_bin.zip
# Wed, 27 Dec 2023 21:54:32 GMT
ENV JAVA_SHA256=78ac775c98c21936b976b697605990f73d1b7011e37cc7e2478488a74b2cd247
# Wed, 27 Dec 2023 21:55:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:55:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80ade58e2c5fbafaa925a419ca6ce4b8f8cd0a9a96e57f7455d615f0dc76215`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e28802ba179dfa146caf64698e6c9b933ae4ad531c655ecb6b100d124072518`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 515.9 KB (515925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c10f9b8524da54d2ac52d4ce679135798c2e857be96c19e536276e259a802`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c0e9f85d53663b6bbb6fe4c4dda8f1b527c64ce73a6096d9d5bef2cd39c2c5`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 333.3 KB (333306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82223523acc44a78e539e6ad9b73f6a3be75fef3d521aa98c60aaba363ed46c5`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1613150671b588068ddb255daa6f6f74a8e5f471f352637ca7dbfd796f4f73`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b9861928b62f80af0506b71b12aa78d76c2420e55ac4d64999cbfba37c9ad4`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f36f79adeea9e2f543c321661856a73064369ab96a7ea51794274c40095b8b`  
		Last Modified: Wed, 27 Dec 2023 21:55:16 GMT  
		Size: 197.7 MB (197703628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb43d44649ce1a66d072b27b0c33e87cb152dc2be1d836aa5ca4cf9b7f183ee`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-29-jdk` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:1b1efc6dae3149789aaa5dfaaa4fa14df8e3201312991fbcfc7f1050f79dc48d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258276020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e794e73c68d0d6f8370b2decf9541c3913b9b951ddb92c5d76101ffe64732b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Wed, 27 Dec 2023 21:53:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Dec 2023 21:54:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:54:48 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 27 Dec 2023 21:55:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:55:11 GMT
ENV JAVA_VERSION=22-ea+29
# Wed, 27 Dec 2023 21:55:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_windows-x64_bin.zip
# Wed, 27 Dec 2023 21:55:12 GMT
ENV JAVA_SHA256=78ac775c98c21936b976b697605990f73d1b7011e37cc7e2478488a74b2cd247
# Wed, 27 Dec 2023 21:55:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:55:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821d0b0e2fb48df9f31dcd774f4f7adcb6c69b71cefad58415400ed7ef1c713d`  
		Last Modified: Wed, 27 Dec 2023 21:56:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc9906cbf38c2eb35e10a6f0851b0f59400cc54c7286145fbfe688287ff9f88`  
		Last Modified: Wed, 27 Dec 2023 21:56:07 GMT  
		Size: 499.9 KB (499921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9a2644e173e4475592460d7e2f4de01edb9a09a2c55bc45751e23f00475b3a`  
		Last Modified: Wed, 27 Dec 2023 21:56:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27422bdb0e7ee73d6d2a825bf0545fe4575d3637e63e83a18d5ff075a3082b2d`  
		Last Modified: Wed, 27 Dec 2023 21:56:07 GMT  
		Size: 344.0 KB (344002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae45750ac2c8a1d8fb767e60ecf775621c4de7f80937c3ab81bf6c9cafd9ca9`  
		Last Modified: Wed, 27 Dec 2023 21:56:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6ec707040730b4da66e2ae3308251a8b102dacc0e1ee7c67931fc60068cfe1`  
		Last Modified: Wed, 27 Dec 2023 21:56:05 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b18374e443a9fe7cd3429d72f1bc36de897a6a964f5ea021c270db2b3575954`  
		Last Modified: Wed, 27 Dec 2023 21:56:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996605bc47a1edcf242257c3123db2d0a2141713323bbda668b7da648e3f3363`  
		Last Modified: Wed, 27 Dec 2023 21:56:16 GMT  
		Size: 197.7 MB (197715326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158f8182a9c9ee2b4d694c7c2aebc0b455c0419825643eefbfe61605bd80d911`  
		Last Modified: Wed, 27 Dec 2023 21:56:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
