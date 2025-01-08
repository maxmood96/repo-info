## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:c3e8807dc96ea6c6a984ad114216587b05387a19b0edcf3ab7ede5703dc07639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:8bc4e525c1929b5249aa5c9bdfc55a1b640f4fb571af4509af958b31e7736ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310633907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011d37185def7340179612c944d1148abb1a0da7b341c83d513283a47080bc70`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3d59505e59f7752fb155bd3cfb2597a2969a2674bf6772205f8ef370f0c21b`  
		Last Modified: Mon, 06 Jan 2025 20:28:37 GMT  
		Size: 48.8 MB (48774245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b45f4adc554a3a273730b0ba32e0a600992c82579f08989bc8633351df2c1`  
		Last Modified: Mon, 06 Jan 2025 20:28:39 GMT  
		Size: 212.8 MB (212760960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:c823951ffc56dff5b3b8485638be60e1ae5041c9c2bfba4bfb66804d0f60261c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86c7139dadf2fdc5a561adae4e990c25647a629763604a709688fe0ead74da5`

```dockerfile
```

-	Layers:
	-	`sha256:16a7f61fa0c20a421f7ea4e936d4a6a272687924f6fe8ebfe6a83437e39c1570`  
		Last Modified: Mon, 06 Jan 2025 20:28:36 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d503b273d20cb5877e21c6ad55a84f914f6dcb9007a2e6cd11de88ed363188`  
		Last Modified: Mon, 06 Jan 2025 20:28:36 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0794fd45329c9d19265bac1e26acb0dcd79e98c2a498eb2ed81232675618f175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307578180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85d5c2d470d26915c45a03a11444dc0b67c9180fbb18aef5d14649ec43f6a6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50730d7cdebc9dd971fe547b229ac9b36632531d0634a0903681766460bf2cf8`  
		Last Modified: Tue, 10 Dec 2024 01:26:17 GMT  
		Size: 49.2 MB (49196487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908b77bb4af733fddd6a2a44d87781125169d879a7dc5005c79cb7497bbb5a0e`  
		Last Modified: Mon, 06 Jan 2025 20:33:43 GMT  
		Size: 210.7 MB (210714301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:95d21298fbee671ebd722f6ad2ab10b10c5603f56bbb9667b014f864af3e5541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68e78eea0c16587ec4d24b1dd4621da3d4b6392d4436b4f18fe5ed775dc68ee`

```dockerfile
```

-	Layers:
	-	`sha256:0621227d093da6d409775d9292f31e2cf7f6e5985d760b64b5343aef4a7dfd07`  
		Last Modified: Mon, 06 Jan 2025 20:33:39 GMT  
		Size: 4.9 MB (4905337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:567eed38c322db959d962e9d81b326ed673e43601d3cad638b73e620accd1d69`  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:664fe21f0bda4e53f955a98d61a422fecb2bcbf598b8b02a08390f45520d8955
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463421658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50f391966c9a52fda8b952da1a373b0e722540b2450163b173e4f1d9025634f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Mon, 06 Jan 2025 22:06:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 22:07:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 22:07:00 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 06 Jan 2025 22:07:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 22:07:08 GMT
ENV JAVA_VERSION=24-ea+30
# Mon, 06 Jan 2025 22:07:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_windows-x64_bin.zip
# Mon, 06 Jan 2025 22:07:09 GMT
ENV JAVA_SHA256=d71df74a22fe12237dff1469d7adae9469331d0c68bbb3dc7145af17fd85cc76
# Mon, 06 Jan 2025 22:07:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jan 2025 22:07:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5da787373e799d1f3cab1cdf85af590d5d63ba85767b4c100e2e2a6c39c251c`  
		Last Modified: Mon, 06 Jan 2025 22:07:43 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5848ca1657704a01cd23d79c93bac681fe9b80b3adf2632808a90031bb0a3d29`  
		Last Modified: Mon, 06 Jan 2025 22:07:43 GMT  
		Size: 352.8 KB (352766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf88e41ea70a7a46c9e3e62b0232be091e976e63c4131c72747c9f07e7691eb`  
		Last Modified: Mon, 06 Jan 2025 22:07:43 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c6669e2281270caecebe0891ed98ba68f52cfcada1d98ae5a8d6d1449f8671`  
		Last Modified: Mon, 06 Jan 2025 22:07:43 GMT  
		Size: 339.4 KB (339368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dca2a37a5866146f091a583e456cc671635de2db28d3fbaede8c42b576f6079`  
		Last Modified: Mon, 06 Jan 2025 22:07:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9451359a5f8fe4d3d6d73e6d537314e70faa0399658093a9b0faf13afb34b9d`  
		Last Modified: Mon, 06 Jan 2025 22:07:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46fe1de17487b175b0dc666f2f3ab53bc8f776a0af778b5436e838f5352c548`  
		Last Modified: Mon, 06 Jan 2025 22:07:41 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279d751c11ebb100495914101f776a93df3ee0c1c5116fc8539a84d063ad6dba`  
		Last Modified: Mon, 06 Jan 2025 22:07:52 GMT  
		Size: 208.8 MB (208848205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d99f63891123d6b2dd0e9d68bb081eed83f17a2187fd2f54f09ce778428ad63`  
		Last Modified: Mon, 06 Jan 2025 22:07:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:c9af43f0dc42a4d837bfcb12cb3b9b73846c7e4512717e074c50a41978102307
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223856356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acd5f27592028c0fab7408b3b912caf1ca5107aee0dcd461fb2cc66f73e424a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Mon, 06 Jan 2025 20:27:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 20:28:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 06 Jan 2025 20:28:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:21 GMT
ENV JAVA_VERSION=24-ea+30
# Mon, 06 Jan 2025 20:28:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_windows-x64_bin.zip
# Mon, 06 Jan 2025 20:28:22 GMT
ENV JAVA_SHA256=d71df74a22fe12237dff1469d7adae9469331d0c68bbb3dc7145af17fd85cc76
# Mon, 06 Jan 2025 20:28:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3cd554a84bfc6f86f4eef76ec05b1263552eaf041438095456c955308ef2fd`  
		Last Modified: Mon, 06 Jan 2025 20:29:04 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee3be2e21409d5ce3327950de33dc67479481ce9216e67b0470ebb8012b7b9d`  
		Last Modified: Mon, 06 Jan 2025 20:29:05 GMT  
		Size: 485.6 KB (485616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a7bd5257bf6226d588158326b2f2d376512767a9d7546f45083563f4ab07e2`  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c4a21a51c0840066a2ace5941fd9e09c37bbbd19228e81f2840225f3c3fb8c`  
		Last Modified: Mon, 06 Jan 2025 20:29:04 GMT  
		Size: 343.7 KB (343671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a408c8baef246a55c86f1cadd7bc8a9b4038d378a86e6a3242c8e3cf0683b470`  
		Last Modified: Mon, 06 Jan 2025 20:29:02 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba763abd015fe8169fb1b5c11c235fee06c0e6ecd41d193e16d748f9a4b53d5d`  
		Last Modified: Mon, 06 Jan 2025 20:29:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0979a2c0f9cc607391b8498df1ab50ec9961aa4e2d2475fc7c15967a92c8b6`  
		Last Modified: Mon, 06 Jan 2025 20:29:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44eeb81648e174e77febc4377783413a873655d6fb995be69576e5368a108`  
		Last Modified: Mon, 06 Jan 2025 20:29:17 GMT  
		Size: 208.8 MB (208848928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc830c27ff9a94089936a8e885eabf7c7a5c85d2bbf1ca2b35427e3f0286c218`  
		Last Modified: Mon, 06 Jan 2025 20:29:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
