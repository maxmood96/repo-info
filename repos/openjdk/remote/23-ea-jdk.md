## `openjdk:23-ea-jdk`

```console
$ docker pull openjdk@sha256:b535d3fc2f2885bc03a6db8f038254905a58f4a5077edf9d49f0b3a1d1822cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:98cf64d706845d928540cc01a1db7656010b41eace830d6ad62412139c87320d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296766378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d8e4045837982a129377c0a91c4cb9c237d0e6054e8d057798c47ad348705e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 18:48:15 GMT
ADD file:95cf7039855dd392d2faa5bb16415fdb79680afe50aecf7c299b8b2dd377328e in / 
# Thu, 09 May 2024 18:48:15 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fcbdc4090331ae224779b095ccebf7fa4fd896fb807b7d6bdb37776132e9710f`  
		Last Modified: Thu, 09 May 2024 22:31:50 GMT  
		Size: 49.0 MB (48998671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2a314d9887d1e4006fd4fb544fb1fbfd091992a79adf007b72460fa5ed7b13`  
		Last Modified: Fri, 10 May 2024 00:51:56 GMT  
		Size: 37.9 MB (37862337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a6b3472b2139ed2b1edfe18a7222a85ce7ecca167e82ea290701a6f3636f9`  
		Last Modified: Fri, 10 May 2024 00:52:00 GMT  
		Size: 209.9 MB (209905370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:d3f35ff7d7a0beac1671cf742600a8d52cb1c3ee765c2236a555ad65f15cf0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ad10db1cfc9a9b5af3f2f944e883ed66ba1d6d8b259189ce5bb7f58d2a7b89`

```dockerfile
```

-	Layers:
	-	`sha256:4a6caa97271757286b65e94afd43e23f26b719f88a9fd37007dd4f2c1c92829f`  
		Last Modified: Fri, 10 May 2024 00:51:56 GMT  
		Size: 3.3 MB (3333220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd2eecbfa451374dde47fe91d1f717d12c6fc6c7f8f2fca9d1f4a792af7cf98`  
		Last Modified: Fri, 10 May 2024 00:51:56 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e0244c35f97e1b6a73722347e2de17b40b3eeddc243ea7e5e0d99bc06792a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293701170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d8bfec162c1fc4a53e2898605aab031d2cbc45eff11b00d1c14c02223abfc5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 18:48:15 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Thu, 09 May 2024 18:48:15 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a4be78b09aad15f916c85a97d9c9410e09e7e9b619c370b687ef5f9e20a44d`  
		Last Modified: Thu, 09 May 2024 23:52:47 GMT  
		Size: 38.3 MB (38259792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e16324649ff2078771a0c4462393a30105723fa51d90ce9fef72725b1c19ba`  
		Last Modified: Fri, 10 May 2024 01:13:47 GMT  
		Size: 207.8 MB (207787578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:c58d455ad155b111b5f17127be582667a6a8dfb0852c5d76422047699b9a7c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d2b2c847ff5babc9aeec86852580d82bcc6f14cfada32d25bba7ec3f634425`

```dockerfile
```

-	Layers:
	-	`sha256:7b872bed7a7fe783a55891443a095bda9d8c36086dd4b8b338aa40ad902b861a`  
		Last Modified: Fri, 10 May 2024 01:13:38 GMT  
		Size: 3.3 MB (3331418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cb15adf6ff03ba4b31939ea60e9e5f71c1e90eca427772b7191f2463eafadd`  
		Last Modified: Fri, 10 May 2024 01:13:37 GMT  
		Size: 19.8 KB (19764 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - windows version 10.0.20348.2461; amd64

```console
$ docker pull openjdk@sha256:b8e396abc1b364aa7b7067c82011e1e1a52675f4751a6f10c2fbe7d4fbcf71f6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318151043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0589174154ed5dc6482db25f0ea4e057f47a7ebad87c241dc21131a336d23c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:00:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:00:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 May 2024 22:00:27 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 May 2024 22:00:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 15 May 2024 22:00:33 GMT
ENV JAVA_VERSION=23-ea+22
# Wed, 15 May 2024 22:00:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_windows-x64_bin.zip
# Wed, 15 May 2024 22:00:35 GMT
ENV JAVA_SHA256=a849b0c4f58cb28b02e6c43660886859ce8678d18224b4038ad69c1e3ead6249
# Wed, 15 May 2024 22:00:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 15 May 2024 22:00:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b25e2aa5b0f0eed7caa2bccb0bf82f1fe9cdfb7143a210314b5de0b3afc6b2`  
		Last Modified: Wed, 15 May 2024 22:01:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd625612b5cf9281af127ce591158439b4f678aa2d91784c126443b5081d514`  
		Last Modified: Wed, 15 May 2024 22:01:03 GMT  
		Size: 359.2 KB (359208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaee157c9d897ff5dc3dc66edc620bbaca6cb104f622c026fb290e44b7201cd`  
		Last Modified: Wed, 15 May 2024 22:01:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749adcef71c1519cfd2925fdabddff609e3e930ffe50d505ac13c3c37e94fcab`  
		Last Modified: Wed, 15 May 2024 22:01:03 GMT  
		Size: 342.7 KB (342659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3edc6a76496fd042367259aebc95676ecf0fa7d2e4dda2f0d50ff254597a807`  
		Last Modified: Wed, 15 May 2024 22:01:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc576ca03f454200c1da3874811c6e25feb42cb8c3cf555fe03949980034fbdf`  
		Last Modified: Wed, 15 May 2024 22:01:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea8479107a79477f93a5aadf13b6132a124a724dc9bcab9134145458aad4f0b`  
		Last Modified: Wed, 15 May 2024 22:01:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715208dab702d7172c6c56c193659f2a36915f9834d918549536d85bfa5035dd`  
		Last Modified: Wed, 15 May 2024 22:01:12 GMT  
		Size: 204.8 MB (204770067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5a21fda36dce738b3dcb4d3ebb9a29b085a3f169d10c42bbe025163ae3d58d`  
		Last Modified: Wed, 15 May 2024 22:01:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-jdk` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:f8cd02c69f7add5da53b3a2c473fc913e1a3274ac5225d10b7edf0806fe5e981
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385347745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de223529e44c80f84cc59ba15f77d5b46374130570184af962394b0eaeae0968`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 May 2024 21:53:01 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 May 2024 21:53:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 15 May 2024 21:53:31 GMT
ENV JAVA_VERSION=23-ea+22
# Wed, 15 May 2024 21:53:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_windows-x64_bin.zip
# Wed, 15 May 2024 21:53:32 GMT
ENV JAVA_SHA256=a849b0c4f58cb28b02e6c43660886859ce8678d18224b4038ad69c1e3ead6249
# Wed, 15 May 2024 21:54:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 15 May 2024 21:54:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44618fd5a605c180c336d69509daf8d91a62393cf845d717e4ede61b994e0be9`  
		Last Modified: Wed, 15 May 2024 21:54:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c42adb3890d0a7bd1d39037e5df9ab87f7b98dfa3bee68f35b5f66eb66ced4`  
		Last Modified: Wed, 15 May 2024 21:54:32 GMT  
		Size: 490.6 KB (490628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fc127618fa27b988d349870c872cf96a1c9386ea3389066bd1f17238436026`  
		Last Modified: Wed, 15 May 2024 21:54:32 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38777da71a7f080075ea4c07fd6be08dd8c33ad800a0d3b52462a44f7649e6b`  
		Last Modified: Wed, 15 May 2024 21:54:32 GMT  
		Size: 346.2 KB (346191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7395ded8b493063ca2906b809cf58a570b57f36e80dee7a17470db7b9ba63aca`  
		Last Modified: Wed, 15 May 2024 21:54:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930248ef0cb13e84eadf0a192207da3cd58cc8be4d9bf7940d95f2e02995a590`  
		Last Modified: Wed, 15 May 2024 21:54:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ff29df2a6ae145c5271ded1c9155beda456550ac944c658f9c5276f25d8fc1`  
		Last Modified: Wed, 15 May 2024 21:54:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8262af7bf3ee17f1c51c8d9792ec3a55946f76a3055311a3adf44f7c00a1f4`  
		Last Modified: Wed, 15 May 2024 21:54:41 GMT  
		Size: 204.8 MB (204791706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320a1a5bd9f7c73d80781729911fedc8f4b53dfea6619e60d5e093b9bc3ef391`  
		Last Modified: Wed, 15 May 2024 21:54:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
