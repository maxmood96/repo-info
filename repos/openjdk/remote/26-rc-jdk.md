## `openjdk:26-rc-jdk`

```console
$ docker pull openjdk@sha256:16f09a34238c34cfbc28ac7447d1a6948c803dd8a2720c552cfda47e8a2f1794
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
$ docker pull openjdk@sha256:7297bc0750cde943b19f4e8ccbc0e6b3ca968c608fc5a4d9fd567edbe1a12aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313542163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4be149be6d870ec2d926bddccfaa99cc9f41a847c1a8385aa809694c9924afc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:38:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 19 Feb 2026 19:38:29 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:29 GMT
ENV JAVA_VERSION=26
# Thu, 19 Feb 2026 19:38:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f15c9ff2a00ce61779592faebfb95ed52f9cb90c301b95e02b59d80be6ed56`  
		Last Modified: Thu, 19 Feb 2026 19:38:53 GMT  
		Size: 38.3 MB (38296685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70044eb955e310c1a90e03aba26215ca051dc9800cea2c59a35eb746fa0cd56f`  
		Last Modified: Thu, 19 Feb 2026 19:38:59 GMT  
		Size: 227.9 MB (227936607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:81279e38a9a214f5c6de48bef556ed3909a0e1e8ce6797a17f6a295dceaf2d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c9ea5d1a325e071271c5ac68f900127a6206d905f29e48b278e37972063e7c`

```dockerfile
```

-	Layers:
	-	`sha256:63ea3a9e6d7c2a917de15d61eebb2482e1b7f2fba9fab02989b9a9e424c99d7c`  
		Last Modified: Thu, 19 Feb 2026 19:38:52 GMT  
		Size: 3.7 MB (3654117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb436a74bbbdafe3e865b7509fc31f048d89d07337a5951fb2f16ea06209d0b`  
		Last Modified: Thu, 19 Feb 2026 19:38:51 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08023c7307aae5e22851f24fd85c3d3ee27281f1107d7d83aa70cf3420dc687d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310459546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0e558bcc5bc7ae9e8023fa2423dcca60a857573c97fff726da2592f27b9770`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 19 Feb 2026 19:38:01 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:01 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:01 GMT
ENV JAVA_VERSION=26
# Thu, 19 Feb 2026 19:38:01 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba169c606464ec011ece3abb80fcb27b052386c7535df541d2aa96937b5cdeb`  
		Last Modified: Thu, 19 Feb 2026 19:38:25 GMT  
		Size: 38.7 MB (38693389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0997b4a308402c88eb0b0ffa16502d30e40641d49d28fbfa202fa1f2ce8c8`  
		Last Modified: Thu, 19 Feb 2026 19:38:33 GMT  
		Size: 225.9 MB (225864177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:178a0b82f8ece9098436781c21922ec392a83ac028ea91ef7148efa2af30eb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8366d442a33cf3921c59c2d30e4baab277443933714b3e0cbe270ad734d2e4d7`

```dockerfile
```

-	Layers:
	-	`sha256:ae4ebfd0260ccb2a22ef3c87d3ddd58e6e6c90a9d07a0c05e200348c09b113a8`  
		Last Modified: Thu, 19 Feb 2026 19:38:24 GMT  
		Size: 3.7 MB (3651735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b76eafa9acc79c8568bba963b21f39c855f0bd182eb3dcca9380c2cf638c12`  
		Last Modified: Thu, 19 Feb 2026 19:38:24 GMT  
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
