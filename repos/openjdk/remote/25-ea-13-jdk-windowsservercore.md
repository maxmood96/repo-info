## `openjdk:25-ea-13-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:a7b22a92ae6b2fe4d84be6ed1931a0d4dd27b5cf0e31da9264ac2673ec41856f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-13-jdk-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:9f0ae4973fe934969fd7235b1a8f0d729e20cc678d7549371b4299910b750f8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3025171627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b0a5cd2f8aa20ce8bd85e0decd3fc5c894ceb12c8b78cf47c46532585b0200`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Mon, 10 Mar 2025 21:10:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Mar 2025 21:10:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:10:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 21:10:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:10:21 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 21:10:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_windows-x64_bin.zip
# Mon, 10 Mar 2025 21:10:22 GMT
ENV JAVA_SHA256=5182d7ac4519ceda5c809ccaa65ed9f2bea331524a65f59c3fccfe52fc878ac6
# Mon, 10 Mar 2025 21:10:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:10:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d6162003cfa1060e50ca2e92849e0ac2ed9ead55fb02c6c255e0fe82417ffe`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44eebad473320c6fb7d9c39f9317dfef5aaae34613d73a17c0beb859b1c259`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 394.9 KB (394858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bc3d99504d0dca5d870e329aa5ba19abaa23dbdd8d1e8cd8c092c3f7314c21`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ec08f34cb8d4e3b9a7ff4f988b1effc4eeb847e809f44979f88897666d9513`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 379.3 KB (379311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27f889002e47b8942b9887d714a0731d50e8516c0b98c71607eddfaf9fa11b`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5763c02d9a26dd15d690f6c8ae3e800d98b5d02524775b504d6e28cb6faa9c`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcca8a81cf71935833dfe918867ae9443b041afb5ba1fa19d010603f9c0700c`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee54ee92adf4f418c221b89341a863526fbf0285efc127e354179bedf380d68`  
		Last Modified: Mon, 10 Mar 2025 21:10:59 GMT  
		Size: 207.8 MB (207801918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0841fda61205c5f139bbf554cc41f03626e0c8446f09a95ca5b40df90fb4726e`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-13-jdk-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:06f1af7fa770650d996a4db7a3248bc8a305cbe0ba2e8cb8f9d301671fee4a16
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472376545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66195a042ee8e1372eab998dd67b800b2cf479edaf4a0c436a95aa34373d4d41`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Mon, 10 Mar 2025 21:05:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Mar 2025 21:06:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 21:06:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:24 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 21:06:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_windows-x64_bin.zip
# Mon, 10 Mar 2025 21:06:25 GMT
ENV JAVA_SHA256=5182d7ac4519ceda5c809ccaa65ed9f2bea331524a65f59c3fccfe52fc878ac6
# Mon, 10 Mar 2025 21:06:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:48 GMT
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
	-	`sha256:91a146723cf5b549f9d0d2fb3c7deb4fe3e62fd4ff402d1bfd5f00c5131e8946`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6eb97dd92925a9ff756f3b7f29e11e53f5aa2fecde4b0f37a2e2bda48e56b`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 375.2 KB (375246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8c1aa1319d63eaf2e0cb7d6666ed7a40f8c59acc4635239dcbafb8cb7aa799`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c98b89b7d1ba14700577876fbd6b3630c04a8ed3058050f2c7415d789b30e`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 354.5 KB (354496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43a188f92f878b82a67f37f81b9a286e667a447d8f47ab5e12a8c8e5b0a22ca`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87f293452a56c47beddc137a11113bd4bc062d842e95a26206ce2c321988ff4`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa90467f6e12f9898cc1dd84e3c72fb9c3432b95e1b9f424f16854413e21c573`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fdb1ea33f83e9a903b0760d880ff9a603c1f5b4cece404d13fe84d495f2ef`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 207.8 MB (207781086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41db02b87535953a5a8b73e31d77447ec91334b1c37835ae2c13d52b3b1cd7c`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-13-jdk-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:6b0abeed33d2586009790db5a2b573b361a2dad84edf65a7321c52d1cd583e26
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345403027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c648b07cb0f663ac18da234a22263397cb87dc1e76b90aa99397423848a7a46b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Mon, 10 Mar 2025 21:05:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Mar 2025 21:06:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 21:06:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:25 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 21:06:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_windows-x64_bin.zip
# Mon, 10 Mar 2025 21:06:26 GMT
ENV JAVA_SHA256=5182d7ac4519ceda5c809ccaa65ed9f2bea331524a65f59c3fccfe52fc878ac6
# Mon, 10 Mar 2025 21:06:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:58 GMT
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
	-	`sha256:00737b3a8a0e4dbb1197b8d6703f7d279f6e2872a2e4ea11b93890b4b1ac56c1`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7eee08974d42d857025b082f974db6bcc575b980b2144d8d89eb0127fe15c87`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 358.1 KB (358082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f233dd76d3d3e8bcb7df274d85a7275c78c7f3ec66027621914bcbe23e970a77`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b57d039a3280f9eaf74af2f090617586c3b1a4294775b5ac9d88889e2fcd5`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 346.4 KB (346398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151a594bd487d47d360c7c2a6d733f02db300eaade172645ed3f25cb95a3a2f`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca9f2a4ec5c7eea52403d5f2fe76fb165087c1c6c2dffe247faae113191439`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75af185aa72b27a73380f26a4788b4413611e19b3810eaa64160a8c187d7c197`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47a55f4a2e2624bdb72af08d897a9bdf8c3a65a2d6f11e7e16cb71b562509eb`  
		Last Modified: Mon, 10 Mar 2025 21:07:13 GMT  
		Size: 207.8 MB (207781969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4179900255f926f8eb3341b42b0869621e61219dad6add37aa7adbf93733ab6`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
