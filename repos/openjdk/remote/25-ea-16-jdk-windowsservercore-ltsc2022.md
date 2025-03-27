## `openjdk:25-ea-16-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:4c1a589eccebec265809ad07770b0c31c363da79cfbb779cd50f8abff24dd078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-ea-16-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:180d647f7fe4c0d1b7c44d78206ffdd761604f1f3b32b0be59601d76cd436b18
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2478934020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8941cb174da5674422e21877a2da17237764904cddafc9a03dcd67537d45e795`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Thu, 27 Mar 2025 20:45:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Mar 2025 20:45:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:45:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 20:45:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:45:35 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 20:45:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_windows-x64_bin.zip
# Thu, 27 Mar 2025 20:45:36 GMT
ENV JAVA_SHA256=147c12ac39a74d3d9e8372693e0531ab055aef0e9d4f8415efb5b4c3aa202353
# Thu, 27 Mar 2025 20:45:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:45:57 GMT
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
	-	`sha256:d6474f5054fc1dc1295feb1b6482c1debb01b9e92bc9c0112cc3cc330545fccf`  
		Last Modified: Thu, 27 Mar 2025 20:46:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea43c7979b2bface6b1d4fdb2e3a310f3617533a4dd75d6b15186686aa58eec`  
		Last Modified: Thu, 27 Mar 2025 20:46:04 GMT  
		Size: 361.4 KB (361393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ac27f44066ccded18509a832da78e2de360dee863dc67308cfa222a99d0431`  
		Last Modified: Thu, 27 Mar 2025 20:46:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb7740deb3d7a181372ac9fb6d2f0fc5631ffc674604573e9db06791789f0b`  
		Last Modified: Thu, 27 Mar 2025 20:46:04 GMT  
		Size: 346.7 KB (346666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da2029b57b5edafb4ee58211b2a00f8c585abeeeea12b7097c3bed494d07840`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e5c3e629d7d41fac994f6d7ad7483b0b6f4f786e346ee07cd9bba36141e50e`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2c9679a389ec5e468f40fd078b45a3b75c6c1a4e24bc749fef838d591dfe9b`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7cb1be01a5cc8728c8a60f1a74f97ff30e9e226e04310872e8ec776e1f5d14`  
		Last Modified: Thu, 27 Mar 2025 20:46:12 GMT  
		Size: 208.3 MB (208277094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb0954aceecafe72278b2a5b79a8b81c0693d74e57f3f31be71dbdbf4a4b98f`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
