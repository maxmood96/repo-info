## `openjdk:26-windowsservercore`

```console
$ docker pull openjdk@sha256:e1e651d0b889d4c8f710e422c162b51ad60d08952ff6a8c4089163fe5e261d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-windowsservercore` - windows version 10.0.26100.6905; amd64

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

### `openjdk:26-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:920f5c63d0c9a0eef0e53b82f3bfb03f642d452d86fd57fd4bd116e9d22e6e60
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1799572711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce48e935e5c72441eee6e2f45f834efe6b357797b79c81b02a273d47f9e339c0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:25:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:19 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 18:25:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:25 GMT
ENV JAVA_VERSION=26-ea+20
# Fri, 24 Oct 2025 18:25:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_windows-x64_bin.zip
# Fri, 24 Oct 2025 18:25:27 GMT
ENV JAVA_SHA256=dbd547c391f90daa966d5d3a236e5a3cf792dea341d9596eb2a155059fe571a1
# Fri, 24 Oct 2025 18:25:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:26:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116a61045287ead6d3e96e549433b65e0cd74ce2180f5ec4df258d66b09b85a4`  
		Last Modified: Fri, 24 Oct 2025 18:20:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965ee7d4e5941254fb504bbf07a4d846c8116a09543cba0b5dd6a02dd409afd`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 493.1 KB (493131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c552306b194d12184edfc57f11620f4383e3e211e30f804ecc2c62b3daf45`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b2b5536b51c7e63ab0aaa7b83c1ce821c45bacbe94eecfa84d1bc905ee4fbe`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 335.0 KB (335007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c6b48d4b9e27041f607e7788cacf2a1014a2b43034c941e117e70267d2e3e1`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51cee5eca8ba1661d9a9d0aaf49f7e160a3f57b3c082a26e49764644d977f09`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281720dc0cebc19f7f111c9214ae5141953a3670e2135c7858d72a05b821fde5`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9e5b921041249c96fa258465845aa39e5326cc1ed747dbdeb5e71241beede6`  
		Last Modified: Fri, 24 Oct 2025 19:20:31 GMT  
		Size: 221.5 MB (221543812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2217eb78e443602f482082162a9636ac0f1e367296905bd9e618a23ad0fc0af`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
