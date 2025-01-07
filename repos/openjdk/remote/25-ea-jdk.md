## `openjdk:25-ea-jdk`

```console
$ docker pull openjdk@sha256:94eb42c2fd5f8e3303fc2ca83968653117ae5913d85923f31db4c89b0549a7a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:be1ba5f09d2061b2f6b2ac6c154ec6cc2d439e5eae52e3bdb487bef8a3efc267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310792571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf4c65c2e7295459b2df3efaabce9ff3dc22b39ff41d0e13e3e99e820c89639`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Tue, 07 Jan 2025 19:45:20 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07afacb21e616d9ac41fa5658804ed38571980eb6ecd0779713c64842bb8582f`  
		Last Modified: Mon, 06 Jan 2025 20:28:35 GMT  
		Size: 48.8 MB (48774167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430e51b0977958fcc6a84677be0bd3832b2ffd321fe9736ea32a3bb089435bd`  
		Size: 212.9 MB (212919702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a57ec4b2e910e02ffe9cb03734620aaa3442bed8d0d8421a0528881613c6c1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604dc0eea6b2b16f0038c7296491ed0994182f092a92a4c0bcb22edef8647cb7`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ea34c44838a565fa0b949678acc8589db14bb51f2fe56c5189b34e188afc3`  
		Last Modified: Mon, 06 Jan 2025 20:28:34 GMT  
		Size: 4.9 MB (4907559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53218db3a441ce569385b2966e708a3cb6bed148a0439211df5ff1c65f8e2855`  
		Last Modified: Mon, 06 Jan 2025 20:28:34 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f946914047a7d1b86d55c712ca88139e29570b7d72b49707e74c9e0b8062c8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307732026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165ddf036e71bf46b71ff460fce5c89204bb6c838201d012e4aa15c2761107f0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
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
	-	`sha256:e56e753fbc124d85cbb99e125d01d4ce454601183ab9db8a8f35680fe7ce5ac7`  
		Last Modified: Mon, 06 Jan 2025 20:28:19 GMT  
		Size: 210.9 MB (210868147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:dfbcc76c9a2dd23955c4a02e29fe580fea76cd4978389a88ab9caf7e7e9c430a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aeb2845f8c2f8550ff53c787cb8348b61e44fc86d05ed0e5703b0a4e4610d02`

```dockerfile
```

-	Layers:
	-	`sha256:d659fc32fe81a9959feea75d7b1921df5db26f0f7c05ea543ae4bb8e763355e9`  
		Last Modified: Mon, 06 Jan 2025 20:28:15 GMT  
		Size: 4.9 MB (4905321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99ed112db1a9ef5f019ca0d2ae06a2901d3e8e992846053d93c39e27eddc6352`  
		Last Modified: Mon, 06 Jan 2025 20:28:14 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:1f50676a2bf1bd1d247a1d3eb6ade1a8bb1639e08137cb24592def819880794b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463590129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf98d582dfdc94d8e892d4d8e3400becd7016cec140548db8f4e246fbf77ef0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Mon, 06 Jan 2025 20:27:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 20:28:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:22 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 06 Jan 2025 20:28:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:32 GMT
ENV JAVA_VERSION=25-ea+4
# Mon, 06 Jan 2025 20:28:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_windows-x64_bin.zip
# Mon, 06 Jan 2025 20:28:33 GMT
ENV JAVA_SHA256=a269f89b8b7317bbeea0e0df24e66a537aa1762f6b13db3da0fff25ce714ab98
# Mon, 06 Jan 2025 20:28:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:29:01 GMT
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
	-	`sha256:f4b48e7ba38ad4b6d6373d83298ea1580907f56e196503eb0b4628217cc0fd6a`  
		Last Modified: Mon, 06 Jan 2025 20:29:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b28caaf1bd43ed96adcd8af6947789de41cc04ce76dc452a482d29f4e16bde`  
		Last Modified: Mon, 06 Jan 2025 20:29:06 GMT  
		Size: 359.2 KB (359219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4837db16aa18d2ded073b2360b64fb8f9d90f9f19922417f47c3b9dc877447df`  
		Last Modified: Mon, 06 Jan 2025 20:29:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4fa8da22e03b9609328827dd7a950eb69fde71d5a3acc16fa3e38aa4f450441`  
		Last Modified: Mon, 06 Jan 2025 20:29:06 GMT  
		Size: 347.4 KB (347396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007fa8264f4287521a3d237dbc9bf029b1a6895cce8bd89511fbae4cffa67a56`  
		Last Modified: Mon, 06 Jan 2025 20:29:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09debd8cb4e35d53efe5ba82f83cfb3a92fa723d92aac47887641a2b6b34bb64`  
		Last Modified: Mon, 06 Jan 2025 20:29:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22de8f318fb2505ad3d15b44c45a989b6fc113a21f752adfcd002f3c4bd6df79`  
		Last Modified: Mon, 06 Jan 2025 20:29:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1c570b5c154d70ae9de01a4b237c68eddfe5b459e175d5954be22c55f28e0f`  
		Last Modified: Mon, 06 Jan 2025 20:29:16 GMT  
		Size: 209.0 MB (209002147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914a717c287a08c952950c642ee755dca5f1f217bfeb6f31794c8f0f5c43444e`  
		Last Modified: Mon, 06 Jan 2025 20:29:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:37756ff96bbdc664bbeb90f2875249af725c5ffb2f5c102a502b92b23b51ff03
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224012853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baa9b0e3404726684b22b74bb8306c20e91fb2d16398f53d3c0364a517142ec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Mon, 06 Jan 2025 20:27:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 20:28:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:58 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 06 Jan 2025 20:29:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:29:06 GMT
ENV JAVA_VERSION=25-ea+4
# Mon, 06 Jan 2025 20:29:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_windows-x64_bin.zip
# Mon, 06 Jan 2025 20:29:08 GMT
ENV JAVA_SHA256=a269f89b8b7317bbeea0e0df24e66a537aa1762f6b13db3da0fff25ce714ab98
# Mon, 06 Jan 2025 20:29:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:29:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9c28c64c5934715727e50f34212b6ce7722ecdadbc6853c2f0703cd76067c`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1805afc196d9b719a68a1d2f78e8728c2a1e3a280bfeb6dcafa622585187eef0`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 486.2 KB (486242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea14f5040ebfab52b413a5cfc758dc7c1a038b6a94c919a3eb573a231ab9e3b`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4662df3f4b234415b2caece2cc2725d6a703371c33c1b531252fd053c46b67`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 338.5 KB (338487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6509f0be496765d86091492a39222eba375b2f89c6cf946587d0995b9771c6e8`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95597edd1e8852b6182af65e7052f860e24b6539b0a604dfb728c20d1b53af1`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53a0967a33a27e0770d39c47d2fb24e6ce5524c8c705be4ed2826111e7f6227`  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2579ec8940e6a9de984264e9e0aadc357371b8a6045be3c7a830326a58b5595`  
		Last Modified: Mon, 06 Jan 2025 20:30:11 GMT  
		Size: 209.0 MB (209010082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d75680458716856ccb9da8c04fcadef1220048d6dede019dd0b54549f2e3804`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
