## `openjdk:27-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:0f1917272b13b1c1da81b8131ba2f9b355424c3862f3382cbed94e124a01df4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:27-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:7d859c1b2378ad3253e2b654a7bd6f707fa8ec73eb2fa6c969addfba8c19ee26
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1721185849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651f5f69ec50448acefcd6ebe54218772bd068d9e11033f300e9fee07cda4e39`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:08:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:34 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 22:08:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:39 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:08:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:08:41 GMT
ENV JAVA_SHA256=dad15ea855765f796d0a975373f5f6aa7e247d717d129641177c41ee0cbe211c
# Mon, 26 Jan 2026 22:09:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:09:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a1ee0bf0167df6115953b6b1b098fa7a7d283b273426e6102f22f9f9cda0ab`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 403.9 KB (403850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48792ea1b7025d5b1254b2044b585783cbec73f35e438ff315edd7d77db07472`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c729d92fcc29b96e35583ec02da675ce9c8fb502e913f8fec07ceb5600d74a`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 388.8 KB (388796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442a4e75aa3f26e3e8f67ca78b91e4f42f950497956d9d357722aa918051f139`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af94527c78e3478cc47da34e9d0a8333a10af87043c6239e5a3c6c519e3e8116`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c936ac13317978a6f488e1712e5c16379ebaae55ef169b5015d4cc0a207c0a`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40d0fbb771a150b90d600acb5d48bc7182a335e1011814b69ebe9d6d3c1e882`  
		Last Modified: Mon, 26 Jan 2026 22:09:36 GMT  
		Size: 224.6 MB (224625010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609f3fe84f8db0453942811ffc4bca8a6c16f9244eaddb4132c8cdace10323f9`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
