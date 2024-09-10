## `openjdk:23-jdk`

```console
$ docker pull openjdk@sha256:55da369efa94e6e0c576cdf01cd5034448c849744ba033d6107a7581193749c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `openjdk:23-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:79b3709d6cbf229121678d03417b3b43462f0ce9acd617bedf19091068ad90ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300933262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fae20072d2a12db20f634ae5afd5f7617a68ea594d6c852d22fd962804099eb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1ea9e315646607184654c85696fc0269f0c99b2067585f1dc26e206a13230`  
		Last Modified: Tue, 10 Sep 2024 01:54:58 GMT  
		Size: 40.4 MB (40418005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdea025156ce54480a983c8a9ad7b91e8c6002863e9219f9e73f21478e0fd2d6`  
		Last Modified: Tue, 10 Sep 2024 01:55:02 GMT  
		Size: 211.3 MB (211276005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f82c3e9451a4dce4db6ac50e39738eee20b98178c0cb39b378c821abf1d8f7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14faf4928d334231a9a509865bafa6010862fbc61273d34f6b7496328c39228a`

```dockerfile
```

-	Layers:
	-	`sha256:38403cf5d344931a65db5fa2c3b5b98beeb7b2c25210470973a7e6007d305dbd`  
		Last Modified: Tue, 10 Sep 2024 01:54:57 GMT  
		Size: 3.7 MB (3668559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d69e32f25d55ec253015bbb9ef55cd4fa057bac05c397ad813180a3182a9307`  
		Last Modified: Tue, 10 Sep 2024 01:54:57 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9c7eba130249fa6d19a0b7505f20f88e00f7863b0b4aef05f52a2da1ea89f3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297927301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37c977c525bd5d2a8b9e70466202fd26c162867d28b6f1390bdba9851739dfe`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed6a7145c00ee1c4b91b6b37765e2a7addef2d9b96e12546b2f7aad0a198ae3f`  
		Last Modified: Tue, 10 Sep 2024 05:32:56 GMT  
		Size: 47.9 MB (47913808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb8c247ecf1b88686d212c2f55e0f5ac4d4ba8cde9b5d6f216ca338a07e7b87`  
		Last Modified: Tue, 10 Sep 2024 06:43:07 GMT  
		Size: 40.8 MB (40844369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabeb64a81a518f6c45c47b2d4cf89a152dd5787c7b606789c2113c9d3601040`  
		Last Modified: Tue, 10 Sep 2024 06:45:32 GMT  
		Size: 209.2 MB (209169124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a93d6611d55dedd71249c55b82ad8cadc6d514e026c501a99877d609369b7879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3685198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3cc4db004bcb9173cf6b96766580bce86778aa4bb5073597108b3b84ee7e58`

```dockerfile
```

-	Layers:
	-	`sha256:1cae743d2642c91b5d59475c3b6a2730ddcecbf4e2122eef2b8ff9531d727704`  
		Last Modified: Tue, 10 Sep 2024 06:45:28 GMT  
		Size: 3.7 MB (3666870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156e9be1e9d8fff0e29d6b91297027fc49557268e77ce14bbf3ce48c7ab8a9ff`  
		Last Modified: Tue, 10 Sep 2024 06:45:27 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:9f46fceb723dd2413025751cbc8031937d8a9d6df883d5479bacc8b69a4c2fa0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348914114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2da5167a38918f5c63c3355d06cbb754b626c2f4a350cd1de8f17ed8018ce90`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 21 Aug 2024 21:06:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 Aug 2024 21:06:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 21 Aug 2024 21:06:53 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 21 Aug 2024 21:06:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 21 Aug 2024 21:06:59 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 21:07:00 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_windows-x64_bin.zip
# Wed, 21 Aug 2024 21:07:01 GMT
ENV JAVA_SHA256=cba5013874ba50cae543c86fe6423453816c77281e2751a8a9a633d966f1dc04
# Wed, 21 Aug 2024 21:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 21 Aug 2024 21:07:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133c40c9988134d4353a69f04848c3d6a63789ac61ef72130121fc96e3586ea5`  
		Last Modified: Wed, 21 Aug 2024 21:07:27 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b524431054335de8d88803eace3d4c2b570472472ce95c64c3414e5f8c02e2f`  
		Last Modified: Wed, 21 Aug 2024 21:07:27 GMT  
		Size: 372.5 KB (372497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb5712408797912cdd4bc0e01921914703c2970845885d003914d3d75cfac6e`  
		Last Modified: Wed, 21 Aug 2024 21:07:27 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069d234a3a5af85bec04b1d0e2d54369cbab6a853d64b7d69498ca26f449adaa`  
		Last Modified: Wed, 21 Aug 2024 21:07:27 GMT  
		Size: 351.2 KB (351219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb15a23dc54e1d7deb4bbe8b45f4a5370f91bca76b7f5944ba164083d7f3068`  
		Last Modified: Wed, 21 Aug 2024 21:07:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13c5698e2d8b40916d5679930abaeaaf1e9196e90bfeff65f3e01b55f11e544`  
		Last Modified: Wed, 21 Aug 2024 21:07:25 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84b126d3bfb6ea45ed6ceca88b5779683d135e4bf4e1a5824bc4e5a06bd0d86`  
		Last Modified: Wed, 21 Aug 2024 21:07:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283445077676fc6ed753394b211c3b5780d6abf038f2afb3a0b0f1a130206df1`  
		Last Modified: Wed, 21 Aug 2024 21:07:36 GMT  
		Size: 206.4 MB (206417706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0499f8cdca1d039135b3d02a11d9543249761f7a84d47b65925d44a15c6b054`  
		Last Modified: Wed, 21 Aug 2024 21:07:25 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-jdk` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:61f72997ecdc513c550c6e8eb131f1abda7c61d48631a88c7b0c65e5cd05dee4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452560835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b2e37e982d6a90a3b033c348dcfe38f446a11906bc4513cf10a3c71b3dd813`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 21 Aug 2024 21:03:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 Aug 2024 21:04:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 21 Aug 2024 21:04:58 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 21 Aug 2024 21:05:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 21 Aug 2024 21:05:21 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 21:05:22 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_windows-x64_bin.zip
# Wed, 21 Aug 2024 21:05:22 GMT
ENV JAVA_SHA256=cba5013874ba50cae543c86fe6423453816c77281e2751a8a9a633d966f1dc04
# Wed, 21 Aug 2024 21:06:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 21 Aug 2024 21:06:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a1f8c05aff5339c3078e5af9f5131dfb61d771f271583b9f0405dbaa8fa14d`  
		Last Modified: Wed, 21 Aug 2024 21:06:21 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe53ba924c46155690a49c862eef579fbe426c9687dea5620ed90ac4a1edec65`  
		Last Modified: Wed, 21 Aug 2024 21:06:21 GMT  
		Size: 517.6 KB (517576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8eb622b7869fae3d2ddab6a10c31e6fe3cf28b7ab6d0efa64f524b9490534ba`  
		Last Modified: Wed, 21 Aug 2024 21:06:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16625bb0b178dbf4652d22840baeba641c7011db9460f0e44aa13a2421f67984`  
		Last Modified: Wed, 21 Aug 2024 21:06:21 GMT  
		Size: 371.2 KB (371193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172aacde5c9c7724696bdf2674bb5e1d7f01c287b7ba4cfee1a9bf5fafba0efd`  
		Last Modified: Wed, 21 Aug 2024 21:06:19 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0743deea9d087c2a0d6a8c5c6e367105b8b1b2fa2d8b7bf0c918076ac19801`  
		Last Modified: Wed, 21 Aug 2024 21:06:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70222f998f71140a460ce6d47ce3c827e89a5e7306c27112190737b91447f66e`  
		Last Modified: Wed, 21 Aug 2024 21:06:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546c7f8def80d6a0c3dfee4f1b90f5cce639ed7d0ceb6d903a2ff7cac6a146c7`  
		Last Modified: Wed, 21 Aug 2024 21:06:33 GMT  
		Size: 206.5 MB (206461018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f08cfc27e7ed0e9f977d4d2fe1c971b90f4534cfeae299d39eb02346f123189`  
		Last Modified: Wed, 21 Aug 2024 21:06:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
