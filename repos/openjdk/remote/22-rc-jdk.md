## `openjdk:22-rc-jdk`

```console
$ docker pull openjdk@sha256:756d934dd7a6219fbe6aece7dff79843c8c665229f9d022ab346b4c8ba01102a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `openjdk:22-rc-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:0b8632bb0e96fdc84f8a31a0b6fc2a53d9cc1d44d61395126e6e76f23fbc929e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269099615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b9900d2c523e1a4ccf520e4ca5033ad9510c28389a1c373884da454754a476`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:16 GMT
ADD file:cbc540158e77b85113e3a0e0ed1e202046cf293cdb8d7cd890b04883493dbf35 in / 
# Wed, 14 Feb 2024 01:47:16 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81badc5f380f1ca21f6c430303f4107b9b5e0af27c59e3725bf731915b457fc8`  
		Last Modified: Wed, 14 Feb 2024 01:49:17 GMT  
		Size: 51.3 MB (51325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f943f48ed43ed865465947885a23f9ca429300b7943b988ed9b49fa7a174662b`  
		Last Modified: Sat, 17 Feb 2024 00:53:48 GMT  
		Size: 15.0 MB (15005859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac5e3cca0f313dfd16002062e9f1a6fd48c66b5f3a8cfa5f8ddeb1fa53d9ffa`  
		Last Modified: Sat, 17 Feb 2024 00:53:50 GMT  
		Size: 202.8 MB (202768181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9363795f2671b5aaff1b0ea4bb48c49ab47af88d6b84001bfb1657f0c0d0abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b56c12f0efcf9d6b68075ad59d3e304d3871950b10aadf97490c186bbce1974`

```dockerfile
```

-	Layers:
	-	`sha256:ad65a5868101d1ec11d717facb00ff721dcb10744b12ec2cc5aa9f38295c96c4`  
		Last Modified: Sat, 17 Feb 2024 00:53:47 GMT  
		Size: 2.3 MB (2269266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7570de2503bee0e1cbe45e3a5601d8244cff54a8ba9149011327eabac6a65235`  
		Last Modified: Sat, 17 Feb 2024 00:53:47 GMT  
		Size: 18.0 KB (18025 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d09f2e82055cbdcb4a32d601d15d28149719715ccab05d9283564ea64a7f120d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266588997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83d359d5012e197484fbbdfcd46d9fae1cad90b20681516ff2307858ab0ae4d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b1d3eb6a012567065354e86eb0bac67a32e425e65bc6fe8b5cd84b95a0643`  
		Last Modified: Wed, 14 Feb 2024 11:04:46 GMT  
		Size: 15.7 MB (15691290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30549fa3ddde3809fd2069181de3010bb5522bfb570478076e9722d4e5bc0dad`  
		Last Modified: Sun, 18 Feb 2024 05:21:03 GMT  
		Size: 200.8 MB (200824793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ff63298e889a1ade26cd0275dcab4530f68b134defb150468f729c84a12aec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5543d675ca97f2e4c5704f161bc9cdb6f31518f39de726ef563455b852683d10`

```dockerfile
```

-	Layers:
	-	`sha256:6ba93f9c4f99d00bdc70361b302322c9d91be3fa41e5ff041437feb9647cc49d`  
		Last Modified: Sun, 18 Feb 2024 05:20:58 GMT  
		Size: 2.3 MB (2268682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9fc41f90e6b60830e8d63263312e76253a2350e659d9f49678aa6331619551`  
		Last Modified: Sun, 18 Feb 2024 05:20:58 GMT  
		Size: 17.9 KB (17883 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-jdk` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:99304f54beb2911f46ef15c814dc758ffc0cc197d157f8779c78a5a343638177
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109266661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a9e92c8951cdff88155128659ab9484b8ee8a13153ea9bd58d479afed3ded5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Sat, 17 Feb 2024 01:04:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Feb 2024 01:05:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:05:06 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 17 Feb 2024 01:05:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:05:11 GMT
ENV JAVA_VERSION=22
# Sat, 17 Feb 2024 01:05:12 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_windows-x64_bin.zip
# Sat, 17 Feb 2024 01:05:13 GMT
ENV JAVA_SHA256=8f5138fecb53c08c20abd4fa6812f9400051f3852582a2142ffda0dff73a5824
# Sat, 17 Feb 2024 01:05:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:05:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ff04928a44b4919be4000a2c0fddd267b6ec4c3b8f56a08c9e5b468a75f207`  
		Last Modified: Sat, 17 Feb 2024 01:05:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578ecf76f9c90ad06ea52113b39032941f017a67069a0367002e29047389fb54`  
		Last Modified: Sat, 17 Feb 2024 01:05:37 GMT  
		Size: 504.6 KB (504612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25c56159f6955f2a2c8dcbf16359de1243db653c855d17e3dd81be55d646a1d`  
		Last Modified: Sat, 17 Feb 2024 01:05:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb523523ba6a899a4c8fe89b594f9d180a62dea8eeed7854b14adef43fdda40`  
		Last Modified: Sat, 17 Feb 2024 01:05:37 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c5166e4a5a51629f53f8b390a4981e5ed4ca8f39173bc0c7d7d0a94dc71ac2`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce28c3b7bb76b78a97aef7055963682e0fbdba66b253a0dcb5abd5d6f5d1b75f`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c94c6542f6f18d6a3db285032b9d882e36dae77d9f3df575f43916dbaea28a`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe97c65938d9fc1f520075ee05d8d134716b159c58eda187c375b216c1c5fc69`  
		Last Modified: Sat, 17 Feb 2024 01:05:47 GMT  
		Size: 197.7 MB (197744487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f6d09c31332b3ce9109d02ba79809e4bc54bb9c5a0bcf49c42c5a2cb52637`  
		Last Modified: Sat, 17 Feb 2024 01:05:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-rc-jdk` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:93da8acac2a10f5a5ec5000a1365f28e6fff7fec829d628bbe951c969c95e04f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278988647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9964abfc648ec59ecf313b658120a5fac5523c1e6e41a3b39f55c5ad31b05d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Sat, 17 Feb 2024 01:07:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Feb 2024 01:09:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:09:07 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 17 Feb 2024 01:09:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:09:28 GMT
ENV JAVA_VERSION=22
# Sat, 17 Feb 2024 01:09:28 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_windows-x64_bin.zip
# Sat, 17 Feb 2024 01:09:29 GMT
ENV JAVA_SHA256=8f5138fecb53c08c20abd4fa6812f9400051f3852582a2142ffda0dff73a5824
# Sat, 17 Feb 2024 01:10:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:10:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54741948d684c2cf84f1babf4aedc31ba0ca3dc0d64b7adf3505e59a92f48b62`  
		Last Modified: Sat, 17 Feb 2024 01:10:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd53584de83e21bd6543fbd15e6631085f4fbd5412e9b43952ac49633af4b30b`  
		Last Modified: Sat, 17 Feb 2024 01:10:12 GMT  
		Size: 473.7 KB (473661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae48f4eb91d9b63d83f88289dcf9bd836832cc1ac7bb83d150e43db66264b22`  
		Last Modified: Sat, 17 Feb 2024 01:10:11 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d6944bf5a4d2950bc78f96656da2437f1d1ad3a9c64d85f498acf8de1d7374`  
		Last Modified: Sat, 17 Feb 2024 01:10:11 GMT  
		Size: 325.9 KB (325883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba5a3e24491186483f33b899fc4dc752a2f08208dfc5bceb50e61eda22baf13`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a869ee8411dd74c168214deb3d8161a143fd4e44c0f5166ee27b3f111f16ec`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a655dc6663c2af2d739609f26e2c7269346837b87ef4bdc50e7158b0baf6f904`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d7bd202ab86057f72700a11d269c2db0b097b8dbac38c76157ef3235d7bd68`  
		Last Modified: Sat, 17 Feb 2024 01:10:21 GMT  
		Size: 197.7 MB (197732548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e0addaedddfe4f019a9ee22f42446a93688888391527b1f818664d63fa6e98`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
