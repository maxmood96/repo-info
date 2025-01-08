## `openjdk:25-windowsservercore`

```console
$ docker pull openjdk@sha256:0d15ce9bf2c171f62ada72d085e89ab1d38541842fedd3199e7024503e0417d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-windowsservercore` - windows version 10.0.20348.2966; amd64

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

### `openjdk:25-windowsservercore` - windows version 10.0.17763.6659; amd64

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
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95597edd1e8852b6182af65e7052f860e24b6539b0a604dfb728c20d1b53af1`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53a0967a33a27e0770d39c47d2fb24e6ce5524c8c705be4ed2826111e7f6227`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2579ec8940e6a9de984264e9e0aadc357371b8a6045be3c7a830326a58b5595`  
		Last Modified: Mon, 06 Jan 2025 20:30:11 GMT  
		Size: 209.0 MB (209010082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d75680458716856ccb9da8c04fcadef1220048d6dede019dd0b54549f2e3804`  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
