## `openjdk:23-ea-jdk`

```console
$ docker pull openjdk@sha256:43ab18aa2af6001a165a1ad2c285e14aeb972a1776dfa8cb6a70bae0e4c3c030
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a91fa7c462d2f40d2d2ecb1847299b1a9916ba63ab5ae789ed007f3845424876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269452309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6eb171e5566e9df27a667b50cf966b26c61ee54b63cc9f8e97020b4c1043a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc634b2317bcc3caefcafd559ad94a4361088bd5e230a54d9aa3a931d25bdf`  
		Last Modified: Fri, 02 Feb 2024 22:53:53 GMT  
		Size: 15.0 MB (14991013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c50d1c8bc70fb5f164eacc2463bc46978ffb9a92340566127f79aa8e939367`  
		Last Modified: Fri, 02 Feb 2024 22:53:57 GMT  
		Size: 203.1 MB (203139565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c4332137326a5956f97574a2eb2fe83a1acf63d44d2391a7de704022ab92ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af73f58a10fac1fcc0fae308049fa04e5b97f85c1fe3c80a1a819662e1b186fa`

```dockerfile
```

-	Layers:
	-	`sha256:412ea4f4ef8d735ece738a9782df1734e734ee871685c84d371ae9515faeecec`  
		Last Modified: Fri, 02 Feb 2024 22:53:53 GMT  
		Size: 1.9 MB (1915850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5aa34878e33c2d6ed8876d803a4535e8d0da16d4e4f7080d164a5274a87695`  
		Last Modified: Fri, 02 Feb 2024 22:53:52 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:faf7d7338932bc09e70435693d9bacbc2a057e1656ba83f4e2eeba952ac5cdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266793097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6b75056451ed01c93d88f490ccbf75ba40cec5b824dee95f71faefb253dd64`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbecf34c8e1a9b9949041e4c9e805d7ee8c1f00ad6362349a4579d6db495c27`  
		Last Modified: Thu, 18 Jan 2024 10:42:33 GMT  
		Size: 15.7 MB (15702213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b063dde595b109bd2fdffeef4360385896a8ae35e9260c7e81825476b792a4`  
		Last Modified: Sat, 27 Jan 2024 09:23:00 GMT  
		Size: 201.0 MB (201016306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f8703804c1cc247b2bd3dc45e0d6a0900cf706a0a51258cb14c3667aa69d6bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534e9008d112fad7cf30d4b7b335605e415ea9e06b6e74b1245368d902315f6`

```dockerfile
```

-	Layers:
	-	`sha256:6b02fc1ff04250183a71819bd4aaf1a673bc55b0409d3316e9dac5b5a8572cd5`  
		Last Modified: Sat, 27 Jan 2024 09:22:50 GMT  
		Size: 1.9 MB (1914421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46be7bb1f68444192af8b9ffbdf453d3576ff87aba8cbca01832ad3bb17f6693`  
		Last Modified: Sat, 27 Jan 2024 09:22:49 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:e7b6a39a5a84e9c2c9014ca3ec1543e9bec1059f62da72ef777f940ca1dbbc79
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2099006972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3579cec9944ec1ad676c78d0f9e0698ba984b8e00400f88325348039a6c601`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Fri, 02 Feb 2024 22:53:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Feb 2024 22:54:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:54:19 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 02 Feb 2024 22:54:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:54:30 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 22:54:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_windows-x64_bin.zip
# Fri, 02 Feb 2024 22:54:33 GMT
ENV JAVA_SHA256=3bf12bda8aa3d293ed14f6956bd24e598c395e3267be4b58191e542ec7d3479a
# Fri, 02 Feb 2024 22:55:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:55:06 GMT
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
	-	`sha256:0c1c5110a50fe5035f85965fa8f289cefe664b5620395ab917cb90497b76b0f4`  
		Last Modified: Fri, 02 Feb 2024 22:55:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e908fa89d5ef8f77887d0e27a735ad7fc7c1e959086510fa444e405f5ede13b6`  
		Last Modified: Fri, 02 Feb 2024 22:55:14 GMT  
		Size: 506.3 KB (506304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b32740c05a43c95f0a253452d7307a4905a33baca62574a3e3cbe619268ce49`  
		Last Modified: Fri, 02 Feb 2024 22:55:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41772f02cd0c2a51480e8d28c694f8833001c493bf20fbb555dcba1602fec691`  
		Last Modified: Fri, 02 Feb 2024 22:55:14 GMT  
		Size: 359.5 KB (359488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be259a15c08909dce7773edb6e9794bf03df9896813e2830ed480a7164beb5e3`  
		Last Modified: Fri, 02 Feb 2024 22:55:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d16a24a38f721ad643315564b354452dcf232b9a31b184398f266fa5f23d76`  
		Last Modified: Fri, 02 Feb 2024 22:55:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a947cb4fbd2ed6f9312288659abbcd70362abd519d31a548c1cfface56b8d34`  
		Last Modified: Fri, 02 Feb 2024 22:55:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5334dbfca0e3292ba165ae90a5d7fdc043bbac9f3f90a361c39aebf726a14`  
		Last Modified: Fri, 02 Feb 2024 22:55:22 GMT  
		Size: 197.9 MB (197920796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca036b879186e3d7f5ed0fa31f5010a82b3b4760052a85e16776897d5c8e181e`  
		Last Modified: Fri, 02 Feb 2024 22:55:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-jdk` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:aa9112b627416c208f7bd1c50e2ae9788cbb51fe8fc3bac3023957092b5a1002
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268438189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705b661ff948f5470b06612365c84b8f9b8a7bdb39c48602f3224ab282e6b2a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 02 Feb 2024 22:53:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Feb 2024 22:55:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:55:16 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 02 Feb 2024 22:55:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:55:40 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 22:55:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_windows-x64_bin.zip
# Fri, 02 Feb 2024 22:55:41 GMT
ENV JAVA_SHA256=3bf12bda8aa3d293ed14f6956bd24e598c395e3267be4b58191e542ec7d3479a
# Fri, 02 Feb 2024 22:56:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:56:29 GMT
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
	-	`sha256:92019e8fe92b9023266e5e0fc6ba5fbf5d7a9b0c1cc350c307a24f7ee21cf947`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58ec9969fec076e47997c8b1be3c40e7be2f54cc7b61d59e0a412c2e07cb875`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 483.1 KB (483114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60c2a9412548b52abaad522595d6fd351787d6be2b972d9094023051b62d43b`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc300143138a1ca844bbf0b743828afde1ef05a6ab3fecc4d95bd9e8ced709`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 329.9 KB (329915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d84323f82b24f8587e552eee960975bca6ea8ca346346c1ce309a9806409a0`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c668f733ff1b3309ad9d783ecb0d01225879a3765dfe89c98448bb956b01d98`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09f301fcf5b89cc0f889a1bd26b85241018f8f53b479f2b00820d263c2db3a3`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9479a33a8af6082432feacea259738f62e87dedf5259fd74b34744ca7ee2f9f0`  
		Last Modified: Fri, 02 Feb 2024 22:56:42 GMT  
		Size: 197.9 MB (197894872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65c4800a8aeb986b5fe19cc6d65e3d18c8dbbd457ad5da3da38789bc6b9f436`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
