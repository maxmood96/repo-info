## `openjdk:23-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:314e7d9bc049c01fbabb7233544478ce43be9c53c782e9777d3c205101d75b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `openjdk:23-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull openjdk@sha256:7ed2c3cd20d02b8a2bf2b5e33672b406120b4c295decaa8ef40a019b7020a36f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2205855878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d91d7b98743e3b283db9b720558c4063cf713ca386c00c67cfc6fa726b3e3b8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Wed, 10 Apr 2024 00:01:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 00:02:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:02:03 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 10 Apr 2024 00:02:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:02:09 GMT
ENV JAVA_VERSION=23-ea+17
# Wed, 10 Apr 2024 00:02:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_windows-x64_bin.zip
# Wed, 10 Apr 2024 00:02:10 GMT
ENV JAVA_SHA256=d370ad95643e427d9a9f79c527dc3dfbd3fa07ebda3684fe18acba87d4342d57
# Wed, 10 Apr 2024 00:02:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:02:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c643e43ebcbdd806b6a94e25aa6fd089a945d8a3cd64c94505caaffc4a9ebe3`  
		Last Modified: Wed, 10 Apr 2024 00:02:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039599a84370a2ba7c288b3bbd3bf3caf39a57ddcc14d1bdfd948e0a75426740`  
		Last Modified: Wed, 10 Apr 2024 00:02:35 GMT  
		Size: 483.8 KB (483847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c02cdca4b6eced2f3bad861e9319ca716580d032cf8b7c20c26f9db349c824`  
		Last Modified: Wed, 10 Apr 2024 00:02:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0600a270d6938c9732423deb1265c96a65addff9703540b7c3d23a6db1eb5e`  
		Last Modified: Wed, 10 Apr 2024 00:02:35 GMT  
		Size: 336.4 KB (336354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedefdca8f0ba1a12f560bf37f276e2bc3887f92a0ca0d8943983edf9dba0179`  
		Last Modified: Wed, 10 Apr 2024 00:02:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae82518e25be25077dc8c17a0049d2eea10806feb422c3af479b1c6702de147`  
		Last Modified: Wed, 10 Apr 2024 00:02:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865abfd9fad164a074275d0967419a70c695c73701f97d36d86ab93d08c2ab4d`  
		Last Modified: Wed, 10 Apr 2024 00:02:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c265a20814b05184b816f5a5fda38074f710aa21b8abdf06d89b338c5a1ea2`  
		Last Modified: Wed, 10 Apr 2024 00:02:45 GMT  
		Size: 205.7 MB (205654294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457eaae8827dfca6dd15c3241c58df75e3eec2436b4ea8cc074ce2a2f5b42611`  
		Last Modified: Wed, 10 Apr 2024 00:02:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
