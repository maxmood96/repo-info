## `openjdk:19-jdk`

```console
$ docker pull openjdk@sha256:89cfbd3019ba0aa7076458d5a29a4b615c607b0edd621cd078705fcb543ef002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `openjdk:19-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:9fa2f3367427a450beafb24ffbf95b996dd987396b3b05c96be810a1bb265d69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248380437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ea58f7c202505a3959bc4f609e60a79aaf7f54b84aad9193ec78033452db8b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:37:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 25 Feb 2022 03:37:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 03:37:26 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 03:37:27 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 19:56:50 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 19:57:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 19:57:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab18c3f6beb4d98c3f94f4e60b6130e29bc5110daaf90f15eb717e0bd61a1cd6`  
		Last Modified: Fri, 25 Feb 2022 05:31:17 GMT  
		Size: 13.5 MB (13503410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25ee18645a07f836a998155887f151649339892e211701d6048c6b7333f467c`  
		Last Modified: Wed, 02 Mar 2022 20:06:49 GMT  
		Size: 193.0 MB (192995747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6c7c535a85e8078cfcfe723e1eaa633e254bd63172356e6512946c399092220c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248288265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8896663f8f13fa38ac9f1e7f036b4d266532215be923ad4dc4dfbcab2111a7f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:25:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 25 Feb 2022 02:25:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 02:25:42 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:25:43 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 08:04:22 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 08:04:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 08:04:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca767a5052236a4d74f577a368b70a4d1d5482f19c0b1c405b8fc19598510e3b`  
		Last Modified: Fri, 25 Feb 2022 02:47:46 GMT  
		Size: 14.3 MB (14304339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d14e9aa25e5c75b4fdefebe953b4f713b8a8c65a9e30ee5050a55077ea0800`  
		Last Modified: Wed, 02 Mar 2022 08:18:10 GMT  
		Size: 192.0 MB (192032064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.20348.524; amd64

```console
$ docker pull openjdk@sha256:be2eca47c7b9fb0afa9a325304317a17868361b4a485ad512d339e042d5aaa0e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404380588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7a677a90cd6a6a42d8c586e1ccfa89ac1a1baf4ab8212120b1a69eeb7caab2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 13:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 18:40:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Feb 2022 18:40:18 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:40:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:16:49 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 01:16:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_windows-x64_bin.zip
# Wed, 02 Mar 2022 01:16:51 GMT
ENV JAVA_SHA256=14d6f94b755321e7d1024aa1038ec0bc89e9ba6568fe250f0368698662ed5220
# Wed, 02 Mar 2022 01:17:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:17:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:898469748ff68223ab87b654b29fb366c1f4f2b7cfad7a37426346ea16db8dfa`  
		Size: 963.2 MB (963225591 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7062696b7aef1ca33afdf32084a532f7e3151a844eb7cb2455bcc907e0f42a58`  
		Last Modified: Wed, 09 Feb 2022 14:28:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc5298c05f3e14d89c86be0ac333bd8cfa150ada3565e9f2736c19d8cac25b`  
		Last Modified: Wed, 09 Feb 2022 19:16:25 GMT  
		Size: 616.4 KB (616433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21971a484cbb6138250125b67d62f83b05a4770a5da18e51e7b3ac8e5743e725`  
		Last Modified: Wed, 09 Feb 2022 19:16:24 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be28f1a2b136367cb8f8044ec174a09f9976e0f389c7fe25cd4e12f2e59b5a`  
		Last Modified: Wed, 09 Feb 2022 19:16:25 GMT  
		Size: 532.5 KB (532549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cadb837ca2aba0402ecf128fc8fc3320d25d8f58d63e3f4600697dd1bb3b02`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ee8a1fc88fe1f7704a1f2dc3f853de23031115c05623de4910730b33f05e6f`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cc3aae3f6778afd5f0229da116f64cfdb90f1f3fd05c74a10c3ba7a1082ba2`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf53a5b545860edb41110306beeba4a923a6b286739bb19cbb5c23a8e853438`  
		Last Modified: Wed, 02 Mar 2022 03:21:27 GMT  
		Size: 188.3 MB (188298478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045bc86d68464728528354abb9d7b47b0cd84d153b6f987736b45f6d1376d4bc`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.17763.2565; amd64

```console
$ docker pull openjdk@sha256:f4859eab7974ad1875e2c38777c1e8ffb3b3fc750d9f135148b85f9b53470edd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2902507983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc36b0a94ab247fb20c39dbc8076d7bc11282896b8be056f3ae23d6635403`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 18:42:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Feb 2022 18:42:46 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:43:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:17:52 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 01:17:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_windows-x64_bin.zip
# Wed, 02 Mar 2022 01:17:54 GMT
ENV JAVA_SHA256=14d6f94b755321e7d1024aa1038ec0bc89e9ba6568fe250f0368698662ed5220
# Wed, 02 Mar 2022 01:19:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:19:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0c1566a9285d9465334dc923e9d6fd93a51b3ef6cb8497efcacbcf64e3b93fc`  
		Last Modified: Wed, 09 Feb 2022 13:26:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b68a1fe6e4f618e81fe842c9b07d5a79ffffc2c21933db69d5c9e6105091560`  
		Last Modified: Wed, 09 Feb 2022 19:20:09 GMT  
		Size: 358.3 KB (358257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08343ea9810774eba7bea5b402b825bbbb597f2cb7dc0b9958270839899f0886`  
		Last Modified: Wed, 09 Feb 2022 19:20:08 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1318a28fd7f970bded95d3db9d726254043dd9127e1055fac6d3909627f9ab10`  
		Last Modified: Wed, 09 Feb 2022 19:20:08 GMT  
		Size: 311.5 KB (311525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec8936d345d913563518e950cd32287b59cf8d69d1644338d2719daa2ecc892`  
		Last Modified: Wed, 02 Mar 2022 03:21:49 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70e6b70dd1e123575a819c6ca077e9c6047e5ec5bc15f1f9878c7b225df4a27`  
		Last Modified: Wed, 02 Mar 2022 03:21:49 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20db5b758d5cbad60f6dc6bce675b707fecfc167c9c63db8deca5e7ae287e7fa`  
		Last Modified: Wed, 02 Mar 2022 03:21:49 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae96e8568b22a9e120bf01b8c0308f5de85726a3a6c3e7bdf9ff5717a26405`  
		Last Modified: Wed, 02 Mar 2022 03:22:09 GMT  
		Size: 188.1 MB (188114915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8b03ddf86dde80aec610bd9310f0bcec9e9cb7dd5dc9b120b8ac8074e5a890`  
		Last Modified: Wed, 02 Mar 2022 03:21:50 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
