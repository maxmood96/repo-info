## `openjdk:25-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f98ca64ecb4b9ebe2b8cb448bc9e8a2643021cb6c59344e0e86d1090cb93310d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:e66aeb5929210a4e9cddd4e43bd714ed7b68ca3f803b048b45c88e4072001df8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2375422781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5435f6646798a88d8e6ca25a9b48ae80d28f6da957ca477cfc77f9f7deae7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Mon, 05 May 2025 17:30:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:33:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:33:45 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:33:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:33:58 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:33:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:33:59 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:34:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d33ab57eea3ac259c13042d3b5aa44c76b9bb1d5bcb1c32cbbf392de50d776c`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbbd0e4b759e40eac1be5bd24a028ae190614dbf3fdad435620c9d5684e0bef`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 364.4 KB (364360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9213bbf4fd86b63c038405e6baec91de91f5b6da81bf611f3ce1e1eb0fafe325`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb44b0f60d0f2e264b4e84d0533e33807c0959829341314bad86b8c8aa7b17b1`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 310.3 KB (310270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a86735363a8b94069fc4e440baf6ab80ab63f5af6539587ecaff59c6d7b98e`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3391d2a01efc3c421b9bab859e5e7250e865618a137bcd2b6da4cdec66f754c2`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba209b546131662cef9f0e229addcf58971af17f68894e18334bf52d4f08b95`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04890a83c56695270eac5222fc64d9de84c832020fa510ed221907bd5f77861`  
		Last Modified: Mon, 05 May 2025 17:35:01 GMT  
		Size: 209.2 MB (209214248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6768314ead34460fa859d056b7fccfd7c8219e61a0da2113cc91bcb0307fb`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
