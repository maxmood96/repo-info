## `openjdk:26-rc-jdk`

```console
$ docker pull openjdk@sha256:26777815c4f3b369d63b09391ecfb735b5a31ec569d1f9b53422577ba92c99cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:26-rc-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:dd55693886dda9fe5f0878fd19ce2e33881ea7708a180fa5a99b393ad44ea6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313537789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574f5889ef8791cc713690d1e712cfcdd22a4d0f46db394afde46921e104af2c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:12:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:12:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 13 Mar 2026 23:12:36 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 23:12:36 GMT
ENV LANG=C.UTF-8
# Fri, 13 Mar 2026 23:12:36 GMT
ENV JAVA_VERSION=26
# Fri, 13 Mar 2026 23:12:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Mar 2026 23:12:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf71672e4b8b6e263c937c7877c7dfcfca0b6b7b6657877db14fe3b47d7ef1`  
		Last Modified: Fri, 13 Mar 2026 23:12:59 GMT  
		Size: 38.3 MB (38296891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34b8f91864db1429f9ad5e916f79edbf7b29cc9b50abe7e414d5b69e8f9a7de`  
		Last Modified: Fri, 13 Mar 2026 23:13:02 GMT  
		Size: 227.9 MB (227936688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:06d49d654417e80467f544f75ac2c2247657ecae5ad30a7df8734501c266fed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7294218904657dfd26bbf06531f2d07b5225a0de7e90c93605c9631c7d4a2fa8`

```dockerfile
```

-	Layers:
	-	`sha256:c0cd525af32b0ff396c5ce7159dbb632c2882695ffb28e9d9eaca2db07e9f729`  
		Last Modified: Fri, 13 Mar 2026 23:12:57 GMT  
		Size: 3.7 MB (3654123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445968017929f5fb748dc155110ddc9245c7ee1e223c022943bf9a3c7296ee20`  
		Last Modified: Fri, 13 Mar 2026 23:12:57 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1d284bbc3bf9ce802ed77b21824d0a2562d898ec4ec19066e04538f3debcdfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310459850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c8491ff4b731eda09b14e6424a4e14681b25dad45819a0b577b5962cabb70a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:12:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 13 Mar 2026 23:12:07 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 23:12:07 GMT
ENV LANG=C.UTF-8
# Fri, 13 Mar 2026 23:12:07 GMT
ENV JAVA_VERSION=26
# Fri, 13 Mar 2026 23:12:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Mar 2026 23:12:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac32375182e2929693cb1d3af90cc88714117a07ee1304d248a8c8c1d6ccea`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 38.7 MB (38695544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05c2bc90417070dfd08c3ad03d160880899260ef58c473e7a812a9edee2782`  
		Last Modified: Fri, 13 Mar 2026 23:12:34 GMT  
		Size: 225.9 MB (225864120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:2cec99f49f2550fba94e489fa4dd7bcc0a2e355f91b05a1e6f885805cd851203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc9a1ac124539612f1c0cc3cbaddf45e541a3161e0b8ce1ddfea41bd2056e0c`

```dockerfile
```

-	Layers:
	-	`sha256:c3d77b625038a44a4b48af2b20f63e2f07506c1d2c1dde42d8c227cfc5e8fb76`  
		Last Modified: Fri, 13 Mar 2026 23:12:29 GMT  
		Size: 3.7 MB (3651741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b053c02b18d8ec7b17aab8f289e304553f07c1c09e3c56868a0a23ee1355d4fe`  
		Last Modified: Fri, 13 Mar 2026 23:12:29 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:2561d9bdf2cff7e17e2467cb1d4955cc915300b95d00f45e86835a294ad0a930
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306230739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb7d9327a2e96065c1641dbb816ea1d6f32a6221943dc5ad91a7121d14572f5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:57:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:08:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:19 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Mar 2026 22:08:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:25 GMT
ENV JAVA_VERSION=26
# Tue, 10 Mar 2026 22:08:26 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_windows-x64_bin.zip
# Tue, 10 Mar 2026 22:08:27 GMT
ENV JAVA_SHA256=2dd2d92c9374cd49a120fe9d916732840bf6bb9f0e0cc29794917a3c08b99c5f
# Tue, 10 Mar 2026 22:08:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577b380a809fd7aaebdd6a6f0d59a090ff85fbb58921f36c06a704c2d76bade1`  
		Last Modified: Tue, 10 Mar 2026 21:59:21 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0156b576e3f86f67015b3c0b6524b34c8654c1cb0aa722b7bae4deee923477e8`  
		Last Modified: Tue, 10 Mar 2026 22:08:54 GMT  
		Size: 354.6 KB (354650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8ed652983feb31e1e377de8c767bee27f949667d3afd09b3402f77b9f2a285`  
		Last Modified: Tue, 10 Mar 2026 22:08:54 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b81457d6213b580a56c5a0e968d2018a286cba3e4bc5409e1f5c52c1464f448`  
		Last Modified: Tue, 10 Mar 2026 22:08:54 GMT  
		Size: 341.7 KB (341716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfda05b5649db709e92356c4223aafb17d1c2751e65a83c038a9a0fa866feb3`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1a39f11bed4de14f1c9653ef6d31af8213014360bc7da12cc81e4d16c0bca`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd57495802692f632d180dc4605bc6c4d899de2a85884f600a44216ce8be5733`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7505c1be3c4c6627d42475429a95b9ab4e34c051a48802421b24729afd08fb61`  
		Last Modified: Tue, 10 Mar 2026 22:09:08 GMT  
		Size: 224.3 MB (224330498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5821cfd70ef24ca9efb3a59dfaec145a1eef550e0540c2e3142ccd7c2298cc`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-rc-jdk` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:18b941be608cc480f2519df0e05a4aa319337c78d8f27dad0df59355f6ffed3c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207443578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af78a30d336939b18b834ddf15e8535f61de78fda8b9f6a3a9c12e385a05640e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:14:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:14:35 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Mar 2026 22:14:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:14:41 GMT
ENV JAVA_VERSION=26
# Tue, 10 Mar 2026 22:14:42 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_windows-x64_bin.zip
# Tue, 10 Mar 2026 22:14:43 GMT
ENV JAVA_SHA256=2dd2d92c9374cd49a120fe9d916732840bf6bb9f0e0cc29794917a3c08b99c5f
# Tue, 10 Mar 2026 22:15:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:15:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bce865a5fef3c3d366224bb94ee05dc622261950fdd529edc41f69aa86a82`  
		Last Modified: Tue, 10 Mar 2026 21:59:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b29feaa0115655b201b08086e85be930ce940980c84af318b9466074a5914`  
		Last Modified: Tue, 10 Mar 2026 22:15:10 GMT  
		Size: 486.1 KB (486100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afce6bbce6056bd05b4b7350dda6759ad0f4a207289d7831613cd9b723567105`  
		Last Modified: Tue, 10 Mar 2026 22:15:10 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0ed55d8a6263fddba0acb38150bca671a72efbbebaeaf865b5fcbef313da9a`  
		Last Modified: Tue, 10 Mar 2026 22:15:10 GMT  
		Size: 335.0 KB (335015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f6e44e86b9c30c478b5351727e20586febd3bd051f2df3dd76ecfe50192307`  
		Last Modified: Tue, 10 Mar 2026 22:15:08 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7f8692ce45fbc68468fa5aeab8737ecc0f58bdf90c86c53afa7836bdfd54bc`  
		Last Modified: Tue, 10 Mar 2026 22:15:08 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a8ece55d3794e47b16e5be61a47fb4d8221dfa161dff5bfb8f3e16f621084d`  
		Last Modified: Tue, 10 Mar 2026 22:15:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb409f4fee3ef76b36f81fd44e4607164a282d37b06dd4b3452cb337edbc1c8`  
		Last Modified: Tue, 10 Mar 2026 22:15:29 GMT  
		Size: 224.3 MB (224333243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a416dac114a122a697c530067a924608a3eaed6e02ff4cca5656839e22169c`  
		Last Modified: Tue, 10 Mar 2026 22:15:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
