## `openjdk:26-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:1aba79766d7997ddb51ede0b52387965a61ccc2ff403d251895929c37039eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:dcaf1b0fcb10da8796f5e3995ce88ddce631d60fcf93c9fd0b74db5c0db89ea4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442588550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df30acd51fb7d80fdd310d0958b10fe94753801c489fc7a6673fb1083e55fb64`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:25:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:52 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 18:25:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:58 GMT
ENV JAVA_VERSION=26-ea+20
# Fri, 24 Oct 2025 18:25:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_windows-x64_bin.zip
# Fri, 24 Oct 2025 18:25:59 GMT
ENV JAVA_SHA256=dbd547c391f90daa966d5d3a236e5a3cf792dea341d9596eb2a155059fe571a1
# Fri, 24 Oct 2025 18:26:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:26:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571af3b90b3defe521c8285732a5f27a7d3abdaa40750b1b3e6b3d6208a2b69d`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63342a0df8c3b04da2641155654f3abb2efd56e5631d876efd52b593ded2533e`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 357.3 KB (357257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778674c5686153fd6b36a9dce761dd8d20054eae0ac61ec44dc9990e84afa732`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa57fff4e53c6a15dc770524ac1915eb558c250371f1fab8177c48c85bee2`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 339.9 KB (339859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415656e85a86621f67a54d2f4580c516da12bed96b4b70919b275baa66d3e033`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b0b4804f525525dbfc6675fabde05c6aa78a4e69fe543eff6d529d1eb3e979`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f4143e4d79f6d99ae2b1bfa65167a789d64367ecd72eb819142ccca08a0b18`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e15882bb296b95dc8e2c193f8548e10e565b2b1331985ae12f75b576e0f3c9`  
		Last Modified: Fri, 24 Oct 2025 19:22:23 GMT  
		Size: 221.5 MB (221536571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a5769a93539dbd680ec29a6ec9b65125efda73eb2831a4dc1fe17de224a154`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
