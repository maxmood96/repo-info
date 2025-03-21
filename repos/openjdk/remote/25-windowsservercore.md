## `openjdk:25-windowsservercore`

```console
$ docker pull openjdk@sha256:54f88955dfe3f8e49de45527efc61e026c4af9b4b3ceb748aa2f71a43e710e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:6506d6bb85c1de8ac30a4a243e3ee3fc3b7c64d619af20a6a2df8b6f9d7be79e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3117371676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f701ca969bdb34ca86d47f8dabc54524299423ac209edb7f85e3f410fd93a876`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Fri, 21 Mar 2025 17:18:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Mar 2025 17:18:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:18:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 17:18:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:18:33 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 17:18:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_windows-x64_bin.zip
# Fri, 21 Mar 2025 17:18:37 GMT
ENV JAVA_SHA256=a095e71a2552995360224643760900b2c44fc91dad10cab9d289bed71fa936dc
# Fri, 21 Mar 2025 17:18:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:19:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f29c6dad3e1d96433b03ed05cc6309f224ea92a969bfab4887167529bd13d33`  
		Last Modified: Fri, 21 Mar 2025 17:19:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dabe5df79724f97b77b6a2ae2dfd576801a9c0ba0aa5afec9f7deb8af4fe268`  
		Last Modified: Fri, 21 Mar 2025 17:19:11 GMT  
		Size: 401.9 KB (401919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410d739f391e8433c3eb33d92cdfdf11e0a3000f2e6ef5b6adf7485cd9665f49`  
		Last Modified: Fri, 21 Mar 2025 17:19:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10b4e9db977732cf18dcba6e85eb5dd1ec9ee95a27e73611500da08336efcf7`  
		Last Modified: Fri, 21 Mar 2025 17:19:11 GMT  
		Size: 385.3 KB (385286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf378787f91bad6a2467b655ef19bb5532578365e268a653571dcfc63a630acb`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43df5ce49f6a47b2f2b3d80a330fcf41850c6cc86a181135a2309bdbd52907ae`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9007cf78149c45d331fd747cffdd24e5ae7398bee87e0c1366eb04eafeaae`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0417b4393bcc741f4057e53138efad28110760c4a03f3596695415be79aa1a`  
		Last Modified: Fri, 21 Mar 2025 17:19:23 GMT  
		Size: 207.9 MB (207928976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff24e7b8e0cac7a58d4cdeb32a6b4373346f9b5f2441f187fdf0843d52309a`  
		Last Modified: Fri, 21 Mar 2025 17:19:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:7fffa5ae2d585664f5a9315639ed4b5f167dc2207c747ffd52009b90ee1b055d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2478547769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf45bb111caed9cd7ddf9ed3fe1a016463d07dec7b15c490703d598d4caf18b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Fri, 21 Mar 2025 17:21:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Mar 2025 17:21:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:21:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 17:21:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:21:34 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 17:21:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_windows-x64_bin.zip
# Fri, 21 Mar 2025 17:21:35 GMT
ENV JAVA_SHA256=a095e71a2552995360224643760900b2c44fc91dad10cab9d289bed71fa936dc
# Fri, 21 Mar 2025 17:21:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:21:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f379f06fa75c4e44e374efb896cc1a2a305a0ec35e4b5381c3a3d3f40b6b762f`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8769919e37c5f16ced3587f18562a353374956be3ad123c666fc3c1c1ee375`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 361.7 KB (361748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db36bd2a1f0f65ae5d121a12f57cc94469632ca277b9ffa9d2b9815b2ff97f9`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209cc8b876cfd7786dbed6cadbffd064cd7f4129d29f78bc84f33a8d2117df9e`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 347.5 KB (347533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4e6f5024b44a5715e0171b91af8c8c7f8ba72a3173ab6a9e362e9a92390856`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36803b8cbf1bfa57586e698b16ebf22ee0cf7b7897f2683a053ab3fe4982a7c7`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275269dc2b115c47cfcb04c02fff89caac64a77bca3b7b3f1db8d77571f0e025`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac8778d4970ae0eeb63f9d47f85215932aeebe93c60b66b03700e67bc8aa01e`  
		Last Modified: Fri, 21 Mar 2025 17:22:11 GMT  
		Size: 207.9 MB (207889484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9673b9c96cad644cb789913b5a1cd5ae085619aab32a641d886fe6b093e5db`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:3995bae6863f529980d80559465051a18c29f26e2393248d7d3286e3a458845f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2360193389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139dcda29592b699634068860908758abd9ea7a5b2ff752c81142755ed1923f6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Fri, 21 Mar 2025 17:16:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Mar 2025 17:17:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:17:20 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 17:17:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:17:27 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 17:17:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_windows-x64_bin.zip
# Fri, 21 Mar 2025 17:17:28 GMT
ENV JAVA_SHA256=a095e71a2552995360224643760900b2c44fc91dad10cab9d289bed71fa936dc
# Fri, 21 Mar 2025 17:17:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:17:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79207f2177d6845797b0817847078d4d6dd5ea90aab1efeff99a81659263c7e6`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe4fedb6c8705826bee29c3d281dcbe969a91c6ff312f3d9c56723e19518d0`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 341.5 KB (341476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6865af3755eadda1958e1e828851c76e29d85609846870f331a044c4e767c2e3`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7afc79c6049e83f64448aa2fbcd652435d5bdc7d5b0886c8a9139f90cb800a`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 332.1 KB (332126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c25587320e34c7c0c2c501042ce24bc5c995d4046d2d297342a9b3eab6508a0`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a14a51d5c9dcb38a3e7a985f2757a764a27eadaebb9f9feb198974f71099f9e`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb74eb8d91dcd2aa7a44ca646dddf87c181c56b911b795a18fe422c97bd28a`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad5da8215fb889f89ff018e86c90b2e160359f111373a6092349f752abf6e0`  
		Last Modified: Fri, 21 Mar 2025 17:18:06 GMT  
		Size: 207.9 MB (207877359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747ebe89f34874a9758188d8399c52b866c267c0a0e2cdb090ff45fc1862e3d8`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
