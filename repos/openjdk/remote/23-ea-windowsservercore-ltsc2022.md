## `openjdk:23-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:4e1369083aee7d8839100343864e6360d93c3dc32b3ca6522dd7cef9766ca11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `openjdk:23-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:843cdee68aab6bb5f284c7e362ca7118dd12159571f86487491ffd1b6c2f9414
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098946374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9082f30d292cafee1543b26a098a0f150d28a646769b033242a01e9e9db13507`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Fri, 26 Jan 2024 23:49:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jan 2024 23:50:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:50:39 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 26 Jan 2024 23:50:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:50:46 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 23:50:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_windows-x64_bin.zip
# Fri, 26 Jan 2024 23:50:48 GMT
ENV JAVA_SHA256=ed56621259542fefdd1f8719171f0b87d695f984be01061164420c2b90b8ba62
# Fri, 26 Jan 2024 23:51:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:51:50 GMT
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
	-	`sha256:833d22f5afd031f90baa77091adb5ecab17207dbc9af240a813b638255ed78bf`  
		Last Modified: Fri, 26 Jan 2024 23:51:56 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c803be6f6ea6ef620b5c3c8a58fa324a54015d2bcbc7d37242f8c79b931392`  
		Last Modified: Fri, 26 Jan 2024 23:51:56 GMT  
		Size: 495.4 KB (495442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61573e5fef97c95aaadad5f762563cf4095cb5d3129017b35a3a32bd73444cd0`  
		Last Modified: Fri, 26 Jan 2024 23:51:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdcf643ca62d90e885393a2304a3a8207abee86cb232bb9de6c3a3345298d70`  
		Last Modified: Fri, 26 Jan 2024 23:51:55 GMT  
		Size: 348.5 KB (348515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05fbc5efaf59be248d90f384c0e8181c087106b6da9e87a168ec87b69cb79ea`  
		Last Modified: Fri, 26 Jan 2024 23:51:54 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a659d67636addc516d758f8bc1e3e1583f83b4057cfbef41bb3f90501f6d80`  
		Last Modified: Fri, 26 Jan 2024 23:51:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7f253123bef65c7a53cf2c5f0d239bdb4db208232cb9653fbbc803e6c34c4f`  
		Last Modified: Fri, 26 Jan 2024 23:51:54 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ab743261cd6d73d45d16e8fd4760143f12ca9d7d7959033d10d052ad960530`  
		Last Modified: Fri, 26 Jan 2024 23:52:04 GMT  
		Size: 197.9 MB (197881866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afca2450486a18772b00c6890d560b58b95af82086c3c34969ee4729aa06e86e`  
		Last Modified: Fri, 26 Jan 2024 23:51:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
