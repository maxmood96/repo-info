## `openjdk:22-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:70ae79f255045ec227d0801e5a60534d4715ade1beb97e4f3878e8f061b1fd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `openjdk:22-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:965b10e1e2642c7d35c34c98b3889fb5db012a3b876db18584af004907da5e9e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098798485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0398f6ca05cc3c2bb9bb60101a6917f0fac554b9f5d3d6024ef3e2b45b2da23d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Sat, 13 Jan 2024 01:15:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 01:16:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:16:14 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 13 Jan 2024 01:16:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:16:20 GMT
ENV JAVA_VERSION=22-ea+31
# Sat, 13 Jan 2024 01:16:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_windows-x64_bin.zip
# Sat, 13 Jan 2024 01:16:21 GMT
ENV JAVA_SHA256=4b5b81fcbe9e209bde075929fc5e99b71fd2ec4b2ad046404aec3476daf5c148
# Sat, 13 Jan 2024 01:16:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:16:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba2d7f2709cd759097cf2b04bca8663e5a344bba070388c574aeaf626de47e`  
		Last Modified: Sat, 13 Jan 2024 01:16:46 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e0733becb6344625b5e5731fdd5ab10f57095d3e5d259df52852bf1e53ab3e`  
		Last Modified: Sat, 13 Jan 2024 01:16:46 GMT  
		Size: 497.1 KB (497073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f735d3c53b88ca5d3891c3ec26f859a9bcc5ce655d3d502db22f4977967717db`  
		Last Modified: Sat, 13 Jan 2024 01:16:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848aa2a59a6e4804dd5459a6c82df779b9a70a73179e4304e76d8c2c77447d7`  
		Last Modified: Sat, 13 Jan 2024 01:16:46 GMT  
		Size: 350.1 KB (350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96b4a9a3f88cf32ae1f9a12831e697fe8760886b34e36a6167ace0c9f004bda`  
		Last Modified: Sat, 13 Jan 2024 01:16:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c3841eab26c990026eacb5e90a5e1ee2ee15949a9ae43cdef10859f53d4514`  
		Last Modified: Sat, 13 Jan 2024 01:16:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091c5273dea5743e2a307c6a58269d7fcf66b91f9434aba23f2c253e4857ab26`  
		Last Modified: Sat, 13 Jan 2024 01:16:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202b70d195985a51bc2327b66ad6debe2a22535f1600c9606a19376a1a4f7ef`  
		Last Modified: Sat, 13 Jan 2024 01:16:56 GMT  
		Size: 197.7 MB (197730924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b482af3e6ccaa25ed66c26ce3a541621d969c3cf4197efcfbb5579dc51a0068`  
		Last Modified: Sat, 13 Jan 2024 01:16:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
