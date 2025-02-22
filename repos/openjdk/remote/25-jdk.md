## `openjdk:25-jdk`

```console
$ docker pull openjdk@sha256:18b198697c1f6d79c47a4408b7cebe9f27d6557092140344d56901489b20644f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:6ab7221dbdc0bf53fba6d170e652681f32846cd297924cd060a39d8895476b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309672154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa16e6b11460d5fdcec124558de0f4475628ba0c371d58fd18e0adc01cddb1c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:38:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:38:59 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Fri, 14 Feb 2025 23:29:27 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cada48f8581eadeb3200817f6b344fc706ec21061a69d0ecfe8f7c0762cef5`  
		Last Modified: Sat, 22 Feb 2025 00:29:52 GMT  
		Size: 48.8 MB (48768376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e5e7a275506d722ef17d9931a63ec2164798f12a7a5923e020174b4d85080d`  
		Last Modified: Sat, 22 Feb 2025 00:29:54 GMT  
		Size: 211.8 MB (211812887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:76fb20a1bbe6345057e7a7620c34988d181c8e8c4057c2c93d3057294b3629e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35082f5bd85f581561987d4c726fa68d2478c81c2e8a7708d139746c8a1e7b79`

```dockerfile
```

-	Layers:
	-	`sha256:afd2b8d5ec1c3c523b18b288ac140c377d71d09e5839f8ecf43f66e6492d1989`  
		Last Modified: Sat, 22 Feb 2025 00:29:52 GMT  
		Size: 4.9 MB (4910767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e77481c56760af145c5c667f61c85f1e8486908d60e767aad5a649e6a074548`  
		Last Modified: Sat, 22 Feb 2025 00:29:52 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:78a0bd4d69fc9384cb01643cf179aef1941de85924f7138d4284bf3d0d6e45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306648128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35508456100572075b1b9f06b3d9ecf00f7b41f887c2980a26c311d6297dc18b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:39:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:39:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 06:45:29 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca163d5e019bf3d8fffa833ce86f630b0f296399ec45fe5da979a5e604b2e20`  
		Last Modified: Sat, 15 Feb 2025 11:34:54 GMT  
		Size: 49.2 MB (49187884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308e335b711e69fb95f2f620a9d8770e4392ee6e70ec17112f70aeba1e5288bd`  
		Last Modified: Sat, 15 Feb 2025 11:34:58 GMT  
		Size: 209.8 MB (209791029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f072da4d93aa6888c7e1e913f204f3dacc77c9e1b7ecb792c1300317372ce3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d2b3f97ec921b7d6a5794485fed3361cdb383d041193d2a53c5439718343a8`

```dockerfile
```

-	Layers:
	-	`sha256:e676754ed3332494aa9bd6e1b523b5d16551b8fed603c1315a413c222003018b`  
		Last Modified: Sat, 15 Feb 2025 11:34:53 GMT  
		Size: 4.9 MB (4908529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7696914a3a2122c91b9e2eeacfce3223ebeb52ddf8024fc2f28912ad8800255c`  
		Last Modified: Sat, 15 Feb 2025 11:34:53 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:29148395fcc22e96558eb5b2b34815728e6fade263d8a544b5b8c1a83e900ea5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709052943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8de973d5de62ddc042b2050f71f748c168d25992bf47f06eb62c4c2e29afd9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:32 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 00:31:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:39 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 00:31:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_windows-x64_bin.zip
# Sat, 22 Feb 2025 00:31:40 GMT
ENV JAVA_SHA256=7db003a6e122cc08ddd88b60142284f2461efe69b7007138277f55c2b4cf1d4a
# Sat, 22 Feb 2025 00:31:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ddd2d7a81fc53d954a9dd2d0c34b6dc11de32b78f776de50f9b8d3612777b`  
		Last Modified: Sat, 22 Feb 2025 00:32:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ccffd1373b539222b7f4bbfc6083f3e1847112d8175dd9bcf6d2f1d5e7e399`  
		Last Modified: Sat, 22 Feb 2025 00:32:04 GMT  
		Size: 401.1 KB (401147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab598190fdc93227bcd60de240df753030cb05380822e60fa0878c2acb361f70`  
		Last Modified: Sat, 22 Feb 2025 00:32:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8cee35d5dc36789c3c29ff11a43d366bfdf5a263426f8d89ccc05ad7132c6b`  
		Last Modified: Sat, 22 Feb 2025 00:32:03 GMT  
		Size: 377.5 KB (377458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c93e9bbcbcca94aba03552457f79655d9423967d17b5825b54bf288c5fcba`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb3840e2336439da3190de915e1bf68a3719c90b08c86ef6a4ce8d79c32ebd`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef1732e979389c8693edc405d9d91bdf37cadcf8669c1543287c9493f124f23`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68567142facd3ae450b9798fdacc53083f6e9e6cb4dcaceb9c778f0f61e716ef`  
		Last Modified: Sat, 22 Feb 2025 00:32:15 GMT  
		Size: 208.0 MB (207988864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed0205b8d202632969b54b4f3d3c6e78043f5da7954ed95f2df333427f7661`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:2403ea720741867eecabfa68f2ef392dc04373949dcf4a841b42c1e27e6aa131
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472590100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa9191bbd4eeb51743ca0593fd0783b6d9e4bcee367da9dabace4b008d45f9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:35:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:36:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:36:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 00:36:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:36:15 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 00:36:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_windows-x64_bin.zip
# Sat, 22 Feb 2025 00:36:17 GMT
ENV JAVA_SHA256=7db003a6e122cc08ddd88b60142284f2461efe69b7007138277f55c2b4cf1d4a
# Sat, 22 Feb 2025 00:36:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:36:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45bc8c9cbb25c116eef37c13b8ade4fbcb56e7293f7f535233a54ddda954039`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c309c47c6bc31a5f1b9c065524af9814a298e66b9e0cdd3284ac8d86b84046e`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 390.1 KB (390084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e3388eb33e18d864906803dd1b20c573a91916f3d823de8887fe279639464`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dbaf8bcae22d8dcf369d0ea0f18f67bf03df045cecfc662beb8b1358e16f75`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 368.4 KB (368430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420cba2a981f01e3a4aecb389649d23d5d09f9baebbb6ec4b5f3a2ceab5c5309`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f84f220a5f57aae7b3c8b8011603cc54d5ebaf2ea0a20494bb02414a1e0ecd`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015b2546805846ff63a2c28502c0d01fc8c9136d009c6a33a97d21cff1caa53a`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820497b72c0c22f4340b02bb837adbafa993517e1a397c00c34d91ed51e7f2db`  
		Last Modified: Sat, 22 Feb 2025 00:36:52 GMT  
		Size: 208.0 MB (207965878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39ea1cf6fdc4bb9c23a836d29942bcd2b5ae1d6fd89c198f344dd52d4610e2f`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:b0044cb58ee10d3a29ae6308fffd8e8a72fe7bde1ff24af349fbe15fb6732802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345488805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340b18ef1db8f1cb1b983667c00f0acd19d9b87c8df459d1d67ffe8ce6832bf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:30:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 00:31:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:17 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 00:31:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_windows-x64_bin.zip
# Sat, 22 Feb 2025 00:31:18 GMT
ENV JAVA_SHA256=7db003a6e122cc08ddd88b60142284f2461efe69b7007138277f55c2b4cf1d4a
# Sat, 22 Feb 2025 00:31:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f50f6cbe3865f5c184d4ff2f5e9cf2093782b74aee23e6dee59fc855c4370f`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fae8f29d1211bc98369b5b304ceb2cd8b3f6c577f51abdfd892e652b7c8d670`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 334.1 KB (334091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9735253bb27cb86172a025e8832d097e76e61ff6d5b0162917b94dd3bbecc5a7`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86283bb64395f3a921d08d687f1c2058371dd9ee7735230feea87b280620889`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 322.6 KB (322623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2051c5c4267e597d26e97c3e209b90e77b1c7f8545a01140a982eaab0ad3183`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3317a4fc74fc17152cb42a5c6ede2d09d0bc18b9139b42d3d625c84377e35ec`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3153b53bb02f5ddbf36767449a154f140c5a3cc4aea674e9baa5f8aa43d828f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f520d901b1489840f82c899ad0aeb80a4101c5e5f578dc6f911d92ca38385e5`  
		Last Modified: Sat, 22 Feb 2025 00:31:56 GMT  
		Size: 207.9 MB (207915459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e41c8a4199a949e0dd5dbd9269c1684ddd3aa36566dc32b560f55ee0fb3b89`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
