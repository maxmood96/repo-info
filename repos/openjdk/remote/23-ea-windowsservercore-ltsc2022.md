## `openjdk:23-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:97f5bc73dd1cf67183f62324768db02dcca83d8c709d2504aeba8e0268310947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `openjdk:23-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:9e94eacc678a0ebb03b5b50dd305f127c78a090fbc18c754be2af02660b34903
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109423364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db5ec9dd5fec16e1ed98999f65e50e05ec52cf73a43646c84ab0ac23cc22042`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:04:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:05:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:05:16 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 14 Feb 2024 20:05:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:05:22 GMT
ENV JAVA_VERSION=23-ea+8
# Wed, 14 Feb 2024 20:05:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_windows-x64_bin.zip
# Wed, 14 Feb 2024 20:05:23 GMT
ENV JAVA_SHA256=3bf12bda8aa3d293ed14f6956bd24e598c395e3267be4b58191e542ec7d3479a
# Wed, 14 Feb 2024 20:05:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:05:43 GMT
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
	-	`sha256:f1adc40ac6783423ae8c427f8a9c75bc3f8423037089ac9a55899ab4000ac93b`  
		Last Modified: Wed, 14 Feb 2024 20:05:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385bfb9b627e5dfd49895b57c5cecb06a945816b39f3ecbe86cace77682d1679`  
		Last Modified: Wed, 14 Feb 2024 20:05:50 GMT  
		Size: 504.0 KB (503992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74b06b63c9c87360f7f5092bae8a6143093613f5da732b83c64c075307bbb72`  
		Last Modified: Wed, 14 Feb 2024 20:05:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5376f0bf822edacaaba9d884173c798ee9fd9073f70cc6bde6a70e82873c973f`  
		Last Modified: Wed, 14 Feb 2024 20:05:50 GMT  
		Size: 354.9 KB (354865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f68de43a74c5217362e45939c743c2e518df9fda4f3d54d8be96f254270ba9`  
		Last Modified: Wed, 14 Feb 2024 20:05:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e69477c2e6a9673808cd250d81f763b3a66eba70b4d6d457c50055fd68e5f94`  
		Last Modified: Wed, 14 Feb 2024 20:05:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b5fccaeec144a908003cfd6c8814ec78aa1f6f740908fa3fccb674b55cd0a7`  
		Last Modified: Wed, 14 Feb 2024 20:05:49 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082bffd234f2be6626e059312f6cee4d62aea6edfdb7122dd98ef6608a244b9`  
		Last Modified: Wed, 14 Feb 2024 20:06:00 GMT  
		Size: 197.9 MB (197902592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366449e3db53e03e198ed1d66685336a82ed12e74f02c1bcb9271a9cce882fb9`  
		Last Modified: Wed, 14 Feb 2024 20:05:48 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
