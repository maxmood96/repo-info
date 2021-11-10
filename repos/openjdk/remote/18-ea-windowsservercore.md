## `openjdk:18-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:a991c6b5666e0d0edb90abea94e1ad76b3803a3b2f91841aed6ceae81380a206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `openjdk:18-ea-windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull openjdk@sha256:e8255df62dff59325ca6e55e1bcc9080692eaefdcdbb1d7deaafb57971ee86de
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369632853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f00655015db4254b3d0354638c0dbea2256f1b504ac92eb2577f6a5a1884f4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:23:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:23:24 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:23:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:23:42 GMT
ENV JAVA_VERSION=18-ea+21
# Wed, 10 Nov 2021 20:23:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_windows-x64_bin.zip
# Wed, 10 Nov 2021 20:23:44 GMT
ENV JAVA_SHA256=d86fa72089f38517f71cc0bc0b431978c3c5c820971af065f17813249833bd87
# Wed, 10 Nov 2021 20:24:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:24:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4afb60e31b5cebc49ca0785c802982ffcb26a35cbf45cb86cfacf57f997ea`  
		Last Modified: Wed, 10 Nov 2021 21:03:27 GMT  
		Size: 616.5 KB (616541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db941a11fe2589a4b4de4126a25fa46cf249f4a92b8a2096088b8a6ef786873`  
		Last Modified: Wed, 10 Nov 2021 21:03:27 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d59e6a5010c5f473824d430525059a4a652ec50176e6bc1e1b6b1cad7c7a562`  
		Last Modified: Wed, 10 Nov 2021 21:03:27 GMT  
		Size: 549.7 KB (549708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b698dd11831adf277aae025052bc6eef078afd78744099225fd6ecd561fdcb6f`  
		Last Modified: Wed, 10 Nov 2021 21:03:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0900c61346cbdc2e5203cfe88ec50506b93be59c3bd52564a8b95a1e0f5f4d`  
		Last Modified: Wed, 10 Nov 2021 21:03:24 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006246c3aa0e0f4bc3f01c03d0e7d48693d0725b25f3e78f3581915d92760caa`  
		Last Modified: Wed, 10 Nov 2021 21:03:25 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f8dd5277feae03b608b6cc2ff3cd3dc5107d8e8b71c5d8af8412db74134f7b`  
		Last Modified: Wed, 10 Nov 2021 21:06:46 GMT  
		Size: 183.9 MB (183851222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ce1c5faf404eee966a95111144858ca8a1cd9b461dc6660bda459e2b91294`  
		Last Modified: Wed, 10 Nov 2021 21:03:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:2844a4f5ef91b81e8639e3c77c53eb720cb1a92d7615cb49e474db929c7f0e4d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2890432121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb6fdab0d77d354269b0c787da93627f788070ff04e27610bf4d74ac6947dbb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:25:40 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:25:41 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:26:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:26:31 GMT
ENV JAVA_VERSION=18-ea+21
# Wed, 10 Nov 2021 20:26:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_windows-x64_bin.zip
# Wed, 10 Nov 2021 20:26:33 GMT
ENV JAVA_SHA256=d86fa72089f38517f71cc0bc0b431978c3c5c820971af065f17813249833bd87
# Wed, 10 Nov 2021 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:28:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7f0affb9ccb091d200f0da9e1f9185ac51673de7fed0c7b6d5c33e7c906911`  
		Last Modified: Wed, 10 Nov 2021 21:07:09 GMT  
		Size: 358.8 KB (358799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a21fb561807e9b05cf652f1182dc25ef7b18f2232c5d220b81c2839b72e500`  
		Last Modified: Wed, 10 Nov 2021 21:07:09 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5e7fa285671a6b0e47f3b3605a5bd4cbf01edeb0b1f9b6b7640b3709ab7385`  
		Last Modified: Wed, 10 Nov 2021 21:07:09 GMT  
		Size: 319.7 KB (319676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27f6a08e6bde711bb8374842ac82c0cad5fa223e6215af6895d7b1ae20ab601`  
		Last Modified: Wed, 10 Nov 2021 21:07:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17e13d4cdd0b960ba531f11242bb58c8a359c38dbd6bb4bdd03853994bc2ce`  
		Last Modified: Wed, 10 Nov 2021 21:07:06 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847b4d31b558449e54882e692193c6e77fd877cb8d037083d8898f0a3e4efe6`  
		Last Modified: Wed, 10 Nov 2021 21:07:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a35ec7cf69a61548328a852bd3c946f51685d419a4c79f87802db51db08c50`  
		Last Modified: Wed, 10 Nov 2021 21:07:26 GMT  
		Size: 183.6 MB (183623942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5753877e7a39a9e13e30aa822049b0a084cda5de4a40cd5f6ace47ac2fc9eb10`  
		Last Modified: Wed, 10 Nov 2021 21:07:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull openjdk@sha256:393e2252dd54db1eae006103f025518c7a5ad43752461ed3d8ee1de90f0395ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6457431629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d306462a846e7b818d1a0e0e8ab77db60ccccfd35a285ce2ee8647be0f0f9de`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:29:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:29:10 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:30:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:30:06 GMT
ENV JAVA_VERSION=18-ea+21
# Wed, 10 Nov 2021 20:30:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_windows-x64_bin.zip
# Wed, 10 Nov 2021 20:30:08 GMT
ENV JAVA_SHA256=d86fa72089f38517f71cc0bc0b431978c3c5c820971af065f17813249833bd87
# Wed, 10 Nov 2021 20:31:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f998978d6856e995f1d9c4942941c32a17a4d88aff023bd7b9c78fc2a16c252e`  
		Last Modified: Wed, 10 Nov 2021 21:07:51 GMT  
		Size: 355.7 KB (355709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efceaabe52cac09e507c97b920e08a9358526f82a968e0123516aab06c1ac57b`  
		Last Modified: Wed, 10 Nov 2021 21:07:50 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b2835ec5caac2405ac77407ac306d4269c837a329e31ef3e1e8ff58363dec8`  
		Last Modified: Wed, 10 Nov 2021 21:07:51 GMT  
		Size: 346.8 KB (346841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d9bca52a27503493f0c99b4a99920bf0977ea36e5c98d5640b9974957eaf1c`  
		Last Modified: Wed, 10 Nov 2021 21:07:48 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3555ad46e455b194d91f0a0c93835b1f759bed8eca17a3a0dc657385bd13c`  
		Last Modified: Wed, 10 Nov 2021 21:07:48 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a124c261e3810baa7b86d3002f7c9bb0d9b74f151a368c9efdd7dbda0dd0d5`  
		Last Modified: Wed, 10 Nov 2021 21:07:48 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d67ffbd95a6b961816519f50fa3d55ae7eb440d88109b8d6784a1093bfe62e2`  
		Last Modified: Wed, 10 Nov 2021 21:11:11 GMT  
		Size: 183.6 MB (183629721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06fd0b5df6b3417d9ff1f2bdf32c8c9ed0d6a0c45b70e6db8fb0a0019e361d7`  
		Last Modified: Wed, 10 Nov 2021 21:07:48 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
