## `openjdk:23-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ce7c79715e342cde5d0f1421b490df4ee327473bdd3b189074c83991206e8516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `openjdk:23-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:9fcdea4c607d91ad7177743bbd3d83e20389c0d3f275d1f5cd796600898e3a14
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325330581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c12b503606e16c4cc8e4ae75f91be6bb3674a8d17ce36070f1fd20f6d4daeb9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Mon, 08 Jul 2024 20:56:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jul 2024 20:57:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:32 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 08 Jul 2024 20:57:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:39 GMT
ENV JAVA_VERSION=23-ea+30
# Mon, 08 Jul 2024 20:57:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_windows-x64_bin.zip
# Mon, 08 Jul 2024 20:57:40 GMT
ENV JAVA_SHA256=bbefe5300370b3a67927c127a1e24a08b8cb1dd37d41b428ed931836e092652b
# Mon, 08 Jul 2024 20:58:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:04 GMT
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
	-	`sha256:2cc07ac574c4eaca07e761475585085c686773c50ca8f3fb9ef3b82b6659fa40`  
		Last Modified: Mon, 08 Jul 2024 20:58:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b564dd2f5779bb676cd1edb738f5aadb43c2f289973c2ae00d277dc7c18cdc`  
		Last Modified: Mon, 08 Jul 2024 20:58:11 GMT  
		Size: 357.0 KB (356972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8732429a9f6257d8c8c05ec63892b47374545a546f12ebe8cf41d546014527`  
		Last Modified: Mon, 08 Jul 2024 20:58:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871a8a633db48f3d2ab452397f9260826213506477410d9fcac90a68c90574fb`  
		Last Modified: Mon, 08 Jul 2024 20:58:11 GMT  
		Size: 342.9 KB (342886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4796201e45e56cfa6d9a57220b638592fa1ab5988359196788e24d74c56157a4`  
		Last Modified: Mon, 08 Jul 2024 20:58:09 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68283a358a9fdfaaf45b1f8e9759fb0a6fd63273d24cbaea3b8708ef929dee3`  
		Last Modified: Mon, 08 Jul 2024 20:58:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77b7a49b6018fef73203c3a85b6f04a2ec0ee628408e41a6ebd49881324ed28`  
		Last Modified: Mon, 08 Jul 2024 20:58:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218f96e45f261b892454f09560f7c70b3d5d4cddabc829749d8d7d5132c1bb07`  
		Last Modified: Mon, 08 Jul 2024 20:58:20 GMT  
		Size: 206.4 MB (206432730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002657905a0925ea41d3da37cc0a95e60cc38b928cd0a1a8b42aec22f9ba987f`  
		Last Modified: Mon, 08 Jul 2024 20:58:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
