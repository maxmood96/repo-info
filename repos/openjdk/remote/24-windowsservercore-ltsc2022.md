## `openjdk:24-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6f2658cb0be6e5fa57dd6524e51617e4ab2c8e48a797fbaf8842b82814878e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `openjdk:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:0efa4058149b59998d6942de27a849e52aa332db20bb6b82b0cb2dada68951e9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325435891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4796a5f5096cc88c7fe1944e0d7b36c26aedd0510b682c2646aa56f6985fd9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Mon, 08 Jul 2024 20:56:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jul 2024 20:57:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:36 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 08 Jul 2024 20:57:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:43 GMT
ENV JAVA_VERSION=24-ea+5
# Mon, 08 Jul 2024 20:57:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_windows-x64_bin.zip
# Mon, 08 Jul 2024 20:57:44 GMT
ENV JAVA_SHA256=6311a1a2de647471859f4eda1f035e7da59a26882c2bc3e456a97e88b9e9647b
# Mon, 08 Jul 2024 20:58:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56e6013afe5aad14ae831320fcc1439d2a8c8850cc862490ce4daf86f0ea0f2`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8d818e4212d9524f07bc31fb22eb5943759dac42c8faba8f183d1f847823f8`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 369.3 KB (369325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d652ef65eb43b7cc75a79bf3ce2cbc5cc502e09a1855f92a5dfd8ddec7a7e6e6`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1a00af15309a7e78189abe71742948d05f14a13c0c98166eb85aea63bf5a11`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 320.3 KB (320270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f12416285128fa398f4ace89455f42afbd3afc34304a3b8d7695e140b670181`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4098926a0cdd237a5638844be108a9150c4e50250c7ac38cb0ca7562980988c7`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785927fa36ac33800af4f021b9a4bcb9f1256360bcb346210baadc1b3ccd6b49`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff02cf044c24869c6f18a6c0345ab59e16c2fc27c914c82b2d83c2b26aa8b76`  
		Last Modified: Mon, 08 Jul 2024 20:58:24 GMT  
		Size: 206.5 MB (206548299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27dfbc167ff30c92ee6604f5d556112f9c248679203ad02bb8fb80930310a02`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
