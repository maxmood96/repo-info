## `openjdk:25-ea-jdk`

```console
$ docker pull openjdk@sha256:271519cc2eae00ff2ed94b335ab71df083b8251b0b06008b294ca23bf2ca95de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:089037b0c8da9b6cfe8f3d9f370988f4c7611acee5b7e254cc09abebef60e25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310617885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a1042c97f7511e6abce9adf23d6ff37fbebe527465b93f8ac9ff334966294`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Jun 2025 23:22:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 25 Jun 2025 23:22:00 GMT
CMD ["/bin/bash"]
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 28 Jun 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_VERSION=25-ea+29
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='4fcf990db7180589d31e39c0985acb5d19a6992d77c94892636b4035b004dd3f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='565ce268822423c068fb97a832ad2c4add94427561e8e3ce29057fb8ccfbb72e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce631430a40b2548b9ce0b52eab6ed208da9a7030aa14db4f7cc77cdac7cb23b`  
		Last Modified: Mon, 30 Jun 2025 17:29:43 GMT  
		Size: 38.1 MB (38092609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055ee233ac2e1b5ecef49743953859f76178fe094110e9f806e6c67768dc56bb`  
		Last Modified: Mon, 30 Jun 2025 19:05:43 GMT  
		Size: 223.0 MB (223024614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc03035f3935d941e66ab8387fc1824c43e5eb5c34d28e7177b425e529b841e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f07386dd444d40eb6e6608df8d4fb55812bf3dab741df9cdeeb1d84fbb8424`

```dockerfile
```

-	Layers:
	-	`sha256:0e851343bb8158d2432c5c9bc25e74baa609bdb191f2d78e6e035ef0e894772f`  
		Last Modified: Mon, 30 Jun 2025 18:23:27 GMT  
		Size: 3.6 MB (3641308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14acc3dcfab0a182241cbabd514d56d0f387b61999956666c80dbc183bf6e917`  
		Last Modified: Mon, 30 Jun 2025 18:23:28 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1b502e0489bb924a5f1fd44c3ee82cd639f5711e91901fe4190d1b905a709d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307398757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0469fa14c8f66fe9a8bcdc7b92479ef35e6300e0ec5e9c5cea8370c06bde09`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Jun 2025 23:22:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 25 Jun 2025 23:22:52 GMT
CMD ["/bin/bash"]
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 28 Jun 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_VERSION=25-ea+29
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='4fcf990db7180589d31e39c0985acb5d19a6992d77c94892636b4035b004dd3f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='565ce268822423c068fb97a832ad2c4add94427561e8e3ce29057fb8ccfbb72e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8651adb19772f22f50f38bb61855702b5099b0a0045fea8c9db8dcc1cadfea34`  
		Last Modified: Thu, 26 Jun 2025 05:13:18 GMT  
		Size: 48.1 MB (48087180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0ee1c604fdbae17917604a097f1f42ae8abcc22cd62c1260386266d1d6ac8`  
		Last Modified: Thu, 26 Jun 2025 04:43:33 GMT  
		Size: 38.5 MB (38495135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df56d3cb3b0aea333de9cd05c77d0fc6eca11d8d820a0ab086b78f3659db74`  
		Last Modified: Mon, 30 Jun 2025 19:06:15 GMT  
		Size: 220.8 MB (220816442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:bb224ad21a8fbc56ffeb17e973499af14ee79160c84edceb5348f1b3b1aaa230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1916378b11cf56f0213d580debefe040e33dd8bda5932d663f62e6fad87932b3`

```dockerfile
```

-	Layers:
	-	`sha256:223e63fb980c57498c0943a1e898fc4d8bbea5aebdbb90d7829086e5981296b6`  
		Last Modified: Mon, 30 Jun 2025 18:23:33 GMT  
		Size: 3.6 MB (3639070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28830cb0e0432843582ed83545212ff568792f043a6f4eaa4a03b190d40c6674`  
		Last Modified: Mon, 30 Jun 2025 18:23:33 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:acf5f59999512f6ea1c15582061e89cd34d73dfd6a0124a63faeab8c259e056b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695880398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3549407f67fcbd654cdd917d8dfe8d3eea2d9cd48c8387bdc1e020601c72891`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 30 Jun 2025 17:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Jun 2025 17:34:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 30 Jun 2025 17:34:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:24 GMT
ENV JAVA_VERSION=25-ea+29
# Mon, 30 Jun 2025 17:34:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_windows-x64_bin.zip
# Mon, 30 Jun 2025 17:34:25 GMT
ENV JAVA_SHA256=397a0df027bd02d080370a97f2ef38cd9130020afb8e124d86949c681e2cf191
# Mon, 30 Jun 2025 17:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:34:45 GMT
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
	-	`sha256:e5ce60371b30b92ee83806dafb4392b1739cd6221758f36d160e71c49a7d814a`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86940ce2ed1474859f47a4b2a88b2892bc48b925d3807250355a279e86c43012`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 403.5 KB (403485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085b77f73c31521d773d475b17009ca1ef5c319f5f65004cba55d259441e4ea`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b3fc94f1a479a4419b8c4e95e59e9d084df7be6015719487643a9d94c5fa7a`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 384.7 KB (384739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce506488f3dc9ce87228f7c1d2647aebdddf1422e6d24539901c171e2474da2`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b66d1c24189e25845057d8f7bc131298b18506f83d144cc70d605cf701b7c3`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f6efbbc7ec85c8e9d968eb6497091c728ff1ddb089aac46c8df07a09169916`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ab5529f598d3db69e9b5be9a047f8340b58cd1e2da849a2fba28d389d244b`  
		Last Modified: Mon, 30 Jun 2025 18:10:12 GMT  
		Size: 218.9 MB (218910072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820a5ff5b2ed28c0d1e10a685f4047646d2e345c03e9f118383d3a0865335cfd`  
		Last Modified: Mon, 30 Jun 2025 17:38:12 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:0db5592173658059ac8212418d6b49e95e8048ddd55b1a6a2aa2fdabb4fe427b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499852870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc1a0b01ed22478725191ed682e086467bc5237b245acfa4f45f297b8b4d773`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 30 Jun 2025 17:28:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Jun 2025 17:29:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:29:16 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 30 Jun 2025 17:29:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:29:31 GMT
ENV JAVA_VERSION=25-ea+29
# Mon, 30 Jun 2025 17:29:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_windows-x64_bin.zip
# Mon, 30 Jun 2025 17:29:32 GMT
ENV JAVA_SHA256=397a0df027bd02d080370a97f2ef38cd9130020afb8e124d86949c681e2cf191
# Mon, 30 Jun 2025 17:30:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jun 2025 17:30:08 GMT
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
	-	`sha256:83f5646370ce93bff89e19b0e053d19b0676771998bc921ce093ef81ba02ff29`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e86f0ddba952f236fe7c4b5622312bb1af4a20f647e5f645708f41205bd009`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 364.8 KB (364775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bb595908a5e523d7a8843ac8b3bca7788efb7732aaac11f1f0d8bd373161f8`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172bf25c02c37fe71e113a7c23ff94c0bafe4c285681a23184713c267016bc63`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 353.3 KB (353300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78381352d741350acb5d2b2698270523332b84d8d8a9e3a67ae1e31af368319b`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a7c1910a636cfe7998456062a411789c8b9095501457507b8d775a9b214f6d`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a62fd6ba7b66d5e1cc59607882bc0e68576820fd1fcf2fdacef6d9d38b1e1a9`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cad975ac93c746ecfded08245e6a41f7a767146d441d2e58f3e652468e28588`  
		Last Modified: Mon, 30 Jun 2025 17:36:41 GMT  
		Size: 218.9 MB (218875499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceccb0d301174cb6e5951fa4eb7d5572dc12e012fe3ff7ea34b9c18a84572e1`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
