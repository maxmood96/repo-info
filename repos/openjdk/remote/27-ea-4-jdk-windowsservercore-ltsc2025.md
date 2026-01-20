## `openjdk:27-ea-4-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:a32d66d4de648d590b41df3113bd10b5ed895bf75095d5173150b3d915d4ad0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:27-ea-4-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:f6fe9daecd84da6d1e1e691c171b9aa9685291b463b900847a006c98e2fa7420
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f65302859abb515129f1dec963ad4c304a2fbe6d247164a0eefd0394ccbb43`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:00:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:00:46 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 13 Jan 2026 23:00:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:00:52 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 23:00:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Tue, 13 Jan 2026 23:00:54 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Tue, 13 Jan 2026 23:01:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c348082658f8a5ab278a6856dfa04fa2a0bb282804f2a57c36436a6688e78`  
		Last Modified: Tue, 13 Jan 2026 22:58:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da49a7f48a8c8a72f9029b2060d520ec51aff2040a883199f800be0e23b6781`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 401.6 KB (401627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b883a1aaca55ac0ddb6ea87618bc903e2384d419dff78ab3111b8c7d7d00b`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743279e77085da41e412ceadf20e068d4cec0712b4a4bd18027fcef50afff768`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 388.4 KB (388395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e68fe60762d7163005606dc0a6a7fbd8f3ee3c40cdcf22e1d73fc2069932468`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed2dd9d2d48687deb3f810080590e3bdace26052455ecf060f50f4e26da6797`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb5d749a0778cebc1fd0e469ce99d6d9d425fdc7ecb308795e4527eebda1822`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd1144ea2cb72a26c87648f037ccd9d5375d2f300af1c4ecca7781ad249222b`  
		Last Modified: Tue, 13 Jan 2026 23:02:10 GMT  
		Size: 224.3 MB (224314938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf834ae3de2bc4dc54c4704299b7aeca438edb1d40094664d1119fb1cfd27063`  
		Last Modified: Tue, 13 Jan 2026 23:01:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
