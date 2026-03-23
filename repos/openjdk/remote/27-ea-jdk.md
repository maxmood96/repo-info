## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:c1eb1f404aa0c4219b11e46d07c5e02ae526df0522b681a9e137fff2a1ec787c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:4c37a837a65589a336ace24f8733a1fb87f4299356feea039f540442b0a24f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309176023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3fad46629398254c865da08d4e74e872b01de0a1c6601f3cec4505283a9f4a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:14:40 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:14:40 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 17:58:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 23 Mar 2026 17:58:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 23 Mar 2026 17:58:15 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:15 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:15 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b98cc56637e4fa1749005c0e126912a1b56aaacc09ce33acbc53f090ab5577df`  
		Last Modified: Fri, 20 Mar 2026 00:14:50 GMT  
		Size: 43.1 MB (43050023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8ac8ba5fa4edd11f2fc63a4a43df4e29a46cdafe49311d0c1c698f80214fc5`  
		Last Modified: Mon, 23 Mar 2026 17:58:36 GMT  
		Size: 37.7 MB (37656003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84ea033de0bed3c8fd8ef42b2b72e3ae64f2b11924baf4d952263014dbbfeaf`  
		Last Modified: Mon, 23 Mar 2026 17:58:42 GMT  
		Size: 228.5 MB (228469997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:be56120e4b3daed16b37c9ff246ec1d1721ec3bded747316d07871e6bddbf408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0c6c6e59765015fb517019cb81ab21d8ec8f04e979c00030fb1333527cd6e`

```dockerfile
```

-	Layers:
	-	`sha256:f4af94e979ec3688285f719e9159226e6b7524e6b42ece2f766cb6788586cb08`  
		Last Modified: Mon, 23 Mar 2026 17:58:35 GMT  
		Size: 2.4 MB (2368335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9c6a0f9f005f83f2394bd20d62813f922bb5e7da15912240afc8197e85086d`  
		Last Modified: Mon, 23 Mar 2026 17:58:35 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f66bb377e26854fb6a37faf18c91fe3dfb3e3347d6866ec0a21c58e84855039b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305576852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25f02b074b7cdf0cee5aa6604a0dc8f3fe90a68318fd44118b331855e7afd6e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:38 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:38 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 17:57:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 23 Mar 2026 17:58:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 23 Mar 2026 17:58:10 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:10 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:10 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0341f6c98c0ded39ac1fd938e19b49e5d1980b5cf0e44b058cbbaac4f81336be`  
		Last Modified: Fri, 20 Mar 2026 00:12:48 GMT  
		Size: 41.5 MB (41455727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fe5779896c3eb1b6d3e846d83e4aab19460999fb5696defab0276d7c283f93`  
		Last Modified: Mon, 23 Mar 2026 17:58:32 GMT  
		Size: 37.7 MB (37679719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4abf4d42372f8099e7a70e47982223a2968d5fe2a95f549afe579e6865bfc3c`  
		Last Modified: Mon, 23 Mar 2026 17:58:36 GMT  
		Size: 226.4 MB (226441406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:0269474f634b9b21e6d9ac1b5178f55a9ca55a88075331c674e978d84575a590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7f70703fa2451ff8f3b8be9cdd7b095d8d5d4d6a5023c271099658d672d297`

```dockerfile
```

-	Layers:
	-	`sha256:659a9e4031d1c0c4ce21dbf17fd214015fcac61896a228b32a515fe1009a0420`  
		Last Modified: Mon, 23 Mar 2026 17:58:31 GMT  
		Size: 2.4 MB (2367863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e9d3a00a402d3f27d1a3c305bba65d42d29b2a498748f6495015985416d123`  
		Last Modified: Mon, 23 Mar 2026 17:58:31 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:3760d5261532ac45f98b7a94e43a57a6cace6c267974f4217605d178175a2402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306787858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712d3ca60d5bb8d2d994e6ab67596c306db94417ff673114d52f9c5e78226b75`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 23 Mar 2026 17:59:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2026 18:00:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:00:20 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 18:00:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:00:27 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 18:00:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_windows-x64_bin.zip
# Mon, 23 Mar 2026 18:00:29 GMT
ENV JAVA_SHA256=036103af3a6b6a7fb78955d438f100e620132a28640df5277dd69e8678a924a5
# Mon, 23 Mar 2026 18:00:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:00:59 GMT
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
	-	`sha256:3d965dd410e3195b9ae57caf4f1c339e13a22baf8f46191f070f943dc14aa66f`  
		Last Modified: Mon, 23 Mar 2026 18:01:06 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091abd0bee8579150e2a66dc763d1226bb48d8fe4779f411027f54ebd320ac8a`  
		Last Modified: Mon, 23 Mar 2026 18:01:06 GMT  
		Size: 403.9 KB (403875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbe3771ce949f77e8d85416219d1ddc6f8b25bcf431aaa259e5eac24f135296`  
		Last Modified: Mon, 23 Mar 2026 18:01:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5dbfa0b1c6d05c5c2d5612a095e1f9e04579ad630ca79b441ae5b4e09953db`  
		Last Modified: Mon, 23 Mar 2026 18:01:06 GMT  
		Size: 385.3 KB (385341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364088be8a50446eb4ac1eb3dac1e98be63efe912c8f012a82e15d795b8d9a81`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70f0466cf371da550758f7e6f5442dea965406b4f180439bdc54b023d49d1c4`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a06caa864b0c79cca2719bbdbfb548efd2eea63f64c5246a56ccc0ec7810e6`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aa6acc09d5b2852ca57f66ba97eb72cc4aef9a4113a7266e89e141695d3f2e`  
		Last Modified: Mon, 23 Mar 2026 18:01:37 GMT  
		Size: 224.8 MB (224794734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58e8a04d0fafe12399768a744ebc1560e6e028635a06fcd2b63a5b7674adad8`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:dfd43e0ea001df8280569c9fdb26891ccba845e3905974e95d561ff996303b4e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207912078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b21859f72b107d29c32a5bdad732657b448f6fe8e20b6d6d3d27dcf4d807d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 23 Mar 2026 18:21:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2026 18:22:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:22:22 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 18:22:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:22:31 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 18:22:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_windows-x64_bin.zip
# Mon, 23 Mar 2026 18:22:32 GMT
ENV JAVA_SHA256=036103af3a6b6a7fb78955d438f100e620132a28640df5277dd69e8678a924a5
# Mon, 23 Mar 2026 18:23:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:23:41 GMT
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
	-	`sha256:a5e70bdc88dd20cec2da9e31448ebb1ef7e1cae0295119642e4c9b963bff73d9`  
		Last Modified: Mon, 23 Mar 2026 18:23:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d67259ed24f89a0a4aebc56c8a2ea60f124af392f46d71d282f42191e08d0`  
		Last Modified: Mon, 23 Mar 2026 18:23:53 GMT  
		Size: 505.2 KB (505249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba144e8d8da234e91983e03b3083fa516b6e60f6389dbcc8cec0ceec61281b4`  
		Last Modified: Mon, 23 Mar 2026 18:23:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca10d54bd002a2f8739e979f174281036c7e88ecd45fdd222c80de2a54064a4`  
		Last Modified: Mon, 23 Mar 2026 18:23:52 GMT  
		Size: 345.3 KB (345310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcba2fa6db45de5dcb1424dd4d82069c5f59a62a43eb52649319f236e27805ce`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c73186d90f627106e2fd69251dbbe9ed9a1620d20e7ec7a66c92a58bb6b4311`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec9bce3698367ea02c6b137e2988ba352d670037abc27328fe964c108fcbf98`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e3ba7b530164e099c41e8722c4461962d9d54caa01549933df8773894b88ad`  
		Last Modified: Mon, 23 Mar 2026 18:24:06 GMT  
		Size: 224.8 MB (224772256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56f16b7a64d76621414703b64a64e3f130ad99f095bad86cf7b539a881459bb`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
