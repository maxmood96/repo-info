## `openjdk:22-rc-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:a8c41d2ebf054b2c8a03c0bca1e9297829c852e340ec8fbf05af5a432f6c5f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `openjdk:22-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:b895b1c014827f6b2420b8f1495137192aeb92abf05247a60848ce46420c6229
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109227332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8c164b4d235cb328e4a8716fc92ebec00f58f1ef8af18578bf106f9e69c94e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:00:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:01:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:01:08 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 14 Feb 2024 20:01:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:01:14 GMT
ENV JAVA_VERSION=22
# Wed, 14 Feb 2024 20:01:14 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_windows-x64_bin.zip
# Wed, 14 Feb 2024 20:01:15 GMT
ENV JAVA_SHA256=66546cc473f6f4ebb8161a8664afc6e04fa80cdf5c93a33e07f57eb1c27d6682
# Wed, 14 Feb 2024 20:01:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:01:34 GMT
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
	-	`sha256:0db9d271e2a51b2b5aadaaac2912c5ca628b310b55e20bccdeba1c5dce2b7695`  
		Last Modified: Wed, 14 Feb 2024 20:01:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd473ceeccc8887c3f1a847dfff208cf69928d392a3962e87370975853dcdc`  
		Last Modified: Wed, 14 Feb 2024 20:01:38 GMT  
		Size: 491.5 KB (491458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d303b5bbf46f397384cb13e51a8d9ded9240f983cbf6f4c9fef62c757c0a36`  
		Last Modified: Wed, 14 Feb 2024 20:01:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241c513149f9949edcafa8bf129e957976d4b6051bb4887c8ffc0f3abbd09159`  
		Last Modified: Wed, 14 Feb 2024 20:01:38 GMT  
		Size: 342.6 KB (342585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a81464d4885d3cac25f874ffd8a116422e8ca5e6d3b54ed296924e885f00e22`  
		Last Modified: Wed, 14 Feb 2024 20:01:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75b07f3b96a1dbedb285f3352cfdfddbffbf92c64c81d6f5f85cdae01730e6e`  
		Last Modified: Wed, 14 Feb 2024 20:01:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eca8796000fc581f001eb015f76ae4a47f7a4f2268fc3e540835e233535919`  
		Last Modified: Wed, 14 Feb 2024 20:01:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5c5607c5fdfc2ad4c1eca61d4129b84e889547df6eccb15febebff247d721`  
		Last Modified: Wed, 14 Feb 2024 20:01:48 GMT  
		Size: 197.7 MB (197731381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8635c82a0b1b04f082bf4a9b3954fad5c5d1add5a6e947b1fbbc10f342e139`  
		Last Modified: Wed, 14 Feb 2024 20:01:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
