## `openjdk:15-ea-jdk`

```console
$ docker pull openjdk@sha256:d6b7aa8c0b96929989de58d0ae8bd5434f47e6efa78c60ee9c147ccc946122c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `openjdk:15-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:1cd456e948bbd99d5ed64530bc941e365654071416cb4a66ac2e80571e9b50a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259958202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18650a7b66321cd5d57a2e0631fc07fe4ac73a5aa28e4a2b4ef8bea878d093c1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 17 Jul 2020 02:36:32 GMT
ADD file:0846801b1ef59a7513feb7e2704d8b0c5618da23e28ecff72f64ac14799ee0c1 in / 
# Fri, 17 Jul 2020 02:36:32 GMT
CMD ["/bin/bash"]
# Fri, 17 Jul 2020 02:53:07 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 17 Jul 2020 02:53:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Jul 2020 02:54:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 17 Jul 2020 02:54:21 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:54:21 GMT
ENV JAVA_VERSION=15-ea+32
# Fri, 17 Jul 2020 02:54:57 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-aarch64_bin.tar.gz; 			downloadSha256=9480832ee9344c7e87ab39c4a4c7c1a224a576a9442e0eedfc52bb67acb7788b; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-x64_bin.tar.gz; 			downloadSha256=70521c1fa8a44e3073862fc10bcae2f1c2b688b5ce354734ceb242dd52145c51; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Fri, 17 Jul 2020 02:54:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce8f778fef067eed3d092243c838d674cb1ef39441d85d0ca84382084a69093`  
		Last Modified: Fri, 17 Jul 2020 02:37:13 GMT  
		Size: 48.0 MB (48014772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778faef342036a08101af5d8806ab4f17eda31d2a4e102e33a115bc619bc019`  
		Last Modified: Fri, 17 Jul 2020 02:58:39 GMT  
		Size: 16.2 MB (16187244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e475c2a6f6548708b82ec29032b8b3595e6f031771a79106e0055f75133c90d7`  
		Last Modified: Fri, 17 Jul 2020 02:59:22 GMT  
		Size: 195.8 MB (195756186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eee3b4670277c5eaaa9c38b81e906a410c7194a661aa1928156e640893341e84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239939379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142e8abc4283842d1835822f3b90a9c8ad1c58102abedd223b4ba080e81819b0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 17 Jul 2020 01:45:21 GMT
ADD file:f07cad218c7e24e1cbce662268da25d9318627f636feebb0f669155354c7f365 in / 
# Fri, 17 Jul 2020 01:45:25 GMT
CMD ["/bin/bash"]
# Fri, 17 Jul 2020 02:03:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 17 Jul 2020 02:03:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Jul 2020 02:06:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 17 Jul 2020 02:06:46 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:06:58 GMT
ENV JAVA_VERSION=15-ea+32
# Fri, 17 Jul 2020 02:08:54 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-aarch64_bin.tar.gz; 			downloadSha256=9480832ee9344c7e87ab39c4a4c7c1a224a576a9442e0eedfc52bb67acb7788b; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-x64_bin.tar.gz; 			downloadSha256=70521c1fa8a44e3073862fc10bcae2f1c2b688b5ce354734ceb242dd52145c51; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Fri, 17 Jul 2020 02:10:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5053e285643065e9638a069d53c6f62fd6bf1d6d4d16001d48a66ee024d7397`  
		Last Modified: Fri, 17 Jul 2020 01:45:56 GMT  
		Size: 48.6 MB (48633508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7d1facfda57a46d98e2882cdeac87e1b92ca135e73948039ab5c8e3c1f5598`  
		Last Modified: Fri, 17 Jul 2020 02:13:50 GMT  
		Size: 16.4 MB (16442484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73be7494f9d16d59a037a87a873a291241f736f167755f7f12ebdc98bdda9aed`  
		Last Modified: Fri, 17 Jul 2020 02:16:13 GMT  
		Size: 174.9 MB (174863387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-jdk` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:eb07e262086c8bc620b0128cba38915186cd5a81feac74cb7f2277ebc4f1b9a9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2515695824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc8450f3ad0992e8531d40668f4fe0f9d561c23808fecd7264bb56a78d0e5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 01:45:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 15 Jul 2020 01:56:24 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 15 Jul 2020 01:56:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 16 Jul 2020 23:01:24 GMT
ENV JAVA_VERSION=15-ea+32
# Thu, 16 Jul 2020 23:01:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_windows-x64_bin.zip
# Thu, 16 Jul 2020 23:01:25 GMT
ENV JAVA_SHA256=b6234e651de32b418b6f1b7119761e5b576a2474b937e764ed543b0c73ddb521
# Thu, 16 Jul 2020 23:03:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 16 Jul 2020 23:03:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca5cb7caf11332b67bae426682385af17fa897c718adce9713b111340eb0d71`  
		Last Modified: Wed, 15 Jul 2020 02:42:28 GMT  
		Size: 9.1 MB (9136637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d284b2483b2f168e3ba6ac5972ceaa54db6f335b7cea2a7ba976ec79bceab7`  
		Last Modified: Wed, 15 Jul 2020 02:44:41 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9df741ee75c4cf331249ca7555639e3d621263ed2b077eabfcb7e526e62959`  
		Last Modified: Wed, 15 Jul 2020 02:44:41 GMT  
		Size: 293.0 KB (293037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854f156fe948208d22698346e4948c07faf3849242090cc8bad8f1aa70213339`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265def16c6816003c143432b9310634f9d184fb134a50ef8954390627a76b42e`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b0c42b6c22bda3949c8bb8c3446f180aaf3da1048eb4e85d4b6add5753d082`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531c6f15fe07017e96d7753878366436e7b4bc55550daff431cdaa985f00d5f6`  
		Last Modified: Fri, 17 Jul 2020 00:21:04 GMT  
		Size: 196.1 MB (196067208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024e886f87bb5417e3b02dc021eead5da9630e3312c10a9c87265edfba56eb90`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-jdk` - windows version 10.0.14393.3808; amd64

```console
$ docker pull openjdk@sha256:010710068fa11f0d5af0c1044d70e5fdacb0f7313cd83ff67a786cfb1e64232c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5958313988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ead1e2fea38fd1f190a19be64f3cf3af16d5f201375cb04be3133d029aae48f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Jul 2020 16:57:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 21 Jul 2020 17:16:13 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 21 Jul 2020 17:17:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 21 Jul 2020 17:17:34 GMT
ENV JAVA_VERSION=15-ea+32
# Tue, 21 Jul 2020 17:17:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_windows-x64_bin.zip
# Tue, 21 Jul 2020 17:17:37 GMT
ENV JAVA_SHA256=b6234e651de32b418b6f1b7119761e5b576a2474b937e764ed543b0c73ddb521
# Tue, 21 Jul 2020 17:20:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 21 Jul 2020 17:20:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf5cd76cb63f861b644ea8339d6249d5372f121099524df379003e1bbb30d9`  
		Last Modified: Tue, 21 Jul 2020 17:37:06 GMT  
		Size: 9.9 MB (9859351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edde4f5d2475ddaa914cd8a18292e5416187a1d7599750442f00e50cea3a660`  
		Last Modified: Tue, 21 Jul 2020 17:41:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f135e0cc29026835e3fac8ad10c245c3be829884607063cd668de1eb0a212f7`  
		Last Modified: Tue, 21 Jul 2020 17:41:14 GMT  
		Size: 9.8 MB (9799598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5caf0698d6342a0f59625ee1cba80d2bd4227a2da7c473b7cfe8984e45d92607`  
		Last Modified: Tue, 21 Jul 2020 17:41:08 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b60d5a069ba289be22ae8fcf2e528fd3fdf17bfff0e51821a54471d8e0d03`  
		Last Modified: Tue, 21 Jul 2020 17:41:08 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c4f9c89a8248cb488d5d90d669ffd81227ec7620ab65ae87ce37eaccbb12d0`  
		Last Modified: Tue, 21 Jul 2020 17:41:08 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e60e2027bffb9f61a88581266b6811cd0ddfe2090dd360ea5eacdea7d1149b7`  
		Last Modified: Tue, 21 Jul 2020 17:41:34 GMT  
		Size: 201.2 MB (201186103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fd4f475f6f7d1bcdbd439ce6e1b37654b4fdd5e4ac299bdd1714690221ccd4`  
		Last Modified: Tue, 21 Jul 2020 17:41:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
