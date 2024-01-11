## `openjdk:22-jdk`

```console
$ docker pull openjdk@sha256:13171db03c9c96d30ab021ebded77d543b19018697a30d014d0ab939627423dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:0cd1201c3127b67e0ce6ed701a5b5b1a9cc41094a33899df0c2f27bcd4e7f131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269069182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f9e66430c848698c16ed7f22c532e41c92f5c32cb8e706a15807cf5d27c879`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:50 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
# Wed, 20 Dec 2023 22:40:51 GMT
CMD ["/bin/bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404fa60e90b20bfc31e712d3a17dc4797c53701a0f3d8c492aa6d5b5760a9ae0`  
		Last Modified: Tue, 09 Jan 2024 00:55:08 GMT  
		Size: 15.0 MB (14995204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15ba8bd89c310846774296e4692795c62666e162d12f88d0071a6dfb359447f`  
		Last Modified: Tue, 09 Jan 2024 00:55:14 GMT  
		Size: 202.8 MB (202750510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:cc503e0221eb9d0c04649678325de74317efe51f67ae11d5622b17106c85aab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3700011656f867b5f6b601d750e65f7aa128cd0d8fbd62b633d280629a86201`

```dockerfile
```

-	Layers:
	-	`sha256:c05cb01d403ed0fd912b8d2197b92d60dc7e37a9c6e1adaae397039624bd33d2`  
		Last Modified: Tue, 09 Jan 2024 00:55:07 GMT  
		Size: 1.9 MB (1915851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8216b33a7c0a6efeae09e4c34f8a84fe2fbd3efeb2d1ac5587431b3099d9f256`  
		Last Modified: Tue, 09 Jan 2024 00:55:07 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:59787d5d8068c7378a819bbc3df3fdc311186061682ce5a739218a5d160482c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266561228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d7a10afd2cd8330c9513e3c84313cea01194a934ebd6eff7070f8efd54e38`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:53:14 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
# Wed, 20 Dec 2023 22:53:15 GMT
CMD ["/bin/bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
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
	-	`sha256:6f9344eface56f983d3996df846576de97223d111287297956250fdbeee45218`  
		Last Modified: Tue, 09 Jan 2024 02:23:07 GMT  
		Size: 200.8 MB (200791473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a0c73be1836798952d54f05a046325b35d0ed4f8f4c2c50ae306cfcb2cc8d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7728130a879c78e09b2982331e8e7132d7e49a0106c23eacba3842908d3a6071`

```dockerfile
```

-	Layers:
	-	`sha256:40ece831d737f9fd56df8eb3267fc95b67fa186a019b710954632701011bf2f5`  
		Last Modified: Tue, 09 Jan 2024 02:23:02 GMT  
		Size: 1.9 MB (1914425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0823aee33559b3673417bbc3ed71853b814f153b95fc44342657fca849b3d93a`  
		Last Modified: Tue, 09 Jan 2024 02:23:01 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:7bde41da20e21240a5cf9c91fd881997645421e90f1c693399a638e06a6f45f6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098748709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf57a8eca335754d1d4a59af11860d7fa0e4dac30d0754bfe091cafef1c1812`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:01:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:02:10 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 11 Jan 2024 00:02:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:02:16 GMT
ENV JAVA_VERSION=22-ea+30
# Thu, 11 Jan 2024 00:02:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_windows-x64_bin.zip
# Thu, 11 Jan 2024 00:02:18 GMT
ENV JAVA_SHA256=3714f6cd54b27fcae643df9a1c2a10ae44a9ded4e6a4ede6866067717b70e01c
# Thu, 11 Jan 2024 00:02:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:02:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f5a614a170e540862fa9bbc246c5f620a39d5de7881318ae57b14de491be44`  
		Last Modified: Thu, 11 Jan 2024 00:02:57 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7ba034f1ec11129a3645d4b3bb91b6877a2d50791e8adf32cecc86d5fe7bde`  
		Last Modified: Thu, 11 Jan 2024 00:02:57 GMT  
		Size: 484.6 KB (484624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45db7c187521bbb4bb4e805ade8b99d2f8b394a40514972ef2923dc87f0e41d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100a1c0ab65f6e55945ef2caf5ab09938d755ba7508ee1bd8c301b99231a0b92`  
		Last Modified: Thu, 11 Jan 2024 00:02:57 GMT  
		Size: 337.2 KB (337193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d9942fae12ece51e3c605987ce5564f81c280af2f68218d4740f7d9e9531fc`  
		Last Modified: Thu, 11 Jan 2024 00:02:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a303359f5e1bc1f425a80f3d31a46f2aac48a7b3bf2244111d91a7eca289d86`  
		Last Modified: Thu, 11 Jan 2024 00:02:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec1a25174d85294ab9ac7a44d49751a44d915d3ca614dc2ee7ca4a3cb1f6c81`  
		Last Modified: Thu, 11 Jan 2024 00:02:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00af2a6be0eec3ce7a2f1971bd9408a45ee21417ea6f8d7bd38478060708075f`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 197.7 MB (197706459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44958ce909d669c2f993f14d81b01508d8df8737a1ca5066ece018a2f293e169`  
		Last Modified: Thu, 11 Jan 2024 00:02:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:0bc0cdc0d0aa77c248c224f19b5b065775d24f612bbcedc41a6c1def0f2891ef
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268330302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85632b4d4dcb68bd3fe0ccfc852b3f7cf091f21e0b959b62c7b9f200cbd0f12b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:04:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:05:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:05 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 11 Jan 2024 00:05:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:28 GMT
ENV JAVA_VERSION=22-ea+30
# Thu, 11 Jan 2024 00:05:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_windows-x64_bin.zip
# Thu, 11 Jan 2024 00:05:29 GMT
ENV JAVA_SHA256=3714f6cd54b27fcae643df9a1c2a10ae44a9ded4e6a4ede6866067717b70e01c
# Thu, 11 Jan 2024 00:06:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433a6cb03ec5e8f2a55bbb07639c61e730f6ffcf3d0751f7f73b9f25d74f33`  
		Last Modified: Thu, 11 Jan 2024 00:06:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d74051661fb8014dc80f169c07c26d54a0c56f02f78e1d2263afc11637a79e3`  
		Last Modified: Thu, 11 Jan 2024 00:06:18 GMT  
		Size: 510.9 KB (510950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b26645e9a24ffca30e88ae96823b2f28fc70f3ff5b571dd5d2712a2b13860eb`  
		Last Modified: Thu, 11 Jan 2024 00:06:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12388de77dd7a2e9c1cf0212d8e301e765b690cb672b561a33062b29caab11ac`  
		Last Modified: Thu, 11 Jan 2024 00:06:18 GMT  
		Size: 357.6 KB (357592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e567fe341a02db9ce57836b39737c948686861867936fc18af0ffee4fb0239a`  
		Last Modified: Thu, 11 Jan 2024 00:06:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6722bae78cfdff26bb5cfe11963b15edb057320e5e6f15320480deaa29e41`  
		Last Modified: Thu, 11 Jan 2024 00:06:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377ad9a9e94616af18b4e43f93aa74f3188f0085c850b168ee5b82370117d8`  
		Last Modified: Thu, 11 Jan 2024 00:06:15 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068a20268af6362af16bec52c7c11f238a5fbfc6f829c622279c5ea7ea8a6db`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 197.7 MB (197731479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb20b96423ada2275a841afaa1d5e6347821be6c91730bf5fc386dc37efd807`  
		Last Modified: Thu, 11 Jan 2024 00:06:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
