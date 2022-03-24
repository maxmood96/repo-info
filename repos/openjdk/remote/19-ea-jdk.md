## `openjdk:19-ea-jdk`

```console
$ docker pull openjdk@sha256:e031868fa331b60f4dc1dfd543a8fc52855b49ba7debe4a1bb1d59a44ceb725c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `openjdk:19-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:f66e9723eab0072d5903e277d78d15834c063ad95e2a40d289c093ad85e2aacd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248729071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bc5c350476f5c743035c3e2f9bafa2b838bdc2734c12c5124216bc7fe5d448`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 01:39:10 GMT
ADD file:c0f0a367bc612431ac9286b506fef5505e0b5f3969515486d8052ec381524261 in / 
# Thu, 24 Mar 2022 01:39:10 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 01:59:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 24 Mar 2022 01:59:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 24 Mar 2022 01:59:04 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 01:59:04 GMT
ENV LANG=C.UTF-8
# Thu, 24 Mar 2022 01:59:04 GMT
ENV JAVA_VERSION=19-ea+14
# Thu, 24 Mar 2022 01:59:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 24 Mar 2022 01:59:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9d3d14d30b79ab021a558da3520be505bd2c5ab0f4c85aa07a3ed43524cea2f`  
		Last Modified: Thu, 24 Mar 2022 01:40:02 GMT  
		Size: 42.1 MB (42111482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8d91aae4872bdf5c523549a1c38e887a3d031b5f174e2e3686d0eca9415dca`  
		Last Modified: Thu, 24 Mar 2022 02:06:25 GMT  
		Size: 13.5 MB (13531708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9567c074f36b342dd1b5cd0d032a4a031e155339503d80c6f31802326e52f15`  
		Last Modified: Thu, 24 Mar 2022 02:06:38 GMT  
		Size: 193.1 MB (193085881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:833f1f10323ae449b0dcbf93f014913b9b7ff1c774c3edef68a739997f5c5a01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248432424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1939228642b59dce771ac05a69c6da7a58888ac7260b3509c46cc1ffcab3efdb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 04:46:53 GMT
ADD file:9674a82df5b1239197195a2f3626b6e5eab1f7c671cdf25578626e3eb6692f53 in / 
# Thu, 24 Mar 2022 04:46:53 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 10:16:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 24 Mar 2022 10:16:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 24 Mar 2022 10:16:50 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 10:16:51 GMT
ENV LANG=C.UTF-8
# Thu, 24 Mar 2022 10:16:52 GMT
ENV JAVA_VERSION=19-ea+14
# Thu, 24 Mar 2022 10:17:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 24 Mar 2022 10:17:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:443da1826734425262e1c8e7c345e160e645bcdffe66214c9b5584e7cefb32ae`  
		Last Modified: Thu, 24 Mar 2022 04:47:52 GMT  
		Size: 42.0 MB (42018766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5d141b87233a64529bec2cbc772163de08d7c37a9cb96e374ee921c3e827aa`  
		Last Modified: Thu, 24 Mar 2022 10:29:56 GMT  
		Size: 14.3 MB (14293983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d02fda17ac7c7d1bae16e1bdfeea41d519e9c2a5d2812ba1bab2292b49495ea`  
		Last Modified: Thu, 24 Mar 2022 10:30:11 GMT  
		Size: 192.1 MB (192119675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk` - windows version 10.0.20348.587; amd64

```console
$ docker pull openjdk@sha256:8804a78205d70d7191ab7c3676ff9e422b49b0aa680227ff4c619af0b035c1eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410705286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7709aed1e68a0a4ffc9d23c10598973115fd1805371505bcd823bf063877e812`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 17:08:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Mar 2022 17:08:44 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:09:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 22 Mar 2022 01:14:39 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 01:14:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_windows-x64_bin.zip
# Tue, 22 Mar 2022 01:14:41 GMT
ENV JAVA_SHA256=1149da64d70afbb171b3426eb55763f697a2f9c7db54ab62adcdd1935f7f5643
# Tue, 22 Mar 2022 01:15:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 22 Mar 2022 01:15:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536e5c64699fc55f528fe9ed2ca2c4088a1b329a50236ef20b400958daadc725`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 600.0 KB (600021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242a279bb38e5c0949759b401e7be86d7f899c9457fba0eeabdef0fec92f6682`  
		Last Modified: Wed, 09 Mar 2022 17:40:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f4c6cacc278c66995aee924b612b9af7a269c23ba83a9f7d62e975c98e167f`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 510.3 KB (510254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a13a2cbfb77c65d598a066caf4efb496566b286c783163242b05e815c36e7be`  
		Last Modified: Tue, 22 Mar 2022 03:19:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935ca362df46ea65dc82bbc40dfd2e72c6b0beed022d8030ce2043b97a83c436`  
		Last Modified: Tue, 22 Mar 2022 03:19:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0c041c13a700cb04f8f00693f4e2d8eb37eb2a33db4f0781b0a70b5ee3cfac`  
		Last Modified: Tue, 22 Mar 2022 03:19:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0901f4f60c5bc3514f2184d96d7895551fc4588d5b65a278cf46382442216e`  
		Last Modified: Tue, 22 Mar 2022 03:23:00 GMT  
		Size: 188.3 MB (188339487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fcdea0bf470701b807e017a56f7d444de74bc7910cf75ca2fc2a179f81a789`  
		Last Modified: Tue, 22 Mar 2022 03:19:33 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:dd699b5508eb9364b6beda28eaec9ab0af5a315de768cf6963df9d73bbc7ba54
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2904275839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93260d7825f5536e95191186c796002220d5fc234721a6dafc8b9946f1c2a68e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 17:11:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Mar 2022 17:11:04 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:11:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 22 Mar 2022 01:15:44 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 01:15:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_windows-x64_bin.zip
# Tue, 22 Mar 2022 01:15:45 GMT
ENV JAVA_SHA256=1149da64d70afbb171b3426eb55763f697a2f9c7db54ab62adcdd1935f7f5643
# Tue, 22 Mar 2022 01:17:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 22 Mar 2022 01:17:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082ea46951b109a477871d3f8739d105427abdbef68b50e54b54b4ed440f48e8`  
		Last Modified: Wed, 09 Mar 2022 17:41:38 GMT  
		Size: 356.5 KB (356505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c303714362d4354175bfbd60bde4487fb5663326536432755fabbeca5237db`  
		Last Modified: Wed, 09 Mar 2022 17:41:37 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ced75f82f0e7f243af02f1c1abe1b9baafcfd9b31f208d60f85f675e0fb5c1`  
		Last Modified: Wed, 09 Mar 2022 17:41:37 GMT  
		Size: 310.2 KB (310174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f83a5774439f25805248676b4326f55e2d002cf24041d9c3fdb767fa64bace1`  
		Last Modified: Tue, 22 Mar 2022 03:23:20 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9604764378852d91ae977d2308289c268de323ae5508d58f4d3a01249ce1a9d6`  
		Last Modified: Tue, 22 Mar 2022 03:23:20 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd0c7b42d858dd32e4cfc063a506310f71e7c3601d47054eb25e34ed5ef25a6`  
		Last Modified: Tue, 22 Mar 2022 03:23:20 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378a36cb600fdb15affc539b8fd5699ea54a3e4886f93da5aef17d7266267614`  
		Last Modified: Tue, 22 Mar 2022 03:26:36 GMT  
		Size: 188.1 MB (188148131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99096316162ddc0ad5d5379c105561a020381f2f6bc45fa47b51fb6e9665b5b6`  
		Last Modified: Tue, 22 Mar 2022 03:23:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
