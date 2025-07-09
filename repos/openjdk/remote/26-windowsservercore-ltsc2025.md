## `openjdk:26-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:1e71a84ceebc36bb907d14678d02c8f5f395826ee9b520e1840a17e1f44cfcfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `openjdk:26-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull openjdk@sha256:f7ba37f27f987642d0df4e8306d6f7320a8d7660b655c232c986aa2b6d81512b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3710833205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae14b9b4564aa8e416943839e9efdd51764a82cc0c3dc50ceee3ba455500296`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 09 Jul 2025 18:09:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:51 GMT
ENV JAVA_VERSION=26-ea+5
# Wed, 09 Jul 2025 18:09:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_windows-x64_bin.zip
# Wed, 09 Jul 2025 18:09:53 GMT
ENV JAVA_SHA256=884a05860f9ed48a9a26e95900c90750b220618efe84857aa27061fd3657fee3
# Wed, 09 Jul 2025 18:10:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:10:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f7d7e7b74d17a3a394e43e6fc08aa4ae8e9ac6b0d8868e014e74d1617b2a21`  
		Last Modified: Wed, 09 Jul 2025 19:09:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908098a74bdc5a385c002b7d3d64a8a92e3163a8c27f70ed6f9d96b044973c6`  
		Last Modified: Wed, 09 Jul 2025 19:09:29 GMT  
		Size: 391.1 KB (391108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee377c238d243697b29d9d96e4b068c10110db519d39f4ea4b4ffcb32add8b2`  
		Last Modified: Wed, 09 Jul 2025 19:09:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a2c6262721621531ff32c8fa8e56c908bea6250df4210781edeb769f0e768e`  
		Last Modified: Wed, 09 Jul 2025 19:09:33 GMT  
		Size: 375.1 KB (375062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27487be9b1cda83f642d4dc075a21628efb78d71bceee618978394c2d46cf891`  
		Last Modified: Wed, 09 Jul 2025 19:09:34 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb646b13ab8c4fdb021be772b164088ef14e35e2ccd9a6c141eb91b1f7dc11c5`  
		Last Modified: Wed, 09 Jul 2025 19:09:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8841445d721659485ecd7312a69c7a799028195ffc05b65215beef5a18019a`  
		Last Modified: Wed, 09 Jul 2025 19:09:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc54772b30e36a3d952380debe6749f8440c8d41005ebd7f544d97cd953128`  
		Last Modified: Wed, 09 Jul 2025 19:09:49 GMT  
		Size: 218.9 MB (218885902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ae451d09b6531c75d7b1fc70cfdc4ee788b2ab0ed21397bbd16c943178b176`  
		Last Modified: Wed, 09 Jul 2025 19:09:50 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
