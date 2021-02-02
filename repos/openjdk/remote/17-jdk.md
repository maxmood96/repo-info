## `openjdk:17-jdk`

```console
$ docker pull openjdk@sha256:1a78e2b30ab29c39604ffdbfb65eb247a52b4af25ecf96be5e9aee241d9ce5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1697; amd64
	-	windows version 10.0.14393.4169; amd64

### `openjdk:17-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:476c4e09b999ca9eacb30916eee592c60b76722defd7c1c593f39b8586cd08e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240997330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b047dac6bad526bcce5bcd37d86e6d9dfba85ec0a6309b9f5428f022436cce`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:17 GMT
ADD file:2ba8f9c8e1d7e464c075fdd46e81f2e15a69d9a5aefb4b991cccb352e082af2f in / 
# Mon, 01 Feb 2021 20:32:17 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:54:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 23:54:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 23:54:30 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:54:30 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 23:54:30 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 23:55:14 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='0e340613945c78b2eb714ba0850604a1a80a9678ba0e8d81f66629c0ca2c36b1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f3f80fc9b41cfddd89d263ae66c0f514aaeb3db2eadd6c9bf3c31e1b2cdcf44e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 23:55:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63e877180dd1388e46564a2b7a72ddf3559dc506f4b6e8b435ed569643811c02`  
		Last Modified: Mon, 01 Feb 2021 20:34:13 GMT  
		Size: 42.1 MB (42069114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cce05db0e2c91e801a9a4024eedc06badf46bad72a11ee564bbacdbc4cbfb40`  
		Last Modified: Tue, 02 Feb 2021 00:04:16 GMT  
		Size: 13.3 MB (13277751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9608cdf547a7c2a79e6cb7fdacefcf4bc03ca5b49aba92afff7ccf5ff29d71c8`  
		Last Modified: Tue, 02 Feb 2021 00:04:31 GMT  
		Size: 185.7 MB (185650465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fdacd7dda5ebd7559e6b2ea519fa4bdba5c740d914ececbb19da0d3898166196
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236073037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616c2ce0c15b456e772be8cbe42dda4887a9ff8eea30a8387cf48f4c932d8d31`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:00:54 GMT
ADD file:40a46ad11c4530459867a348c980e7ed1ba9fe6bdf74da38208ee8bf7be1f81d in / 
# Mon, 01 Feb 2021 21:00:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:05:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 21:05:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 21:05:58 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:05:59 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 21:06:00 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 21:06:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='0e340613945c78b2eb714ba0850604a1a80a9678ba0e8d81f66629c0ca2c36b1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f3f80fc9b41cfddd89d263ae66c0f514aaeb3db2eadd6c9bf3c31e1b2cdcf44e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:17e75779b55909cd6075d706cc3fc9f838f287de73b35be3d551231217cbd32c`  
		Last Modified: Mon, 01 Feb 2021 21:02:50 GMT  
		Size: 42.0 MB (41996203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fad58a53edbb48f3027bc56f941db82a77fd6d28a6fc25d4bf2462f3bc62bc`  
		Last Modified: Mon, 01 Feb 2021 21:15:35 GMT  
		Size: 14.1 MB (14057108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c971450934d010ca9f87449f240d84945f55545ced545d92e76f8aaec1563cd1`  
		Last Modified: Mon, 01 Feb 2021 21:16:01 GMT  
		Size: 180.0 MB (180019726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:0689d85a1833d5ecb0e82c4aefef6f8c5cb8555ab0b854196f25dc62aceb9784
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2631227717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800d396eb5b6aa7b198ec850b21764f22f2699dfd9cfd263920cee9615afbc62`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Feb 2021 19:15:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:15:47 GMT
ENV JAVA_HOME=C:\openjdk-17
# Mon, 01 Feb 2021 19:16:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:16:06 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 19:16:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_windows-x64_bin.zip
# Mon, 01 Feb 2021 19:16:08 GMT
ENV JAVA_SHA256=7fa795be0deebf36bbf21b5775a7aae0a671642dd431b0b068a9db3e6f8306e0
# Mon, 01 Feb 2021 19:17:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:17:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750be76c45d6cac9367b9122b5847700dbb4c36ccf93eceb4ab0a71c8e815e67`  
		Last Modified: Mon, 01 Feb 2021 19:52:54 GMT  
		Size: 9.4 MB (9385366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662223a8e8b8225632d5378b29c751d503f8dcf00d7c9301a06f2f927752bbc2`  
		Last Modified: Mon, 01 Feb 2021 19:52:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c5e84f5867b1987f252692d77ef0da416f7cc2c16e04642af3e59c1f80fba2`  
		Last Modified: Mon, 01 Feb 2021 19:52:52 GMT  
		Size: 344.1 KB (344056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd43ffbf67d469edaf4838a19afc5bcf55d15f50d1ea73d625d459dd52d8087`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c4230bdffb2703960a924a8d76d972758f2b8514e296ca7ffae3ee2ac5bef8`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e547e9e52fb352b22c558fdbe58c5d8bab5e5534a94f35b761a9267bd77d04`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18315f54cdd154e94d0830dab94bf96112d66eb25a9384587d1c209cac7991c8`  
		Last Modified: Mon, 01 Feb 2021 19:56:24 GMT  
		Size: 185.7 MB (185718187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc098763ea180ca9d4ea731aa78ead7332830728ab56cf3cb16f5209afb44d8`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk` - windows version 10.0.14393.4169; amd64

```console
$ docker pull openjdk@sha256:bffe8fa225fac41db27f2d87fa1f2e0da515c225b300537d0c4a62d6e07ddb86
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6000795032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1179c3aecc97e4f96c8b242b70897229908fbe0feee09e3b250221c16d4ce7de`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Feb 2021 19:18:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:18:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Mon, 01 Feb 2021 19:20:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:20:05 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 19:20:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_windows-x64_bin.zip
# Mon, 01 Feb 2021 19:20:06 GMT
ENV JAVA_SHA256=7fa795be0deebf36bbf21b5775a7aae0a671642dd431b0b068a9db3e6f8306e0
# Mon, 01 Feb 2021 19:22:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:22:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66978b7d55ff893ec83c214709ae41b4b65f437e7e8b19278fc48aaa5804d9a5`  
		Last Modified: Mon, 01 Feb 2021 19:57:01 GMT  
		Size: 10.2 MB (10159693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0292bb01044e6b9c7a671d4265c73c9a1d54aee92863a7b682db8d4778d710b1`  
		Last Modified: Mon, 01 Feb 2021 19:56:49 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff31c24272f760d215fcd442075708726826e6d2697bdce8a3bd97936a8df198`  
		Last Modified: Mon, 01 Feb 2021 19:56:55 GMT  
		Size: 5.6 MB (5611133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7f7b4fcf20faac495ceabbb2a6020e96aa17790e506516a17e32fc854fc29c`  
		Last Modified: Mon, 01 Feb 2021 19:56:46 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269ef76ee9490c0807457e3400c9b11851d2dbf0040abd251e708a83acff9586`  
		Last Modified: Mon, 01 Feb 2021 19:56:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d368c12127fb0b3855f0971679ab9fc49d42d981a6279a38891c6502fcc60`  
		Last Modified: Mon, 01 Feb 2021 19:56:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f70dfa7b6580ad7ae6e411a1141ae5de5d5fe0b7a5de3a26e92c02c35f1bf7`  
		Last Modified: Mon, 01 Feb 2021 19:57:08 GMT  
		Size: 191.1 MB (191121961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486400faddb7ceb6ffdb281acae8fa990a9c9d140096a8330a368120d1835193`  
		Last Modified: Mon, 01 Feb 2021 19:56:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
