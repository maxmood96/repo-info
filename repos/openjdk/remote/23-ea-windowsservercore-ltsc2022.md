## `openjdk:23-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:70a02d5f0f9459c43d690c376ce87e8f29b809fd3a16f8aa49a5be12728ee91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `openjdk:23-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:ffaa1e6de7495bbea0af45b24e569ad26db11f1cef608a2e7d1d382ba5d926f5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155860773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b945cfcb15ea0d01ec43d2883d28cd20d705794c982444b7c09b5ab8a2f6ca7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Sat, 16 Mar 2024 00:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Mar 2024 00:03:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:03:15 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Mar 2024 00:03:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:03:22 GMT
ENV JAVA_VERSION=23-ea+14
# Sat, 16 Mar 2024 00:03:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_windows-x64_bin.zip
# Sat, 16 Mar 2024 00:03:24 GMT
ENV JAVA_SHA256=bda022a1843857170a5addfeffecf490af3c3b93a8925899193a09a093bd8b4b
# Sat, 16 Mar 2024 00:03:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:03:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4f5d3d1534dc31c2c30f1f0700d76a2359b2401c6291e7a39a5abac649d3be`  
		Last Modified: Sat, 16 Mar 2024 00:03:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9525845d439d75526f992868a56075c10cc3fb848b2c8eba33fff869b4bc5a8`  
		Last Modified: Sat, 16 Mar 2024 00:03:56 GMT  
		Size: 500.6 KB (500577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfef0bbe213d3118837b6fc7d7894b2f0abfa97ac8fc78d7673a1d82410793b`  
		Last Modified: Sat, 16 Mar 2024 00:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6910c9de71018e135079124723424307ecfa26f13c28b67168da674be53516`  
		Last Modified: Sat, 16 Mar 2024 00:03:55 GMT  
		Size: 345.9 KB (345950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d89541af641c08a1a8628c51a58e38d1789444896e7c47a42c7cb176b043aa`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e262ff571edbf09e77eef8e33e138948eb43aa0aae511d14f10f3a910f2ae4`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a39e11aba6703bd269a0a633a00da1d03f44f365c7173a36de71677fc841adf`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26714a18e8b1a42e2d38096f45fbf75e1d0f76fe68c1948e36edae9256c98c4`  
		Last Modified: Sat, 16 Mar 2024 00:04:05 GMT  
		Size: 197.5 MB (197547477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89270f1447ed53cbcf0273a00dd0b9a0fd1d636ec1bd3b2cfca3b139c6e551c3`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
